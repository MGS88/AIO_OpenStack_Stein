# AIO OpenStack Stein VBox

You can download the file via google drive due that the file is larger than 2GB:
https://drive.google.com/file/d/1ai7_11HcSTdLziq3X43kyn0HzgEKHuLg

OVA format Image for Virtual Box of all in one openstack stein release based on Ubuntu 18.04 LTS for VirutalBox
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


if the OpenStack http page didn't show up verify that your ip is 10.0.2.15 by executing:

$ ip a

your current ip should be under interface name enp0s3

you can edit the forward rules in VM settings > Network > Adapter 1 > Advance > Port forwarding and change 10.0.2.15 to yours
 
Alternativly shutdown all the machines in Vbox manager and take new IP by dhcp by executing:

$ sudo dhclient


# VMware Image
you can download the VMware image of OpenStack AIO Stein, by:
https://drive.google.com/open?id=11XSY6o5a5S3S5Z4JabzjH5xNVrB3M2RA

# Adjusting the network to access the HTTP page:
Edit > Virtual Network Editor > Change Settings (yes) > Select Type NAT (or add custom for .e.x:VMnet15)

edit the subnet to 192.168.17.0 255.255.255.0

Make sure the VM network adapter is NAT

# recommanded VM specs:
CPU: 4 cores

RAM: 8 GB
