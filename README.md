# AIO OpenStack Stein

You can download the file via google drive due that the file is larger than 2GB:


OVA format Image of all in one openstack stein release based on Ubuntu 18.04 LTS for VirutalBox
to run it, choose the image under file > import appliance in Vbox manager

# Host OS username/password: 
openstack/openstack 

note: root password also "openstack"
# OpenStack username/password: 
admin/nomoresecret

this images toke the IP by Virtual Box's dhcp, which was 10.0.2.15, 
so I added a rule in VBox to access 10.0.2.15:80 by 127.0.0.1:88
# OpenStack http dashboard (Horizon):
https://127.0.0.1:88

Also added another rule to access ssh, to access ssh:
127.0.0.1:222
and username/password is openstack/openstack

To take new IP by dhcp please execute:

$ sudo dhclient

then execute:

$ ip a

to show your current ip under interface name enp0s3

# recommanded VM specs:
CPU: 4 cores

RAM: 8 GB
