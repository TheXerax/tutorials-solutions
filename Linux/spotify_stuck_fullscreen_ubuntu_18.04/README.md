# Spotify stuck in fullscreen in Ubuntu 18.04

This is a solution for the Spotify bug in Ubuntu 18.04. Sometimes, the app stucks itself in fullscreen mode, being unable to minimize it and preventing you to get access to the dock.

1) Install wmctrl if you don't have it.

`sudo apt install wmctrl`

2) Pause the music and run this command while Spotify is running:

`wmctrl -r spotify -b toggle,fullscreen`
