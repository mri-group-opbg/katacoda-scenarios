# Play with FreeSurfer

Suppose you want to execute `recon-all` in FreeSurfer.

Let's prepare our environment!

Run the following command to write your license in the file `license.txt`:

`
cat <<EOT > license.txt
elena.swa@hotmail.it
31311
 *CA5LKFSazHnE
 FSJHQF00tpWss

EOT
`{{execute}}

Download sample MRI data to be processed:

`wget https://github.com/mri-group-opbg/katacoda-scenarios/raw/master/assets/anat.nii.gz`{{execute}}

Create the area for your results

```
mkdir subjects
```