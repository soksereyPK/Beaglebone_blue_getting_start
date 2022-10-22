# Beaglebone_blue_getting_start

### Auto Execute Program on Startup
Reference [Link1](https://stackoverflow.com/questions/28854705/executing-a-script-on-startup-using-beaglebone-black) | [Link2](https://gist.github.com/tstellanova/7323116)

| Instruction | Command |
|------------ | --------|
| Go to /usr/bin | `$ cd /usr/bin `|
| Create sh file | `$ touch myfunction.sh`|
| Edit the file content | `$ nano myfunction.sh`|
| In file content, Put in | `#!/bin/bash`<br />`cd ~/folder/ # this line is go to the directory of the executable code`<br />`./funtion # this line is for executing the programe (can be sudo python3 function.py)` |
| Save and Make the file executable | `$ sudo chmod u+x myfunction.sh` |




### Shutdown BBB
```
$ sudo shutdown now
```
