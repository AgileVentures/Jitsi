Adding New Users With SSH Access
--------------------------------

```
adduser username
```
and then place their public key in 

`/home/username/.ssh/authorized_keys`

ensuring that both `.ssh` and `authorized_keys` are owned by username:username, either via `su` or `chown`
