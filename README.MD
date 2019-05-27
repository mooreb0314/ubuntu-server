# Server Setup
1. Enable the network interface that the ethernet cord is plugged into
Get the name of the network interface (ex: eno1)
`ifconfig -a`

Add that network interface into the interfaces file
`sudo vi /etc/network/interfaces`

Example section
```
auto eno1
iface eno1 inet dhcp
```

Enable the network interface just created

`sudo ifup eno1`

2. Install ssh
```
sudo apt update
sudo apt install openssh-server -y
```
Check to make sure ssh server is running
```
sudo systemctl status ssh
```

3. SSH into box and add public key.
4. Disable password auth??

5. Install Docker
```
sudo apt install docker.io -y
```
6. Add user permissions to run docker commands
```
sudo groupadd docker
sudo gpasswd -a $USER docker
```
Will need to restart session to update user group permissions

