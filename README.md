# BYPASS_HSTS   

This works on Bettercap, mainly on kali linux. So, download these files and replace them in your kali bettercap's caplets directory, this is modified & a less buggy code than the original
bettercap version of HSTS_HIJACK. There are added additional payloads to it, feel free to explore.

# Before continuing with any of the of the steps given below, Download Bettercap from their page from the link below:
https://github.com/bettercap/bettercap

# Steps to replace HSTS_HIJACK on you kali ***BETTERCAP's*** Caplets Directory:

1. Locate to your bettercap install location, then the ***Caplets*** Directory.
2. Usually usr/share/bettercap/caplets
3. Locate the hstsjijack and replace it with the new file.
4. To test if it is working, go to your kali terminal and run bettercap on a virtual network.
5. Run the spoof.cap
6. type ***hstshijack***
7. Now go to your other virtual machine and type google.com, if downgrades to http from https, this means the module is working, if it doesnt work, please go through with the installation process again.

# NOTE: spoof.cap only to be downloaded on kali linux and other linux machines.

# How to run the spoof.cap:

# Note: save the spoof.cap file with the .cap extension only. 

# Commands to run spoof.cap on virtual and wlan networks

# 1. On a virtualbox network:
    
    1. bettercap -iface <name of your local interface> ex: eth0 followed by <The location of the spoof.cap> ***ex:*** /root/spoof.cap
    Command example: bettercap -iface eth0 /root/spoof.cap
    
 # 2. On a wlan network:
 
   # Note: A wireless interface capable of monitor mode and packet injection required. 
 
     1. bettercap -iface <name of your wirreless interface> ex: wlan00 followed by <The location of the spoof.cap> ***ex:*** /root/spoof.cap
     Command example: bettercap -iface wlan0 /root/spoof.cap
     
  # Modification of spoof.cap file is important:
      
     1. Before running bettercap with the spoof.cap run bettercap with the basic command ex: bettercap -iface eth0/wlan0.
     2. Note down the ip you want to listen on.
     3. Right click the spoof.cap file and edit the set arp.spoof.targets {The IP of the windows "Target"}/3rd line to the IP you are targeting
     4. Now run betterap with the caplet ex: bettercap -iface eth0/wlan0 -caplet spoof.cap


***Thank you***
