To find out if SELinux is currently enforcing its policy you can use:
```
getenforce
```{{execute T1}}

If you see `enforcing` then the policy is currently being enforced.

Setting the enforcing mode is similar, but takes an argument:
```
setenforce 0
```{{execute T1}}

Now check enforcing mode:
```
getenforce
```{{execute T1}}

It should say `permissive`.

Switch back to enforcing:
```
setenforce 1
```{{execute T1}}

