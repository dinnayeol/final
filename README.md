#1 task
cisco@labvm:~$ sudo su
[sudo] password for cisco: 
root@labvm:/home/cisco# useradd student
root@labvm:/home/cisco# passwd student
New password: 
Retype new password: 
passwd: password updated successfully
root@labvm:/home/cisco# login
labvm login: student
Password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 5.4.0-67-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

85 updates can be applied immediately.
65 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

*** System restart required ***

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.


The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

No directory, logging in with HOME=/
$ whoami
student
$ 

#2 task
cisco@labvm:~$ ipconfig

Command 'ipconfig' not found, did you mean:

  command 'iwconfig' from deb wireless-tools (30~pre9-13ubuntu1)
  command 'iconfig' from deb ipmiutil (3.1.5-1)
  command 'ifconfig' from deb net-tools (1.60+git20180626.aebd88e-1ubuntu1)

Try: sudo apt install <deb name>

cisco@labvm:~$ ifconfig
enp0s3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::a00:27ff:fec7:750b  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:c7:75:0b  txqueuelen 1000  (Ethernet)
        RX packets 753367  bytes 1047645637 (1.0 GB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 198083  bytes 12591303 (12.5 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 2011  bytes 212891 (212.8 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2011  bytes 212891 (212.8 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

#3 task
cisco@labvm:~$ sudo apt update
[sudo] password for cisco: 
Hit:1 http://security.ubuntu.com/ubuntu focal-security InRelease
Hit:2 http://archive.ubuntu.com/ubuntu focal InRelease
Hit:3 http://archive.ubuntu.com/ubuntu focal-updates InRelease
Hit:4 http://archive.ubuntu.com/ubuntu focal-backports InRelease
Reading package lists... Done
Building dependency tree       
Reading state information... Done
82 packages can be upgraded. Run 'apt list --upgradable' to see them.
cisco@labvm:~$ sudo apt install build-essential
Reading package lists... Done
Building dependency tree       
Reading state information... Done
build-essential is already the newest version (12.8ubuntu1.1).
The following package was automatically installed and is no longer required:
  libllvm11
Use 'sudo apt autoremove' to remove it.
0 upgraded, 0 newly installed, 0 to remove and 82 not upgraded.
cisco@labvm:~$ gcc --version
gcc (Ubuntu 9.4.0-1ubuntu1~20.04.1) 9.4.0
Copyright (C) 2019 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

#include <studio.h>
int main()
{
printf("Hello, World!");
return 0;
}

