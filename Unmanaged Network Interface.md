Received error "ethernet-device-not-managed" while assigning Network Monitoring Interfaces during initial setup.  

To get past this problem, make the below adjustment:

sudo nano /usr/lib/NetworkManager/conf.d/10-globally-managed-devices.conf

change the value for 'unmanaged-devices=*' to 'unmanaged-devices=none'

save and restart Network Manager with sudo system restart NetworkManager
