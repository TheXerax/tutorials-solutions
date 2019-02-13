# Screen tearing in Ubuntu 18.04 (Intel HD Graphics)

This simple tutorial solves the screen tearing in Ubuntu 18.04 (tested in Budgie flavour). These are the steps:

1) Check if you have Intel HD Graphics:

`lspci -nn | egrep -i "3d|display|vga"`

2) Create the file */etc/X11/xorg.conf.d/20-intel.conf* (if the directory doesn't exists, you have to create it):

`sudo nano /etc/X11/xorg.conf.d/20-intel.conf`

3) Then add these lines to the file:

```
Section "Device"
 Identifier "Intel Graphics"
 Driver "intel"
 Option "TearFree" "true"
EndSection
```

4) Reboot your system and enjoy!

Source: [link](https://www.youtube.com/watch?v=IJeX35wbZY4)
