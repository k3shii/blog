# Kioptrix

tcm-sec.com/kioptrix

login: john

password: TwoCows2

## Scanning with Nmap

1. Looking for target IP

* discover network range
* Kali’s IP: 192.168.153.131
* Kioptrix’s IP: 192.168.153.134 (Target IP)

1. Nmap Scanning

```python
┌──(root㉿kali)-[/home/k3shi]
└─# SYN SYNACK SYN namp -sS
```

💡 Scanning will detectable if not using -sS (Stealth Scanning)

* `SYN SYNACK SYN`: Three way handshake
* `nmap -sS`: nmap scanning

```python
┌──(root㉿kali)-[/home/k3shi]
└─# nmap -T4 -p- -A 192.168.153.134
```

* `-T4`: speed 1-5 (recommended 4)
* `-p-`: scan all port
  * `without -p-`: scan top 1000 port (common port)
  * `-p {port number}`: scan specific port
* `-A`: all / everything (OS detection, version, etc.)

```python
┌──(root㉿kali)-[/home/k3shi]
└─# nmap -sU -T4 -p 192.168.153.134
```

* \-sU: UDP scan (typically top 1000 port)
* UDP take forever to scan

## Enumerating HTTP/HTTPS

## Scanning with Nikto

💡 Tips: Save information in text file

## Scanning using Dirbuster

```python
┌──(root㉿kali)-[/home/k3shi]
└─# dirbuster
Mar 14, 2024 5:46:39 PM java.util.prefs.FileSystemPreferences$1 run
INFO: Created user preferences directory.
Starting OWASP DirBuster 1.0-RC1
```

browse → base folder → usr → share → wordlist → dirbuster → directory-list-2.3-small.txt (recommended)

200 - works well

300 - redirect

400 - some sort of error like 404

500 - server error
