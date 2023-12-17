![Screen Shot 2023-12-16 at 12 43 34 AM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/e509c7bb-8335-4f8d-874b-3bff8c295fd1)


<h1>Examining the Influence of a VPN on IP Addresses</h1>

Within this repository, I aim to illustrate the functionality of Virtual Private Networks (VPNs). These tools encrypt and redirect your internet traffic through remote servers, creating the illusion that you are browsing from diverse locations. VPNs are valuable for bolstering privacy and security, as well as circumventing geo-restrictions. In this guide, I will demonstrate the impact a VPN has on IP addresses, location, and general web browsing aiming to enhance your visual understanding of the setup process and provide a clearer insight into how the implemented VPN functions.<br />


<h2>Environments and Technologies</h2>

- Microsoft Azure (Virtual Machines)
-	Remote Desktop
-	ProtonVPN (free version)


<h2>Operating System </h2>

- Windows 10 (21H2)

# Setting Up VPN in an Azure Virtual Machine

## Step-by-Step Guide

1. The first thing you would want to do is to simply go to "whatismyipaddress.com" on your local machine. Observe the current IP Address provided to you. This is what your PC is currently using without any VPN's.

![Screen Shot 2023-12-16 at 1 51 06 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/bfc85424-4be7-4155-9784-4b710ae638e0)

![Screen Shot 2023-12-16 at 1 15 13 AM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/ffb14361-ab3a-4fca-96f7-586e9a5b0b88)

2. The next step within this walkthrough is to go create a Virtual Machine within Microsoft Azure.

- Go inside the Virtual Machine portal by searching it up in the search tab.
  
![Screen Shot 2023-12-16 at 7 43 49 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/52632ac6-a309-4eaa-adcd-ba6227546957)

   - Then choose "Azure Virtual Machine" under the "Create" tab.

![Screen Shot 2023-12-16 at 7 48 27 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/be2f6106-32be-46bc-a04f-7df430a1acfb)

   - Start by choosing another geographic location ("Region"). For my VM, I had randomly set it to "(Africa) South Africa". Also choose "Windows 10 Pro, version 22H2" for your "Image."

![Screen Shot 2023-12-16 at 7 59 41 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/37c70a45-3ddd-4031-8eab-129b1d6624bf)
     
   - Scroll down a bit and choose your size. After that, go ahead and create a Username/Password to be able to log in to your Virtual Machine. Leave everything else as is. Click the box to confirm licensing then hit "Review + create."

![Screen Shot 2023-12-16 at 8 08 55 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/0bcc5f47-4fd4-4a11-8bd9-08ce7a258cdb)

- After your VM passes validation, click create.

![Screen Shot 2023-12-16 at 8 21 59 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/193c2084-6782-4e9b-8c76-81c6a30b8acb)

4. For the third step I ended up using the "Remote Microsoft Desktop" application on my Macbook. You can download this free through the app store.

![Screen Shot 2023-12-16 at 8 28 54 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/27ff32a7-b4ee-4e21-9973-3430b246b1f6)

- Grab the public IP Address within your VM inside Azure and use that as your PC name. 

![Screen Shot 2023-12-16 at 8 32 40 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/f33fe4dc-8581-44c1-8831-081f5ab599d2)

- Once added you will simply use your log in credentials that you created while setting up your VM in the previous step.

![Screen Shot 2023-12-16 at 8 34 04 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/a6e3065f-0d7b-4090-a24a-8e6be650f177)

6. Next, go ahead and open up the website "whatismyipaddress.com" again but this time through the VM. Now observe the new IP Address and location given. You can see that the location corresponds with the region you had chosen while setting up the VM.
 
![Screen Shot 2023-12-16 at 1 53 01 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/9646861c-fc11-4105-a3eb-aba344ee1c71)

6. Sign up for the free version of ProtonVPN (https://account.protonvpn.com/signup?plan=free&language=en) on your actual computer. Then download and install the ProtonVPN client within your VM. 

7. Inside the Azure virtual machine, connect to a ProtonVPN server located in another country like Japan (or any another available countries). This establishes a VPN connection between your virtual machine and the chosen ProtonVPN server.
   
![Screen Shot 2023-12-16 at 1 57 32 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/9fd48842-d0f3-4386-87ea-4fd9eb7f1df1)

9. Now browse back on to "whatismyipaddress.com" again from within the Azure virtual machine. As the VPN is now active, observe how the new IP address and location is different. This IP address should reflect the location of the VPN server (e.g., Tokyo, Japan).
    
![Screen Shot 2023-12-16 at 1 58 15 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/4bf91c3f-658f-4d02-8473-b300cd317e90)

11. As you can see when you also access different websites like Google or Netflix you can see that in relation to the location of the VPN, many different things about these sites could be different. For example, the languages, URL, or even advertisements are all specifically geared towards that country.

12. As always, if you are following this, remember to clean up and delete the Resource Group you created for your Virtual Machine within Azure as this may eat up all of your credits or rack up a huge bill if completely forgotten. 


## Results

Hopefully this walkthrough provided a better understanding on how to get a Virtual Machine up and running, how to install a VPN, and actively using that VPN inside of your VM.  

- When accessing the website from your actual PC without a VPN, it shows your original IP address and your city location.

- After connecting to the Azure virtual machine and accessing the website, a different IP address and the location of the virtual machine (e.g., Paris) are displayed.

- Finally, by connecting to the ProtonVPN server in Japan from within the virtual machine and accessing the website again, another IP address and the location of the VPN server (e.g., Tokyo, Japan) are shown.
