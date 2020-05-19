All objects and subjects on an SELinux system have a label. 

```
ls -Z .
```{{execute T1}}

As you can see there is a file called `helloworld` that has the label `unconfined_u:object_r:admin_home_t:s0`.

The label has multiple components. In the label above you see:

|  Component    | Value        |
| --------------|--------------|
| SELinux user  | system_u     |
| Role          | object_r     |
| Type          | admin_home_t |
| MLS Level     | s0           | 

Each of these components is used differently by SELinux. For now we will focus on the type, in this case `admin_home_t`.

Next find out the label of your shell:
```
id -Z
```{{execute T1}}

As you can see your shell has the label `unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023`.


