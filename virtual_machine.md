# Virtual Environment
- A Virtual Environment is an environment for everyone to use, weather is development, testing or deployment whatever it may be. We create this environmnet so that evryone has the same tool to collaborate together, this is beneficial because no matter what device we use we gonna end up with the same results.

- I used Vagrant to create a virtual environment through a vegrantfile, which was created in my local machine(host). In order for Vagrant to create a virtual machine I used VirtualBox, which all together provided information to the Virtual machine to run.

![](images/VM.png)

## how to set up internet on VM?

- to make sure that we have internet available from our local host
- `sudo apt-get update`. if this does not work, `exit` the vagrant and do `vagrant reload`
- `sudo apt-get upgrade`



## Vagrant commands
- to boot up vagrant - `vagrant up`
- to delete vagrant - `vagrant destroy`
- to pause vagrant - `vagrant halt`
- to check status of machine -  `vagrant status`


Whenever we add new functionality to our vagrant file that means we need to let the virtual box know there are new sets of commands so that it can implement those instructions inside the VM. There are two options we either do `vagrant up` followed by `vagrant destroy` so that it reboots with the newly added data or we can do `vagrant reload` which is quicker (if this doesn’t work use the other options). When we do vagrant reload, what happens is that vagrant goes to the local machine starts to read the vagrantfile pickup the ip address and tells virtualbox to inject this ip into this virtual machine to use the network available in the localhost.



## Linux - Ubuntu distro
- Update  `sudo apt-get update -y`
- Upgrade `sudo apt-get upgrade -y`
- How to start a service `sudo systemctl start name_service`
- how to stop a service `sudo systemctl stop name_service`
- how to check status `sudo systemctl status service_name`
- how to enable service `sudo systemctl enable service_name`
- how to install a package `sudo apt install package_name -y`
- how to remove a package `sudo apt remove package_name -y`
- how to check all process `top`
- who am i `uname` or `uname -a`
- where am i `pwd`
- create a dir `mkdir dir_name`
- how to check `ls` or `ls -a`
- how to create a file `touch name_file` or `nano file_name`
- how to check content of the file without going inside the file `cat file_name`
- how to move a file `move file.txt` from current location to sre folder
- how to delete folder sudo` rm -rf folder_name`
- navigate to any folder change dir `cd nameoffolder`
- how to change back to home location or any location `cd ..` or `cd` enter
- how to copy file `cp nameoffile newnameoffile`
- cut and paste file in a new dir `mv filename filelocation`
- how to check runnning processes in linux `top` or `ps aux`
- how to delete/ remove /kill any process `kill processid`
- how to switch to root user `sudo su`
- how to create/lunch a process for 30 sec - `timeout DURATION comman` eg. `timeout 30s www.bbc.co.uk`
- (nginx is a web server used as reverse proxy)
 (sudo = gives admin access, apt-get = package manager, install = instruction and the last is what we want install)


## Environment Variables

- how to check exisiting Environmnet variable, `printenv`
- how to create an env var, we use key word `export` eg. `export `NAME=Shuvo`
- how to manke an env var persitent on linux ubuntu - `nano .profile` and `export EnvName=value` at the bottom of the file. Then exit


## File permisions
- In vagrant we will write a script that contains a set of commands (instruction) from the user to OS, the script is called provision.sh using `nano provision.sh`
- how to check a file permision `ll`
- change file permision `chmod required_permision file_name` eg. `chmod +x filename`
- - read only permission `chmod 400 filename`
- write `w` read `r` exe `x`
- https://chmod-calculator.com/
## Bash scripting - Automate process with the script
### Code block:

```bash
# create a file called provision.sh

# it must start with #!/bin/bash

#!/bin/bash

# run updates
sudo apt-get update -y
# run upgrades
sudo apt-get upgrade -y

# install nginx
sudo apt-get install nginx -y      

# ensure it's running - start nginx
sudo systemctl start nginx

# enable nginx
sudo systemctl enable nginx
```
- change the file to exe `chmod +x provision.sh`
- how to run an exe file `./provision.sh`