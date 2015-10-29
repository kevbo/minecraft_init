# A Minecraft init script for CentOS 6 (pre-systemd)

There's a [great tutorial](https://teilgedanken.de/Blog/post/8/) I found for getting a Minecraft server up and running, by way of Spigot. Unfortunately, the tutorial
is for CentOS 7, which uses systemd instead of System V init. I don't have strong opinions about using one or the other, but
I did need a compatible way to ensure Minecraft got started. After reading through `/usr/share/doc/initscripts-*/sysvinitfiles`
and looking at some other examples, this is what I came up with. Corrections/feedback/patches all welcome!

## Installation
1. As root, copy this script to /etc/init.d
2. Give it the same permissions as the rest of your init scripts (probably 750)
3. Register it with `chkconfig` (e.g., `chkconfig --add minecraft`)
4. Start it up (e.g., `service minecraft start`)

## Usage
* Start: `service minecraft start`
* Stop: `service minecraft stop` (Note: this uses `mcrcon` to connect to RCON and call `stop`)
* Restart: `service minecraft restart` (Calls stop, then start)
