# Home Lab Running Active Directory (Oracle VirtualBox) | Add Users w/PowerShell

## Introduction

In this guide, I’ll show you how to set up a home lab to run Active Directory using Oracle VirtualBox. We’ll go over the steps to create a Windows Server virtual machine (VM) to serve as a domain controller, install and configure Active Directory Domain Services (AD DS), and use PowerShell to add users to Active Directory. This setup will give you hands-on experience in managing an Active Directory environment and automating user management tasks.

## Diagram
![Diagram](https://github.com/spooky7777/Home-Lab-Active-Directory/raw/main/.gitbook/assets/pivd.png)

<h2>Languages Used</h2>

- <b>PowerShell</b>

<h2>Environments Used</h2>

- <b>VirtualBox</b>
- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>What is Used</h2>

- <b>AD DS - Active Directory Domain Services</b>
- <b>NAT - Network Address Translation</b>
- <b>DHCP</b>

## Download and install Oracle VirtualBox from the official website.
[Oracle Virtual Box](https://www.virtualbox.org/)

## Download the Windows 10 and Server 2019 ISO files.
[Windows 10 iso](https://www.microsoft.com/en-us/software-download/windows10ISO)
[Windows Server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019)

## Create a new virtual machine by clicking on "New" in VirtualBox. Name it "Domain Controller". Select the "Windows Server 2019" ISO file as the boot media.

![](https://i.imgur.com/Be2jxxW.png)

![](https://i.imgur.com/8MQBOSW.png)

##  Configure the virtual machine by giving it two network adapters: One to be able to conenct to the internet and the other for our private network.

![](https://i.imgur.com/qGPgwN8.png)

![](https://i.imgur.com/RcIFAEU.png)

##  Install Server 2019 on the virtual machine and assign IP addressing for the internal network (rename the networks to make it easier to distinguish).

![](https://i.imgur.com/4SVrhRu.png)

![](https://i.imgur.com/oVl8drg.png)
##  Name the server and install Active Directory to create the domain.
![](https://i.imgur.com/G15lqw7.png)

![](https://i.imgur.com/tHPgIGI.png)

##  Configure routing so that clients on the private network can access the internet through the domain controller.

![](https://i.imgur.com/J1o5Yzm.png)

![](https://i.imgur.com/W2Cpyam.png)

![](https://i.imgur.com/ohM8iqP.png)

##  Set up DHCP on the domain controller.
![](https://i.imgur.com/0knegJi.png)

![](https://i.imgur.com/656SaUl.png)

![](https://i.imgur.com/KwsBzCP.png)


##  Run the PowerShell script to create 1000 users in Active Directory.

[Power Shell script for creating users](https://github.com/joshmadakor1/AD_PS)

![](https://i.imgur.com/8gOaTJI.png)

##  Create a new virtual machine named "Client1" and use the Windows 10 ISO file.

![](https://i.imgur.com/zIazcw9.png)

![](https://i.imgur.com/akbopML.png)

![](https://i.imgur.com/uqv8Z2x.png)


##  Connect the client machine to the private network and join it to the domain.

![](https://i.imgur.com/H89DgA5.png)

![](https://i.imgur.com/ussotKO.png)

##  Log into the client machine with a domain account.

![](https://i.imgur.com/MurEpyW.png)

![](https://i.imgur.com/KQEGUzM.png)
