# Troubleshoot/tasks done in Windows
## Network
### Checking Network Settings
- Depending on how network is set, there are possible management needed for the system. 
- For example, servers are using static IP and most of other users are using IP that's assigned by DHCP. 
![alt text](ncpa-1.png)
- To check, go to 'run' on Windows, then type 'ncpa.cpl'
![alt text](Ethernet-1.png)
- It will appear network setting page, usually these tasks are performed by using LAN(Ethernet).
- So click Ethernet you are connected to. 
![alt text](Detail-1.png)
- On here on top there is IPv4 connection - Interent which it's connected to internet.
- Speed says 1 Gbps which is quite fast, typically from experience it's 500mb. 
- Then if you click detail, it will show information on right. 
- IPv4 Address, subnetmask, IPv4 Gateway, DHCP, DNS. 
- Gateway is where your network gets out to access internet or different network band. 
- If it's middle to large size industry, they use DHCP server on different address, since it's small they didn't.
- DHCP asign IP address automatically for each devices unless it's static for specific port. 
- DNS is what changes domain name to IP address, when user search google.com, DNS returns 8.8.8.8 then user access to google.com.
- Since it's on DHCP, IP addresses are coming automatically. 
![alt text](Properties-1.png)
- Click properties to change network settings, then click IPv4
![alt text](Automatically-1.png)
- If both are checked on these, then it receive network automatically (DHCP) and receive DNS automatically.
- Checking other option will allow entering information manually. 

## BIOS Update 
- Typically BIOS update is provided by vendor of PC such as ASUS, Dell, Lenovo, etc. 
- Accessing their official website usually offers update file. 
![alt text](<HP Sample-1.png>)
- For example, HP request either model name or serial number to allow accessing driver.
- It helps to match exact version of driver needs for the device.
- Also, it asks type of OS such as Win 11 24H2, 25H2. Make sure to match exact one. 
![alt text](Lenovo-1.png)
- Many other cases offer way simpler option. For example, Lenovo has it on MS Store. 
- After downloading, it shows all of the options to install drivers and BIOS update. 

## Imaging 
- There were various imaging that I have done depending on Company.
- Typically, company provides iso image file to install on new PC.
- In that case, they have programs generally use within company itself. 
- ![alt text](<Boot setting-1.jpg>)
- There are many buttons to go boot menu depending on vendor.
- It can be F2, F9, F10 or anything, so search on google for it. 
- On BIOS menu there will be boot setup, Technitians can mangage settings. 
![alt text](<Boot Page-1.jpg>)
- This is boot menu page of LG device. 
- There is nothing to boot now because nothing is connected. 
- If USB is attached it will show boot as 'USB drive name' Drive. 
- But, it needs to be set up before booting, else it won't be detected. 
- One of most common option is booting as IPv4 network, allows when connecting to LAN.
- If company set to install image through IPv4, it will install automatically once select PXE(LAN) boot. 

## Intune after imaging
- Some company does it different way. Such as Azure AD(Entra).
- To join it, usually they image just clean Windows image(No company programs installed).
- Then, when login with user account, intune deploys company programs on PC so it does not need to install one by one. 

# Build USB for Imaging 
- https://rufus.ie/en/ is a website I install a program to set up a USB for imaging. 
- Install program from the website and follow instruction. 
![alt text](Rufus-1.png)
- Select device(USB), select image then click confirm. 
- If there isn't specific reason, default settings will work. 
- Then it will load and build your USB ready for boot but once setting it up, all of the files within USB will be gone. 

## Joining Domain
- Then required to join domain and most helpdesk does it before giving PC to user.
![alt text](Domain-1.png)
- Go to Windows Settings -> System Properties -> Domain/Workspace
- Click change then it will display domain change window. 
![alt text](Domain2-1.png)
- Set computer name, a lot of company require to use specific style. 
- Type the domain and confirm, it will display a window to enter admin account and password, once it's entered in then PC will join domain. 

## Password Change
- On user side, there is easy way to change it. 
- Ctrl + Alt + Delete will display a page to click options, click change password will lead to the page. 

## Remote Support
- There are plenty of remote support tool in the world to access someone's PC. 
- However, there are cases that people prefer not to use them due to cost. 
- If it's Windows, there is "Quick Assist" that helps to access easily. 
![alt text](<Quick Assist-1.png>)
- Click the bottom Support Other user
![alt text](Code-1.png)
- Then it will display the code user needs to enter, give it to user. 
![alt text](<Quick User-1.png>)
- Type code on user side then it will start remote access. 

# MAC
## General Tasks on MAC
### Cleaning program for MAC
- Some of users ask managing their memory for MAC and typically uses cleaning program. 
- It is usually only cleans cache files, because MAC has their own memory management. 
- Also, it's heavily SSD based, so it shouldn't affect anything on device's performance. 
- However, cleaning program can delete down necessary cache which means it can be harmful than useful. 

