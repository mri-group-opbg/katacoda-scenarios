Try to run the command:

```
docker pull freesurfer/freesurfer:6.0
```

In 4-5 minutes you will have a running Freesurfer in your environment (it is a 5 Giga package!!!)

Run the following command to write your license in the file `license.txt`:

cat <<EOT > license.txt
elena.swa@hotmail.it
31311
 *CA5LKFSazHnE
 FSJHQF00tpWss

EOT

```
wget https://github.com/mri-group-opbg/katacoda-scenarios/raw/master/assets/anat.nii.gz
```

```
mkdir subjects
```

```
docker run --rm \
    -v $(pwd)/anat.nii.gz:/input/anat.nii.gz \
    -v $(pwd):/opt/freesurfer/subjects \
    -v $(pwd)/license.txt:/opt/freesurfer/.license \
        freesurfer/freesurfer:6.0 \
            recon-all -i /input/anat.nii.gz -s result -all
```

Open another terminal

```
ls -lh subjects/tizio
```

See the size of data produced:

```
du -h subjects/tizio
```

See docker command running with

```
docker ps
```

Take the first column: it's the UUID of the recon-all container.

you can stop it with:

```
docker stop <uuid>
```

If you launch the recon-all continer with the parameter `--name recon-all` you will be able to delete it with 

```
docker stop recon-all
```

Try it!
