# Linux Operating System

## Basic Command

`pwd` : present working directory / print working directory

`cd` : change directory

* `cd ..` : change director backward

`ls` - list folders and files

`mkdir`: create directory

`rmdir`: remove empty directory

`cp`: copy file

`rm`: remove files

* rm -rf
* rm -

`mv`: mv directory / files

`locate`: locate files

`updatedb`

`passwd`: change user password

`man`: use `man {command}` to see manual page

## Users and Privileges

`chmod`: change file permission `chmod +rwx` / `chmod 777` \[read (4), write (2), execute (1)]

`/etc/passwd`: show information of user

`/etc/shadow`: show user hashed password

`su`

`sudo`

## Common Network Commands

`ifconfig`: network interface

`iwconfig`: wireless adapter version

`ping`: `ping -c 1`

* `ping {ip} -c {count reply}` - set count reply
* `ping {ip} -c {count reply} > test.txt` - save ping info into `.txt` file

`arp`

`netstat`: display all connection and listening port

`route`: display all routing table

## Viewing, Creating, and Editing Files

`echo`:

`cat`: show file content

`>`: replacing - `echo “text” > file.txt`

`>>`: appending - `echo “text text” >> file.txt` (append to second line)

`touch`: create new file

`nano`: terminal text editor (edit / create file content)

`gedit`: graphical text editor (edit / create file content)

## Services

`services`: start / stop services

* `services {services} start`
* `services {services} stop`
* `python -m http.server {unused port}`

`systemctl`: enable / disable services

* `systemctl enable {services}` - services boot automatically when open
* `systemctl disable {services}`- services is off when open

## Installing / Updating Tools

Installing updates with `apt-get`

* apt-get update && apt-get upgrade

Installing tools with `apt-get`

Using `git`

* `apt-get install git -y`
* `git clone {git-url}`
* `.config/`

## Basic Bash Scripting

`grep`: narrow down result

* `cat ip.txt | grep “64 bytes”`

`cut`

* `cat ip.txt | grep “64 bytes” | cut -d “ ” -f 4` (`-d`: delimiter. `-f`: field)

`tr`

* `cat ip.txt | grep “64 bytes” | cut -d “ ” -f 4 | tr -d ":"`
* script writing with `for loops`

```bash
#!/bin/bash

for ip in `seq 1 254` ; do 
ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
done

//second method
for ip in `seq 1 254` ; do 
ping -c 1 192.168.153.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
done
```

* run `.sh` file
* prompt echo if user forgot to add IP header behind the sh file

```bash
#!/bin/bash
if [ "$1" == "" ]
then
echo "You forgot an IP address!"
echo "Syntax: ./ipsweep.sh 192.168.153"

else
for ip in `seq 1 254` ; do 
ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
done
fi
```

* save result into `iplist.txt`

bash scripting using nmap

scan the ip address that listed inside the iplist.txt

```bash
┌──(root㉿kali)-[/home/k3shi]
└─# for ip in $(cat iplist.txt); do nmap -sS -p 80 -T4 $ip & done 

[2] 29438
[3] 29439
[4] 29440
                                                                                                                       
┌──(root㉿kali)-[/home/k3shi]
└─# Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-02-16 13:16 +08
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-02-16 13:16 +08
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-02-16 13:16 +08
Nmap scan report for 192.168.153.131
Host is up (0.0012s latency).

PORT   STATE SERVICE
80/tcp open  http

Nmap done: 1 IP address (1 host up) scanned in 0.31 seconds

[4]  + done       nmap -sS -p 80 -T4 $ip
┌──(root㉿kali)-[/home/k3shi]
└─# Nmap scan report for 192.168.153.2
Host is up (0.00061s latency).

PORT   STATE  SERVICE
80/tcp closed http
MAC Address: 00:50:56:EC:B0:CD (VMware)

Nmap done: 1 IP address (1 host up) scanned in 0.48 seconds

[2]  - done       nmap -sS -p 80 -T4 $ip
┌──(root㉿kali)-[/home/k3shi]
└─# Nmap scan report for 192.168.153.1
Host is up (0.0014s latency).

PORT   STATE    SERVICE
80/tcp filtered http
MAC Address: 00:50:56:C0:00:08 (VMware)

Nmap done: 1 IP address (1 host up) scanned in 0.67 seconds

[3]  + done       nmap -sS -p 80 -T4 $ip
```
