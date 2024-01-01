<p align="center">
<img src="https://i.imgur.com/IOuDUwp.png" alt="Logo"/>
</p>

<h1 align="center">Examining the Influence of a VPN on IP Addresses</h1>

Within this walkthrough, I aim to illustrate the functionality of Virtual Private Networks (VPNs). These tools encrypt and redirect your internet traffic through remote servers, creating the illusion that you are browsing from diverse locations. VPNs are valuable for bolstering privacy and security, as well as circumventing geo-restrictions. In this guide, I will demonstrate the impact a VPN has on IP addresses, location, and general web browsing aiming to enhance your visual understanding of the setup process and provide a clearer insight into how the implemented VPN functions.<br />


<h2>Environments and Technologies</h2>

- Microsoft Azure (Virtual Machines)
- Microsoft Remote Desktop (Mac)
-	ProtonVPN (Free Version)


<h2>Operating System </h2>

- Windows 10 (22H2)

# Setting Up VPN in an Azure Virtual Machine

## Step-by-Step Guide

The first thing you would want to do is to simply go to "whatismyipaddress.com" on your local machine. Observe the current IP Address provided to you. This is what your PC is currently using without any VPN's. Below is a diagram of that first step.

![Screen Shot 2023-12-16 at 1 51 06 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/bfc85424-4be7-4155-9784-4b710ae638e0)

![Screen Shot 2023-12-16 at 1 15 13 AM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/ffb14361-ab3a-4fca-96f7-586e9a5b0b88)

The next step within this walkthrough is to go create a Virtual Machine within Microsoft Azure.

- Go inside the Virtual Machine portal by searching it up in the search tab.
  
![Screen Shot 2023-12-16 at 7 43 49 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/52632ac6-a309-4eaa-adcd-ba6227546957)

   - Then choose "Azure Virtual Machine" under the "Create" tab.

![Screen Shot 2023-12-16 at 7 48 27 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/be2f6106-32be-46bc-a04f-7df430a1acfb)

   - Start by creating a name for your VM and choosing another geographic location ("Region"). I had randomly set mine to "(Africa) South Africa".
   - Also choose the operating system "Windows 10 Pro, version 22H2" for your "Image."

![Screen Shot 2023-12-16 at 7 59 41 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/37c70a45-3ddd-4031-8eab-129b1d6624bf)
     
   - Scroll down a bit and choose your preferred size.
   - After that, go ahead and create a Username/Password to be able to log in to your Virtual Machine. Leave everything else as is.
   - Click the box to confirm licensing then hit "Review + create."

![Screen Shot 2023-12-16 at 8 08 55 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/0bcc5f47-4fd4-4a11-8bd9-08ce7a258cdb)

- After your VM passes validation, click create.

![Screen Shot 2023-12-16 at 8 21 59 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/193c2084-6782-4e9b-8c76-81c6a30b8acb)

For this step I ended up using the "Microsoft Remote Desktop" application on my Macbook. You can download this free through the app store.

![Screen Shot 2023-12-16 at 8 28 54 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/27ff32a7-b4ee-4e21-9973-3430b246b1f6)

- Grab the public IP Address within your VM inside Azure and use that as your PC name. 

![Screen Shot 2023-12-16 at 8 32 40 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/f33fe4dc-8581-44c1-8831-081f5ab599d2)

- Once added you will simply use your log in credentials that you created while setting up your VM.

![Screen Shot 2023-12-16 at 8 34 04 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/a6e3065f-0d7b-4090-a24a-8e6be650f177)

You should be logged into the Windows platform now. Next, use Microsoft Edge to enter the website "whatismyipaddress.com" again. Observe the new IP Address and location given to you. The location should now correspond with the region you had selected while setting up the VM in Azure.
 
![Screen Shot 2023-12-16 at 1 53 01 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/9646861c-fc11-4105-a3eb-aba344ee1c71)
![Screen Shot 2023-12-19 at 12 51 15 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/41ac0fd3-3a24-4c8a-bcdc-311526b0c2d1)

Sign up for the free version of ProtonVPN (https://account.protonvpn.com/signup?plan=free&language=en). Then download and install the ProtonVPN client within your VM.

![Screen Shot 2023-12-19 at 1 00 00 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/a73c089f-8a2c-4cc1-b1a9-731c83608c2d)


After installation, log in, connect to a ProtonVPN server located in another country like Japan (or any another available countries).

-  This establishes a VPN connection between your virtual machine and the chosen ProtonVPN server.
-  Upon the time you are completing this, you may see that ProtonVPN now charges members to upgrade to "Plus" which gives them access to other countries. Below I chose "Quick Connect" and was connected to the Netherlands.

![Screen Shot 2023-12-19 at 1 08 30 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/91fb8b8f-1a7e-49c9-94ae-8734970776c1)

![Screen Shot 2023-12-19 at 1 09 29 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/d6d38ae2-032e-4927-8be1-3a161e99328b)

-  Below is a visual representation of everything we have done so far.

![Screen Shot 2023-12-16 at 1 57 32 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/9fd48842-d0f3-4386-87ea-4fd9eb7f1df1)

Now browse back on to "whatismyipaddress.com" again from within the Azure virtual machine. As the VPN is now active, observe how the new IP address and location is different. This IP address should reflect the location of the VPN server (e.g., Netherlands).

![Screen Shot 2023-12-19 at 1 13 46 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/e4c42383-c2bc-4340-8d02-a22f5805d4c3)

As you can see when you also access different websites like Google, Netflix, or Apple, you can see that in relation to the location of the VPN, many different things about these sites could be different. For example, the languages, URL, or even advertisements are all specifically geared towards that country.

![Screen Shot 2023-12-19 at 1 15 54 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/8197b7b0-5a59-46a0-a661-4ce33a692145)
![Screen Shot 2023-12-19 at 1 17 40 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/993bc5c1-8836-486a-8875-a54d22180e13)
![Screen Shot 2023-12-19 at 1 18 34 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/dcccc652-fbc7-4f79-9ead-7e3c383f58c0)

As always, if you are following this & completed everything, remember to clean up and delete the Resource Group(s) that was created for your Virtual Machine within Azure as this may eat up all of your credits or rack up a huge bill if left unattended. Below is the process of how I go about deleting them. 
    
![Screen Shot 2023-12-19 at 1 22 15 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/d181c076-53aa-43da-a9da-aaceceb05fbb)


## Results

![Screen Shot 2023-12-16 at 1 58 15 PM](https://github.com/Emq17/Observing-IP-Addresses-Through-ProtonVPN/assets/147126755/4bf91c3f-658f-4d02-8473-b300cd317e90)

Hopefully this walkthrough provided a better understanding on Virtual Private Networks while also helping you learn how to set things up including a Virtual Machine on Azure, a PC on Microsoft Remote Desktop, and a VPN using ProtonVPN.

In Summary: 

You will see a total of 3 different locations and IP addresses while you are completing this walkthrough:

-  One within your personal computer.
-  Another for your virtual machine.
-  And the last one using ProtonVPN inside of your VM.

