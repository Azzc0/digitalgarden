---
{"dg-publish":true,"permalink":"/linux/snippets/"}
---

# Pulseaudio - Swap L/R channels
Edit file `/usr/share/pulseaudio/alsamixer/profile-sets/default.conf`

Look for the relevant section, similar to this:
```
[Mapping analog-stereo]  
device-strings = front:%f hw:%f  
channel-map = left,right
```
Change the order from "left, right" to "right,left". A restart of the service might be required: `pactl exit`
