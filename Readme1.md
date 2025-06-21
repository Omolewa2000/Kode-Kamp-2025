# Linux Fundamentals Project with Vagrant

**Vagrant Initialization**

![vagrant initialization](image.png)

Vagrant is initialised  - The vagrant init command is used to initialize a new Vagrant project. It sets up a folder with a basic Vagrantfile that defines how the virtual machine (VM) should be created and configured.

**Spining a Vagrant Server**

![vagrant up](image-1.png)

![vagrant up](image-3.png)

Spining the VM

The command vagrant up is used to start and provision the Vagrant-managed virtual machine.

**SSH into the server.**

![vagrant ssh](image-4.png)

Connecting to the VM with vagrant ssh

The command vagrant ssh allows one to securely log into the virtual machine that Vagrant is managing — without needing to know its IP, username, or password.

## Exploring the Linux File System

![mkdir ](image-5.png)

mkdir -p /home/vagrant/projects/devops

Creates the directory /home/vagrant/projects/devops

Uses -p to create any missing parent directories:

If /home/vagrant/projects doesn’t exist, it creates it too

![chown and chmod](image-6.png)

**Manage File Permissions and Ownership**

chown command was used to change the owner from root to vagrant

I created a file named sample-file.txt and it has the permission -rw-rw-r--

-rw-rw-r--

│ │  │  │

│ │  │  └── others: read-only

│ │  └──── group: read and write

│ └─────── owner: read and write

└───────── it's a regular file (-)


(-) means it is a Regular file 

Owner: rw- → can read and write

Group: rw- → can read and write

Others: r-- → can only read

This corresponds to chmod 664

The permission was changed to -rwxr-xr-x using the command chmod 755 sample-file.txt

Owner: rwx → can read, write, and execute

Group: r-x → can read and execute

Others: r-x → can read and execute

The key difference is that I added execute permissions and removed group write.

##  Test Remote Connectivity

![Ping Test](image-7.png)

The ping command is a network diagnostic tool used to test connectivity between your computer and another device (host) on a network — like a website, server, or another machine.

**What It Does**
Sends ICMP Echo Request packets to the target

Waits for Echo Reply responses

Measures the time it takes for the round-trip

What the Output Shows
| Line/Field                | What It Means                                     |
|--------------------------|---------------------------------------------------|
| `PING google.com`        | Target hostname and its resolved IP address       |
| `64 bytes from ...`      | Successful reply from the remote host             |
| `icmp_seq=0`             | Sequence number of the ICMP packet                |
| `ttl=115`                | Time To Live – how many hops the packet can take  |
| `time=24.3 ms`           | Round-trip time between your machine and the host |
| `packet loss`            | Percentage of lost packets                        |
| `rtt min/avg/max/mdev`   | Statistics for round-trip time (min, average, max, deviation) |


**Install and Configure a Package**
![apt install package](image-8.png)

Nginx version
![Nginx Version](image-1.png)