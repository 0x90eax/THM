nmap -A anon
```
Starting Nmap 7.93 ( https://nmap.org ) at 2023-08-03 19:51 PDT
Stats: 0:00:03 elapsed; 0 hosts completed (1 up), 1 undergoing Connect Scan
Connect Scan Timing: About 11.45% done; ETC: 19:51 (0:00:23 remaining)
Nmap scan report for anon (10.10.217.157)
Host is up (0.28s latency).
Not shown: 998 closed tcp ports (conn-refused)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 60b6ad4c3ef9d2ec8bcd3b45a5ac5f83 (RSA)
|   256 6f9abedffc95a2318fdbe5a2da8a0c3c (ECDSA)
|_  256 e6985249cff2b865d7411c832e942488 (ED25519)
80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Proving Grounds
| http-robots.txt: 1 disallowed entry 
|_/zYdHuAKjP  #access denied. Clearly a token of some sorts? phpsessionid?
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

-sU
PORT   STATE         SERVICE
68/udp open|filtered dhcpc
```


