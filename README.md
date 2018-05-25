# Conquest Server Startup Scripts (1.0.0)
Startup scripts for the Conquest game server - uses the "screen" command to manage a session. This also restarts the Conquest Server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/ConquestStartup) - [Official Forum](https://conquest.gameplayer.club/index.php/forum/startup-scripts) - [Official Downloads](https://conquest.gameplayer.club/index.php/downloads/category/8-conquest-sysadmin-tools)

---
These start up the Conquest server at boot time with a "screen" process.

1. Copy **conquest** into **/etc/init.d** - make sure it is executable
2. Copy **startconquest** into **/root/conquest** - make sure it is executable
4. Run "**systemctl enable conquest**" (only needed once, will stick)
5. Run "**systemctl start conquest**" - starts Conquest server without restarting the whole server

When you want to view the conquest console, just enter "**screen -r**" in your shell.

To disconnect from the conquest console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/conquest/nostart**". To reenable it type "**rm /root/conquest/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
