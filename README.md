# RaspotifyCast

![RaspotifyCast](images/RaspotifyCast.jpg)

## Description
This project shows the necessary process to use a **Raspberry PI 3** as a **ChromeCast** + **Spotify** client.

## Necessary packages & acknowledges:

1) [RaspiCast](https://play.google.com/store/apps/details?id=at.huber.raspicast&hl=es)
2) [OMXV](git clone https://github.com/HaarigerHarald/omxiv)
2) [Raspotify](https://github.com/dtcooper/raspotify)

## PART 1: SETTING THE RASPBERRY

#### QUICK Setup (Ethernet connection necessary)

1) Just donwnload the already baked SD Card image in: [link](www.google.com)
2) Download ETCHER to burn de image into SD Card: [link](https://etcher.io/)
3) Burn the image into SD Card.
4) Connect the Raspberry to TV via HDMI and to network via Ethernet Cable.
5) The RapotifyCast should be accesible via ssh by doing: 'ssh pi@raspofifycast.local' (password: "raspberry")

#### AUTOMATIC Setup (Ethernet or Wifi)
Still under work.

#### MANUAL Setup (Ethernet or Wifi)

1) Download Raspbian-Lite Image: [Raspbian-Lite](https://downloads.raspberrypi.org/raspbian_lite_latest)
2) Download ETCHER to burn de image into SD Card: [link](https://etcher.io/)
3) Burn the image into SD Card.
4) Open the SD Card in your machine and open **Boot** partition.
5) Add an empty file called **ssh** and save it.
6) Download the file [**wpa_supplicant.conf**](files/wpa_supplicant.conf).
7) Edit **wpa_supplicant.conf** setting your WIFI network parameters 'SSID_NAME" and "PASSWORD" and save it in **Boot** partition.
8) Extract securely SD Card, insert it into your Raspberry and power it on.
9) Connect to Raspberry via **SSH**. Open a terminal and enter: 'ssh pi@raspberrypi.local"
10) Type: 
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade

11) Change Raspberry settings via **Raspi-Config**. Type: 'sudo raspi-config'.
  a. Change Localization settings to your country.
  
  ![raspi-localization](images/raspi-config_localization.png)
  
  b. Change Boot settings to "Command Line with user Password".
  
  ![raspi-boot](images/raspi-config_boot.png)
  
  c. Enter in advance settings and expand filesystem to the whole SD Card.
  
  ![raspi-expand](images/raspi-config_expad.png)
