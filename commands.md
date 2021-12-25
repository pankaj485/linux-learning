[Hard Links & Soft Links](#hard-links--soft-links)

[List File (ls)](#list-file-ls)

[Environment Variables](#environment-variables)

[Editing Files](#editing-files)

[Pseudo File System dev/proc/sys](#pseudo-file-system-devprocsys)

[Find Files](#find-files)

[Compression and Decompression](#compression-and-decompression)

[Touch Command](#touch-command)

[Create and Remove Directories](#create-and-remove-directories)

[Copy Paste Move and Rename Files in Linux](#copy-paste-move-and-rename-files-in-linux)

[Keyboard Shortcuts in Linux](#keyboard-shortcuts-in-linux)

[Command Line History in Linux](#command-line-history-in-linux)

[Head and Tail Commands](#head-and-tail-commands)

[wc Command in Linux](#wc-command-in-linux)

[Package Management Search Install Remove](#package-management-search-install-remove)

[Logging](#logging)

[Services](#services)

[Processes](#processes)

[Kernel Modules](#kernel-modules)

[Adding and Changes Users](#adding-and-changes-users)

[User Groups & User Privileges](#user-groups--user-privileges)

[Network UI](#network-ui)

[Basic Troubleshooting](#basic-troubleshooting)

[Informational Utilities](#informational-utilities)

[IP Tables](#ip-tables)

[Netcat](#netcat)

[BASH Scripts](#bash-scripts)

## Few Example Commands

- `pwd`: print working directory
- `cd`: change directory
- `cd /`: comes back to the previous working directory
- `ls`: list folders and files in the present working directory
- `ls .`: shows all the files and folders on the present directory
- `ls ..`: shows all the files and folders one directory above

---

## Hard Links & Soft Links

- Creating Hard Link `ln <orignalFileName> <hardLinkName>`
- Creating Soft Link `ln -s <orignalFileName> <softLinkName>`

---

## List File (ls)

- `ls`: list all files and folders
- `ls -l`: list in long format
- `ls -a`: shows all the files including hidden ones (_starting with dot extension_)
- `ls -al`: shows a list of all files including hidden ones in long format
- `ls -lS`: sorts all the list (_the command has the uppercase letter ”S”_ )
- `ls -lS > filename.txt`: creates a file with name `filename` and copies all the contents showed through the command `ls -lS` into it
- `man ls`: shows all the information about commands related to `ls`

---

## Environment Variables

- To access values stored for each environment variable: `echo $path`
- Create new variable: `variableName=values`
- accessing the variable: `echo $PANKVAR`
- Removing the existing value: `unset variableName` (_don’t use $ while unset_)

---

## Editing Files

- creating a text file and writing into it: `echo "contents to add here" > filename.txt`
- editing a text file: `nano filename.txt`
- see the contents of the file: `cat filenam.txt`

---

## Pseudo File System dev/proc/sys

- list all the devices system has: `ls /dev/` (_pwd: root_)
- list all the process and their id: `ls /proc/`
- to see the details of the process running: `cd /proc/<anyProcessID> && ls`

---

## Find Files

- to search for the file with their name: `find . filename`
- to search for specific name of the file: `find . -name "filename"`
- to find all the files containing the passed string in file system: `locate <textToSearch>`

---

## Compression and Decompression

- To compress a file: `gzip filename`
- To decompress a file: `gunzip filename`
- create a compressed folder having files name.txt and hello.txt `tar cvf compressedFile.tar name.txt hello.txt`
- decompress a compressed folder `tar xvf compressedFile.tar`

---

## Touch Command

- To create a new file: `touch filename.fileformat`

---

## Create and Remove Directories

- Create directory: `mkdir directoryName`
- Remove directory: `rm -r directoryName` or `rmdir directoryName`

---

## Copy Paste Move and Rename Files in Linux

- copy the file contents: `cp filenameToPick filenameToCopyTo`
- rename the file: `mv fileName newName`
- move the file: `mv fileName directoryToMoveTo`

---

## Keyboard Shortcuts in Linux

- `ctrl + shift + n`: create a new folder
- `Alt + HOME`: navigates to the home
- `Alt + F4`: closes the window
- `Ctrl + Alt + T`: opens terminal
- `Alt + F2`: prompt to write command
- `Ctrl + D`: removes the line

---

## Command Line History in Linux

- list history of commands: `history`
- execute command of particular index: `!indexOfCommand` (_no space after “!”_ )
- see small list of the commands only: `history | less` (max _500 commands_)

---

## Head and Tail Commands

- Head: `head -number filename.txt`
- Tail: `tail -number filename.txt`
- Read 2 files together: `head file1.txt file2.txt`

---

## wc Command in Linux

- command: `wc filename.txt`
- to know only characters: `wc -c filename.txt`
- to know only lines: `wc -l filename.txt`
- to know only words: `wc -w filename.txt`

---

## Package Management Search Install Remove

- Search a package: `apt-cache search packageName`
- Install a package: `sudo apt-get install packageName`
- Uninstall a package: `sudo apt-get remove packageName`
- Completely remove package and files: `sudo apt-get purge packageName`

---

## Logging

- logs are present in `/var/log` directory
- to see log contents: `cat /var/log/filename.log`

---

## Services

- list all services running on the background: `service --status-all`
- check status of specific service: `service serviceName status`
- stop particular service: `service serviceName stop`
- restart particular service: `service serviceName restart`

---

## Processes

- list process running in background: `ps`
- To run particular process in background: `processNam &` (_It returns the process id_)

---

## Kernel Modules

- These are stored in `/lib/modules`
- list all available modules: `lsmod`
- removing modules: `sudo rmmod moduleName`
- installing modules: `sudo insmod pathToInstall/moduleName.extension` (_note that modules are listed in /lib/modules/ directory_ )

---

## Adding and Changes Users

- read list of groups on system: `cat /etc/group`
- add new user: `sudo useradd -d /home/<userName> -s /bin/bash -g <nameOfGroup> -m <userName>`
- check the new user: `cat /etc/passwd`

---

## User Groups & User Privileges

- create user directly without specifying the group and directory: `sudo useradd -m <userName>`
- verify the user is created: `cat /etc/passwd`
- create a group and add users to it: `sudo groupadd <groupName>`
- verify the group is created: `cat /etc/group`
- delete specific group: `sudo groupdel <groupName>`
- verify the group is removed: `cat /etc/group`

---

## Network UI

- `ip link`: provides the ability to display link layer information, activate an interface, deactivate an interface, change link layer state flags, change MTU, the name of the interface, and even the hardware and Ethernet broadcast address.
- `ip addr`: lists the IP address of interfaces and system
- `man <commandName>`: to see the details of the particular command

---

## Basic Troubleshooting

- `ping -c5 8.8.8.8` : check internet usability with 5 req to `8.8.8.8`
- `traceeroute 8.8.8.8` : trace al the path
- `dig amazon.com`: get info about the website
- `netstat`: list of the active sockets and internet connections

---

## Informational Utilities

- `arp -a`: address resolution protocol
- `route`: routing table
- `netsta -rn`: routing table

---

## IP Tables

- view iptables: `sudo iptables -L`

---

## Netcat

- to create server using netcat: `sudo nc -l -p <portnumber>`
- to create client using netcat: `nc localhost <portnumber>`

---

## BASH Scripts

- Create bash script file: `nano filename.sh`
- To run the bash script: `bash filename.sh`
- Make bash script executable: `chmod 775 filename.sh`
