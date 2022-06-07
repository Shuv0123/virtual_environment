## What is an Open Source software?
- An Open source software is freely available code used to create the software which anyone can inspect, modify and update. So anyone can contribute to improve the software to make it better.


## Linux - Ubuntu distro
- `whoami` tells you which user you are 
- `sudo -i` become root user 
- `cd /` it takes you to root directory
- folder `bin` contains user executable commands folder `sbin` contains system executable commands
- `cat /etc/os-release` tells you information about the machine
- how to check all process `top`
- who am i `uname` or `uname -a`
- where am i `pwd`
- create a dir `mkdir dir_name`
- how to check my files `ls` or `ls -a`
- more info about the file `ls -l`
- how to create a file `touch name_file` or `nano file_name`
- how to check content of the file without going inside the file `cat file_name`
- how to move a file `move file.txt` from current location to sre folder
- how to delete folder sudo` rm -rf folder_name`
- navigate to any folder change dir `cd nameoffolder`
- how to change back to home location or any location `cd ..` or `cd` enter
- how to copy file `cp nameoffile newnameoffile`
- cut and paste file in a new dir `mv filename filelocation`
- how to switch to root user `sudo su`
- how to create/lunch a process for 30 sec - `timeout DURATION comman` eg. `timeout 30s www.bbc.co.uk`
- (nginx is a web server used as reverse proxy)
 (sudo = gives admin access, apt-get = package manager, install = instruction and the last is what we want install)
- to check what type of file it is `file name_of_file`
- if you wanna replace a word externally you can use sed command `sed -i 's/old_word/new_word/g' path_to_folder`
- `echo` is a print command `echo "hello"` it will print hello
- to download a file we use `curl https://link_of_the_download_file -o name_how_you_want_to_save-file`
   - the `-o` means the output of the link
## ubuntu commands
- Update  `sudo apt-get update -y`
- Upgrade `sudo apt-get upgrade -y`
- How to start a service `sudo systemctl start name_service`
- how to stop a service `sudo systemctl stop name_service`
- how to check status `sudo systemctl status service_name`
- how to enable service `sudo systemctl enable service_name`
- how to install a package `sudo apt install package_name -y`
- how to remove a package `sudo apt remove package_name -y`
- how to check runnning processes in linux `top` or `ps aux`
- how to delete/ remove /kill any process `kill processid` force kill `kill -9 processid`

## Environment Variables

- how to check exisiting Environmnet variable, `printenv`
- how to create an env var, we use key word `export` eg. `export `NAME=Shuvo`
- how to manke an env var persitent on linux ubuntu - `nano .profile` and `export EnvName=value` at the bottom of the file. Then exit
- to make a variable permanent:
   - `vi /etc/profile`
   - create variable eg `DB_HOST='123` and save 

## File permisions
- In vagrant we will write a script that contains a set of commands (instruction) from the user to OS, the script is called provision.sh using `nano provision.sh`
- how to check a file permision `ll`
- change file permision `chmod required_permision file_name` eg. `chmod +x filename`
- `drwxr-xr-x` d means it is a directory the rwx permission user-group-others  (u, g, o) use + or - to add or remove permission
   - chmod g+x filename
### calculate permission numeric method
permission can be granted using a 3 digit number and eg 400 the first digit is for user the next is for group and last for others
   - `4` (read)
   - `2` (write)
   - `1` (execute)
- eg `chmod 641 filename` user has rw permission, group has r permission and others have x permission only
- read only permission `chmod 400 filename`
- write `w` read `r` exe `x`
- https://chmod-calculator.com/


## vim commands
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
- replace word in vim `:%s/old_word/new_word/g` g stands for globally



