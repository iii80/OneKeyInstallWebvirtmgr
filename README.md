# OneKeyInstallWebvirtmgr
A script to Install webvirtmgr on Centos mini
This is a script to help you autoinstall webvirtmgr on centos7(mini)



There are two options when you run it.



1) install webvritmgr

install webvirtmgr to centos7 mini. config everything. I config SSH for connecting to kvm server. 

if the scripte ask u questions, just enter (yes) or just press key return.



2) Config Kvm Server 

It will auto login to KVM server and Config KVM server ,then webvirtmgr can use ssh to connect the kvm server.



The first, the script run . it will ask u about create a new account. 

u need give the kvm server ip,and the new username and password. webvirtmgr will use it for manage the kvm server.



then The script will login the kvm server .  and ask u root password.

just enter the password of root and finish all then reboot system.



if u use VNC to connect the kvm host, the script opened 8 port for those kvm host.



u Can edit the kvm host's xml config in webvirtmgr. Config the VNC port to those (5900-5907). 



firewall-cmd --add-port=5900/tcp --permanent

    firewall-cmd --add-port=5901/tcp --permanent

    firewall-cmd --add-port=5902/tcp --permanent

    firewall-cmd --add-port=5903/tcp --permanent

    firewall-cmd --add-port=5904/tcp --permanent

    firewall-cmd --add-port=5905/tcp --permanent

    firewall-cmd --add-port=5906/tcp --permanent

    firewall-cmd --add-port=5907/tcp --permanent

    

You can use this command on centos7mini to download it.



git clone https://github.com/GarySunFromChina/OneKeyInstallWebvirtmgr.git



Then run



chmod +x ./OneKeyInstallWebvirtmgr/*

./OneKeyInstallWebvirtmgr/setup.sh



If You have any questions send me email. My email is sunglen@qq.com.

