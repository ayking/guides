# SFTP Setup

### Creating user
`$sudo adduser alan`

### Creating directory for file transfer
`$sudo mkdir -p /sftp-home/uploads`

`$sudo chown root:root /sftp-home`

`$sudo chmod 755 /sftp-home`

`sudo chown alan:alan /sftp-home/uploads`

`$sudo chmod 740 /sftp-home/uploads`

### Update SSH config

`$sudo vim /etc/ssh/sshd_config`

Add the following lines

```
Match User alan
PasswordAuthentication yes
ForceCommand internal-sftp
ChrootDirectory /sftp-home
PermitTunnel no
AllowAgentForwarding no
AllowTcpForwarding no
X11Forwarding no
```

### Restart and test

`$sudo systemctl restart sshd`

`ssh alan@xxx.xxx.xxx.xxx` should fail

`sftp alan@xxx.xxx.xxx.xxx` should ok

