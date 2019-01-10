# Spotify stuck in fullscreen in Ubuntu 18.04

This is a solution for the Spotify bug in Ubuntu. Sometimes, the app stucks itself in fullscreen mode, beeing unable to minimize it and preventing ou to get access to the dock.

1) Install wmctrl if ou don't have it.

2) Pause the music and run "wmctrl -r spotify -b toggle,fullscreen" while spotify is running.
