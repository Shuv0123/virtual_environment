## What is an Open Source software?
- An Open source software is freely available code used to create the software which anyone can inspect, modify and update. So anyone can contribute to improve the software to make it better.


## Linux - Ubuntu distro
- `whoami` tells you which user you are 
- `sudo -i` become root user 
- `cd /` it takes you to root directory
- folder `bin` contains user executable commands folder `sbin` contains system executable commands
- `cat /etc/os-release` tells you information about the machine
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


## vim
- vim has 3 modes
  - command mode
  - inseert mode (edit)
  - extended command mode
- to create a file `vim name_of_file.txt`
- to get into insert mode type `i` in vim environment
- `o` can also be used to get into insert mode but it will take you one line below
- after editing, to go from insert mode to command mode press `esc` botton and then press `:w` to save the file 
- `:q!` forcefully quit without saving anything
- `:se nu` to see line numbers
- `shift + g` will take you to the bottom of the file
- if you are at the bottom, to go back to the first line `gg` (in command mode)
- to copy a line `yy` and to paste `p` small p to paste below and capital p to paste above
- if you wanna copy multiple lines in a row go to the line you intersted and `4 yy` this will copy 4 lines from whichever line you are 
- `dd` to delete a line 
- `u` to undo
- to cut paste do `dd` then `p`
- to search for a word, in comand mode `/word_you_are looking_for` this will highlight the word you are looking for ( this is case sensitive)  
