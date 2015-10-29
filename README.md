# A Minecraft init script for CentOS 6 (pre-systemd)

There's a [great tutorial](https://teilgedanken.de/Blog/post/8/) I found for getting a Minecraft server up and running, by way of Spigot. Unfortunately, the tutorial
is for CentOS 7, which uses systemd instead of System V init. I don't have strong opinions about using one or the other, but
I did need a compatible way to ensure Minecraft got started. After reading through `/usr/share/doc/initscripts-*/sysvinitfiles`
and looking at some other examples, this is what I came up with. Corrections/feedback/patches all welcome!
