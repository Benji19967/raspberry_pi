# Setting up the Raspberry Pi

## Imager

Download the Imager onto laptop.

- Launch the imager, and then:
  - Enable SSH
   - Use `id_ed25519.pub` key
  - Set a <user_name> (e.g. `labrecqb`) and a password
  - Enter Wifi name (SSID) and Wifi password
  - Enter custom hostname: <my_hostname> (`ben-raspi`)

- Connect USB stick or micro SD card containing the imager to the Pi


## User data

You can always check the info (<user_name>, <my_hostname>, etc) you configured on the bootloader in the file
`user-data` (open it with a text editor).

## SSH

### Get IP of PI

#### Option 1

`ping <my_hostname>.local`

#### Option 2

Get local ip address:

```
ipconfig getifaddr en0
```

Find the ip address of the Raspberry Pi (may need to rerun this a few times until 
the Pi is registered to the network):

```
sudo nmap -sn -n <ip_address>/24
```

```
...
Nmap scan report for 192.168.0.24
Host is up (0.13s latency).
MAC Address: ... (Raspberry Pi Trading)
...
```

### ssh into the rpi:

```
ssh <user_name>@<ip_address_rpi>
```

## Github


On the pi, generate an ssh keypair:
```
ssh-keygen -t ed25519 -C "raspberry-pi-key"
```

and add the public key to github ssh keys.
