File to understand on how to install Jenkins

-- First need to ssh into the server

-- Install the necessary JAVA library with following commands:

```
sudo apt-get update
sudo apt install default-jdk -y
sudo apt install default-jre -y
```

-- Install Jenkins on the server:

```
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt update
sudo apt install jenkins -y
## start the service
sudo systemctl start jenkins
```

then open the server with the following ip:
http://your_server_ip_or_domain:8080

If you can't open, please allow firewall by the following commands:

```
sudo ufw allow 8080
sudo ufw allow OpenSSH
sudo ufw enable
sudo ufw status
```

ref: https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-20-04
