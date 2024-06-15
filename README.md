**pfSense**_

What is pfSense?
pfSense is a firewall/router computer software distribution based on FreeBSD. 

Purpose? 
It is primarily used as a router and firewall software and is frequently set up as a DHCP server, DNS server, WiFi access point, and VPN server, all on the same physical device.


**Installing pfSense**
In this repo, i will demonstrate how to set up pfsense for your home lab. This whole process will be set up on a virtual box and i will be using Ubuntu as the admin system and configuring the pfsense.

Requirements : 
1. Virtual box 
2. Ubuntu installed on the virtual box. 
3.pFsense ISO image

Process: 
1. We need an ISO image for the virtual box. pfSense ISO image can be downloaded from the official page - https://www.pfsense.org/download/
2. Select appropriate architecture. 

<img width="847" alt="1" src="https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/58917b64-9749-463e-a10a-3b83d4ccc121">

3. When the download is completed, Open the virtual box and click on new.

![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/5ae60880-9a48-402a-886d-68d2448c8163)

4. Name the VM, Use the ISO image you downloaded, select type as BSD and Version as FreeBSD 64 bit.
   
5. Allocation of resources like Base memory, and hard disk, should be done based on the requirements.
6. You can set the default allocation. Click on Finish.
![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/dd82a0ed-33ca-4e8d-82b1-bd8877ae716f)

7. Click on Setting. Network configuration is important for the firewall. Select the Network and enable adapter 1 and adapter 2 Set Adapter 1 to NAT (WAN interface). Set Adapter 2 (LAN interface).
   ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/dc764e07-f3d8-4d67-a039-c96cf4d0f964)

8. start the VM and install pfsense.
9. Click on Accept.
    ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/9bccc878-4e2a-4064-9d24-a52f65ec6aac)

10. Click on Install pfSense
 ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/0f3fd1aa-78e2-4fab-832f-706a574748e9)

11. Setting up Network Config. Click Ok and continue.
    ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/23e5fa4f-3931-4551-a933-1f282c83cd57)

12. Select the Wan Interface. It is Adapter 1 which is connected to NAT so it is a WAN interface. and continue
    ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/a5f45065-a472-4b73-a457-d305653b9b14)
D
13. Similarly select LAN interface and continue.
14. Click on Install CE and continue. 
    ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/18654b62-52e7-467b-acb8-bb88160773e0)

15. For the ZFS configuration. It is better to select Stripe type. As we are only using one disk to install the software.
16. Select the disk for the installation.
    ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/7c974b70-e1c7-478e-9236-762a462a43c6)

17. Select the Current Version of pfSense CE click ok and continue.
![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/a37ba03a-c5a7-4a1d-9a60-67b85bcd21cc)

18. This process of installation will take some time.
19. Click Ok and reboot he system. 
    ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/a83c85ff-a762-48b8-9723-bb6e5afd2445)

20. After rebooting - it is important to remove the image attached. Because it reverts the installation process and asks the same question it had.So, Power off the VM and unmount the iso image and then start again. 
21. Start the VM again
22. The IP has been configured.
    ![image](https://github.com/srisowmya2000/pfsensefirewall/assets/59259117/558bec73-f08d-4adc-926b-5393a6ffa5e8)

23. Now We will go to the Ubuntu machine and and do the rest of the configuration.














   



















Reference : 

1. https://www.pfsense.org/
   
