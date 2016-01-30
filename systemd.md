
###Service Control
```
systemctl #list all running services

systemd-cgls #list running services in a tree format

systemctl start foo #Start foo

systemctl stop foo  #Stop Foo

systemctl restart foo #Restart foo

systemctl status foo  #Show Status of foo

systemctl enable foo  #Start on boot

systemctl disable foo #Disable boot startup
```
###RunLevels (Targets)

Run level 3 is emulated by multi-user.target
Run level 5 is emulated by graphical.target
runlevel3.target is a symbolic link to multi-user.target
runlevel5.target is a symbolic link to graphical.target
```
systemctl isolate multi-user.target #switch to 'runlevel 3'

systemctl isolate graphical.target  #witch to 'runlevel 5' by running

systemctl set-default <name of target>.target  #Change Default Target

systemctl get-default #Check Current Target
```
