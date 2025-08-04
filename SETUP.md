# Setting up the Raspberry Pi

## Enabling SSH

https://roboticsbackend.com/enable-ssh-on-raspberry-pi-raspbian/

Steps followed:

- In the imager:
  - Enable SSH
  - Set a <user_name> and a password
  - Enter Wifi name (SSID) and Wifi password
  - Enter custom hostname: <my_hostname>

- Connect USB stick or micro SD card containing the imager to the Pi
- In computer terminal: `ping <my_hostname>.local`
  - Gets the IP address of the Pi

- `ssh <user_name>@<ip_address>`
