Adding New Users With SSH Access
--------------------------------

```
adduser username
```
and then place their public key in 

`/home/username/.ssh/authorized_keys`

ensuring that both `.ssh` and `authorized_keys` are owned by username:username, either via `su` or `chown`


Note also that we enable specific user access in `/etc/ssh/sshd_config` ...

```
AllowUsers sigu sam sysrex
```

So we need to add new users to this list and then restart the ssh service if we want new folks to be able to log in:

```
sudo service ssh reload
```

If the user needs sudo access use the following:

```
usermod -aG sudo username
```
