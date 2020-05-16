# pptp
Note, please back up the system, please back up the system, please back up the system. Say important things three times
pptp for macOS Catalina

Mac OS Catalina completely disables VPN of PPTP protocol, but we can overwrite or add these three files

/usr/local/bin/pptp  

/System/Library/Extensions/PPTP.ppp 

/System/Library/Extensions/PPP.kext 


First of all, your system version must be below 10.15.3. Someone in the forum said that the higher version system could not succeed.

After copying, try to give the driver file permission

sudo chmod -R 755 /System/Library/Extensions

sudo chown -R root:wheel /System/Library/Extensions

If you still can't connect, try connecting CPN manually in the terminal

sudo pppd call xxxxx
