# juniper-ztp
Juniper Zero Touch Provisioning

CentOS7

#Disable selinux because you're a network guy and you dont understand Linux - /etc/selinux/config

systemctl disable firewalld

reboot

yum install epel-release -y

yum install dhcp -y

yum install vstfpd -y

yum update -y

#Configure dhcpd for the interface you wish to use - example config in this repo

#Configure vsftpd to be insecure because you do networking - example config in this repo

chmod -R 777 /var/ftp/pub

systemctl enable dhcpd

systemctl enable vsftpd

systemctl start dhcpd

systemctl start vsftpd

#Place files in /var/ftp/pub
