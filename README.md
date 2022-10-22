# Beaglebone_blue_getting_start

### Auto Execute Program on Startup
Reference [Link1](https://stackoverflow.com/questions/28854705/executing-a-script-on-startup-using-beaglebone-black) | [Link2](https://gist.github.com/tstellanova/7323116)

| Instruction | Command |
|------------ | --------|
| Go to root | `$ cd ~/`|
| Create folder  | `$ mkdir <folder name>`|
| Put simulink files inside folder ||
| Create a bash script that will launch the code at boot/startup | `$ cd /usr/bin/nano <bash file name> Ex(FAVBash.sh)` |
| Type in bash script | `$ #!/bin/bash`<br />`$ cd /home/debian/<name of folder>`<br />`$ sudo ./<name of simulink files> Ex(FAV.elf)` |
| Save and grant execute permission |`$ sudo chmod u+x /usr/bin/<name of bash file>`|
| Create the service |`$ sudo nano /lib/systemd/system/<name of service file> Ex(FAVservice.service)`|
| Type in service script|`[Unit]`<br />`Description=description of code`<br />`After=syslog.target network.target`<br />`[Service]`<br />`Type=simple`<br />`ExecStart=/usr/bin/<name of bash file>`<br />`[Install]`<br />`WantedBy=multi-user.target`|




### Shutdown BBB
```
$ sudo shutdown now
```
