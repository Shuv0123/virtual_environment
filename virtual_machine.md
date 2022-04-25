# Virtual Environment
We are using Vagrant to create a virtual environment through a vegrantfile, which will be created in the local host. In order for Vagrant to create a virtual machine we need VirtualBox, which all together will provide information to the Virtual machine to run.

# how to set up internet on VM?

- to make sure that we have internet available from our local host
- 'sudo apt-get update'. if this does not work, 'exit' the vagrant and do 'vagrant reload'
- 'sudo apt-get upgrade'

---

# Vagrant commands
- to boot up vagrant - 'vagrant up'
- to delete vagrant - 'vagrant destroy'
- to pause vagrant - 'vagrant halt


---

Whenever we add new functionality to our vagrant file that means we need to let the virtual box know there are new sets of commands so that it can implement those instructions inside the VM. There are two options we either do 'vagrant up' followed by 'vagrant destroy' so that it reboots with the newly added data or we can do 'vagrant reload' which is quicker (if this doesn’t work use the other options). When we do vagrant reload, what happens is that vagrant goes to the local machine starts to read the vagrantfile pickup the ip address and tells virtualbox to inject this ip into this virtual machine to use the network available in the localhost.



### Linux - Ubuntu distro
- Update 'sudo apt-get update -y'
- Upgrade 'sudo apt-get upgrade -y'
- Who am I 'uname' or 'uname -a'
- where am I 'pwd'
- how to check files/folders in existing location 'ls' or 'ls -al'
- how to create dir 'mkdir nameoffolder'
- navigate to anyfolder - change dir 'cd nameoffolder'
- how to change back to home location or any location 'cd ..' or 'cd' enter
- how to create a file 'touch filename' or 'nano filename'
- to see the content of the file on terminal 'cat filename'
- how to copy file 'cp nameoffile newnameoffile'
- cut and paste file in a new dir 'mv filename filelocation'
- how to delete file or folder 'rmdir' or force delete 'rm -rf foldername'
- how to check runnning processes in linux 'top' or 'ps aux'
- how to delete/ remove /kill any process 'kill processid'

---

### Permission 
- how to check permission "ll"
- how to switch to root user 'sudo su'
- how to change permisision 'chomd instruction filename'
- change permision to executable 'chmod +x filename'
- read only permission 'chmod 400 filename'
- how to create/lunch a process for 30 sec - 'timeout DURATION command' eg. 'timeout 30s www.bbc.co.uk
- how to install a product - install webserver called 'nginx' (nginx is a web server used as reverse proxy)
- sudo apt-get install package_name (sudo = gives admin access, apt-get = package manager, install = instruction and the last is what we want install)
- how to check if the product is running (status) - 'systemctl status nginx'

---

### Automate process
in vagrant we will write a script that contains a set of commands (instruction) from the user to OS, the script is called provision.sh using 'nano provision.sh' - update - upgrade - install nginx - enable nginx 
![](images/nano_provision.sh.jpeg)

---

### Environment Variables
- how to check exisiting 'Env var', 'printenv'
- how to print specific env var
- how to create an env var, we use key word 'export' eg. export NAME=Shuvo
- how to manke an env var persitent on linux ubuntu - 'nano .profile' and 'export EnvName=value' at the bottom of the file. Then 'exit
