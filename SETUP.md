# Setting up the Raspberry Pi

## Enabling SSH

https://roboticsbackend.com/enable-ssh-on-raspberry-pi-raspbian/

Steps followed:

- In the imager:
  - Enable SSH
  - Set a <username> and a password
  - Enter Wifi name (SSID) and Wifi password
  - Enter custom hostname: <my_hostname>

- Connect imager to the Pi
- In computer terminal: `ping <my_hostname>.local`
  - Gets the IP address of the Pi

- `ssh <username>@<ip_address>`
