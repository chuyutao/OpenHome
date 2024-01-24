# OpenHome

Here are the steps I followed:

-> Bott Storae Disk

1.Connect Raspberry Pi to software and write into the storage disk.
2.Re-Connect the disk after finish writing. You will see it as "boot" or "bootfs". cd into it.

cd boot

3.Create an empty SSH file

sudo touch ssh

4.Eject the disk and connect it to the Raspberry Pi. Power Raspberry Pi. 
(wait a minute for the Raspberry Pi to boot! you will notice the green light goes off as it finishes processing)

-> Raspberry Pi set up 

1.Find the portal for your Raspberry. Enter "ping raspberry.local"

(base) chuyutao@Chuyus-Air ~ % ping raspberry.local
PING raspberry.local (192.168.1.86): 56 data bytes
64 bytes from 192.168.1.86: icmp_seq=0 ttl=64 time=178.979 ms

2.Connect to Raspberry through ssh

(base) chuyutao@Chuyus-Air ~ % ssh chuyutao@192.168.1.86

3.Generate SSH Key 
chuyutao@tracy:~ $ ssh-keygen -t ed25519 -C "Replace with youremail@OpenHome"

4.Add SSH identity
chuyutao@tracy:~ $ ssh-add ~/.ssh/id_ed25519
Identity added: /home/chuyutao/.ssh/id_ed25519 (xxx@OpenHome)

5.Show SSH Key. Copy & Paste the whole second line
chuyutao@tracy:~ $ cat ~/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFabnqFeEtq0inw00j9S0Q278491l8pxL2ZV25aiw xxxx@OpenHome

6.Now you are able to clone the Whisper Repository 
chuyutao@tracy:~ $ git clone git@github.com:ggerganov/whisper.cpp.git





