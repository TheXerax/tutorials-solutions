# How to stop Bluetooth from starting automatically on system startup in Ubuntu 18.04

Ubuntu 18.04 automatically starts bluetooth on system startup. This could be frustranting, so here I have a simple solution:

1) You will only need to edit/make the rc.local file. Most Linux distros doesn't have it, so you have to create it and make it executable. We will enter the lines we need too:

```
sudo install -b -m 755 /dev/stdin /etc/rc.local << EOF
#!/bin/sh
rfkill block bluetooth
exit 0
EOF
```

2) Reboot your system and you will see that bluetooth stops at system startup.
