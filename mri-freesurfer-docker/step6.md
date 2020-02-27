```
docker run \
    --rm \
    --name recon-all \
    -v $(pwd)/anat.nii.gz:/input/anat.nii.gz \
    -v $(pwd):/opt/freesurfer/subjects \
    -v $(pwd)/license.txt:/opt/freesurfer/.license \
        freesurfer/freesurfer:6.0 \
            recon-all -i /input/anat.nii.gz -s result -all
```{{execute}}

While recon-all is running *open another terminal* with the following:

`ls -lh subjects/tizio`{{execute T2}}

See the size of data produced:

`du -h subjects/tizio`{{execute}}

See docker command running with

`docker ps`{{execute}}

Take the first column: it's the UUID of the recon-all container, and the name of the container is `recon-all`

You can stop selecting it by name with:

`docker stop recon-all`{{execute}}
