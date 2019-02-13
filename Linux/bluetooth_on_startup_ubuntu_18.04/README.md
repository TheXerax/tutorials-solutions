# How to stop Bluetooth from starting automatically on system startup in Ubuntu 18.04

Ubuntu 18.04 automatically starts bluetooth on system startup. This could be frustranting, so here I have a simple solution:

1) You will only need to edit/make the rc.local file. Most Linux distros doesn't have it, so you have to create it and make it executable. We will enter the lines we need too:

- Create the file:

`sudo touch /etc/rc.local`

- Open it with nano and insert these lines:

```
#!/bin/sh
rfkill block bluetooth
exit 0
```

2) Then you need to change the file permissions:

`sudo chmod 755 /etc/rc.local`

3) Reboot your system and now you will see that bluetooth is disable
