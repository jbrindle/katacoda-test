Labels are automatically generated and added to objects at creation time. 

Try making a new file in your home directory:
```
touch foo
```{{exectute T1}}

Next look at its label:
```
ls -Z foo
```{{execute T1}}

As you can see the label is `unconfined_u:object_r:admin_home_t:s0`. 

Now create a file in a different directory such as `/tmp`:
```
touch /tmp/foo
```{{execute T1}}

and look at its label:
```
ls -Z /tmp/foo
```{{execute T1}}

This file has the label `unconfined_u:object_r:user_tmp_t:s0`, which has a different type than the other file.

SELinux label generation for files use the directory the file is being created in to determine what the new file will be labeled.
