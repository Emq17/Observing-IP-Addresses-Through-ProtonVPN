![Screen Shot 2023-12-16 at 12 43 34 AM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/e509c7bb-8335-4f8d-874b-3bff8c295fd1)


<h1>Examining the Influence of a VPN on IP Addresses</h1>
For this quick little project, I will simply help demonstrate the influence of what a virtual private network (VPN) has on IP addresses, location, and overall web browsing. This walkthrough below will help you understand visually of what I did to set things up and hopefully give you a better glimpse of what happens once the VPN is implemented.<br />


<h2>Environments and Technologies</h2>

- Microsoft Azure (Virtual Machines)
-	Remote Desktop
-	ProtonVPN (free version)


<h2>Operating System </h2>

- Windows 10 (21H2)

# Setting Up VPN in an Azure Virtual Machine

## Step-by-Step Guide

1. The first thing you would want to do is to simply go to "whatismyipaddress.com" on your local machine. Observe the current IP Address provided to you. This is what your PC is currently using without any VPN's.

![Screen Shot 2023-12-16 at 1 15 13 AM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/ffb14361-ab3a-4fca-96f7-586e9a5b0b88)

2. The next step within this walkthrough is to go create a Virtual Machine within Microsoft Azure. Within your portal set the "Region" to "US West 3" and also choose "Windows 10 Pro, version 22H2" for your "Image." Scroll down a bit and choose your size. After that, go ahead and create a Username/Password to be able to log in to your Virtual Machine. Leave everything else as is and click "Review + create."

3. For the third step I ended up using the "Remote Microsoft Desktop" application on my Macbook. You can download this free through the app store. Grab the public IP Address within your VM inside Azure and use that as your PC name. Once added you will simply use your log in credentials that you created while setting up your VM in the previous step.

4. Next, go ahead and open up the website "whatismyipaddress.com" again but this time through the VM. Now observe the new IP Address and location given. You can see that the location corresponds with the region you had chosen while setting up the VM. 

6. Sign up for the free version of ProtonVPN on your PC. Download and install the ProtonVPN client.

7. Inside the Azure virtual machine, connect to a ProtonVPN server located in Japan (or another available country). This establishes a VPN connection between the virtual machine and the chosen ProtonVPN server.

8. Access the website "whatismyipaddress.com" again from within the Azure virtual machine, with the VPN active. Take note of the new IP address and location displayed. This IP address should reflect the location of the VPN server (e.g., Tokyo, Japan).

9. As you can see when you access different websites like Google or Netflix you can see that the marketing is specifically geared towards that country. 


## Results

Hopefully this walkthrough provided a better understanding on how to get a Virtual Machine up and running, how to install a VPN, and actively using that VPN inside of your VM.  

- When accessing the website from your actual PC without a VPN, it shows your original IP address and your city location.

- After connecting to the Azure virtual machine and accessing the website, a different IP address and the location of the virtual machine (e.g., Paris) are displayed.

- Finally, by connecting to the ProtonVPN server in Japan from within the virtual machine and accessing the website again, another IP address and the location of the VPN server (e.g., Tokyo, Japan) are shown.

This exercise demonstrates how VPNs work by encrypting and routing your internet traffic through remote servers, making it appear as if you are browsing from different locations. VPNs can enhance privacy, and security, and allow you to bypass geo-restrictions.
