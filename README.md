<p align="center">
   <img width="170" height="321" alt="image" src="https://github.com/user-attachments/assets/4596d79b-f5a4-4042-b442-42c3ac4f9f4d" />

</p>

<h1 align="center"> Hosting a Static Website in Virtual Machine Azure
</h1>

<p align="center">

##  Technologies Used

![Microsoft Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)

![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![DNS](https://img.shields.io/badge/DNS-Networking-blue?style=for-the-badge)

![SSH](https://img.shields.io/badge/SSH-Remote_Access-black?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Network Security Group](https://img.shields.io/badge/Azure_NSG-Security-2F80ED?style=for-the-badge)

![Draw.io](https://img.shields.io/badge/Draw.io-Architecture_Diagram-F08705?style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-CLI-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![BobaxTerm](https://img.shields.io/badge/BobaxTerm-Go%20Terminal-blue?logo=go&logoColor=white)



![CIDR](https://img.shields.io/badge/CIDR-Networking-green?style=for-the-badge)
![VNet](https://img.shields.io/badge/Azure_VNet-Network-blue?style=for-the-badge)





</p>


## 📌Project Overview
This project demonstrates how to host a static website using a Virtual Machine (VM) in Microsoft Azure. An Azure VM is created and configured with a Nginx web server to serve static HTML, CSS, and JavaScript files. 

## Table of Contents
- [Created a Virtual Machine ](#1-created-a-virtual-machine)
- [Connecting to Sever](#2-connecting-to-the-virtual-machine-via-linux-cli-mobaxterm)
- [Configuring, Patching and Updating Server](#3-configuring-patching-and-updating-server)
- [Installing nginx](#4-installing-nginx-on-the-server)
- [Uploading website content to the server](#5-uploading-website-content-to-the-server)
- [Upadating A DNS Record for Map Sever IP to a record](#6-updating-the-dns-record-to-map-the-ip-address-of-the-server-to-a-record-i-will-be-using-namecheap-for-this)
- [Verifcation](d#verification)

 ### STEPS


## 1.) Created a Virtual machine

(step 1)

_**Baisc VM Setup**_

<img width="1358" height="636" alt="2-Created a Virtual machine" src="https://github.com/user-attachments/assets/c86658da-a176-4ca5-8000-ab477dfae3a5" />
<br/>


<p></p>

_Inbound port rule setup: I am allowing port 80 for http access and ssh port 22 for remote access for the VM network_

_Also i will be using  username and password instead of a key to ssh_

<img width="1277" height="634" alt="3Created" src="https://github.com/user-attachments/assets/0f30006e-4c34-4422-b40a-fdcd6edc02c7" />

<p> </p>
<p> </p>
<p> </p>

(step 2)

***Disk and storage Setup***

<img width="1145" height="663" alt="Disk setup" src="https://github.com/user-attachments/assets/31bad786-ac8a-46e6-abfc-9df653be3419" />

<p> </p>


(step 3)

**VM Netwoking Setup**

<img width="1152" height="642" alt="Network-Setup 1" src="https://github.com/user-attachments/assets/cabbac14-be59-4458-88b7-9ca7278ea0e0" />

<p> </p>

(step 4)

**Management Setup**
_left at defualt_

<p> </p>

(step 5)

**Monitoring Setup**
_left at defualt_

**Done** ✔


https://github.com/user-attachments/assets/93af4527-0ec6-457f-a565-d0809088cdad



<p></p>

## 2.) Connecting to the Virtual Machine VIA Linux CLI (MobaXterm)

(step 1)

<img width="1330" height="676" alt="connected to server via mobaxterm" src="https://github.com/user-attachments/assets/f369c687-3575-418d-b053-1c5f06157e44" />

## 3.) Configuring, Patching and Updating Server

 cmds

Update  and patch 

_sudo apt update_

_apt list --upgradeable_

_sudo apt upgrade -y_

**Done** ✔

<img width="1339" height="671" alt="patching server 3" src="https://github.com/user-attachments/assets/ae534339-2a7b-4ded-9d93-e1e33ab937c5" />


## 4.) Installing Nginx on the server

Note : Nginx was installed to serve the website and handle incoming web traffic on the server.

cmds 

_install ( sudo apt install nginx -y)_

_verify if nginx is running (sudo systemctl status nginx)_

<img width="1336" height="716" alt="Installed Nginx" src="https://github.com/user-attachments/assets/7726781d-b825-4a7c-85eb-20d839fd6c9f" />

**Done** ✔

<img width="1340" height="719" alt="Installed Nginx 2" src="https://github.com/user-attachments/assets/efb49368-eef9-4dbd-8080-2608b889e8ff" />



## 5.) Uploading website content to the server

cmds 

sudo cp -r Website-files/* /var/www/html/

<img width="1353" height="698" alt="uploading website files 3" src="https://github.com/user-attachments/assets/310549a9-dac0-4e15-851c-290f874cf987" />

Note: The Default Nginx html files needs to be removed

cmds 

sudo rm index.nginx-debian.html

<img width="1325" height="696" alt="removing defualt nginx html file 2" src="https://github.com/user-attachments/assets/3d3209f9-bc1a-4a06-96f6-a2483e824833" />



**Testing** ✔



https://github.com/user-attachments/assets/beec4e8c-afa4-415b-8417-0817f3980d2a



## 6.) Updating the DNS record to map the IP address of the server to a Record. (i will be using Namecheap for this)


http://rivetrecords.online

<img width="1337" height="686" alt="Mapping Address to an A record" src="https://github.com/user-attachments/assets/14b13aad-a189-4277-ac6b-11db9d1e2b05" />


 ## ✔Verification 

**Testing** ✔  



https://github.com/user-attachments/assets/6accf5f4-6a3a-4642-9793-8dd6dcadfcd2




 Conclusion 
 The website has been succesully deployed and tested. This will be available for few days. i will be deleting the server to avoid extra charges.


