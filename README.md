# rPi-5-Install-UBUNTU-DESKTOP-24.04-LTS-64bit
## Create a SD Card with the "Raspberry Pi Imager"
You can get the "Raspberry Pi Imager" here:
https://www.raspberrypi.com/software/

I choose a 500 GB SSD for the rPi5. An SSD is faster than a SD-Card

### Start the "Raspberry Pi Imager" and create the image and fill in the following fields:

- Raspberry Pi Modell : **RASPBERRY PI 5**

- Betriebssystem (OS) : **Other general-porpose OS | Ubuntu | Ubuntu Desktop 24.04 LTS (64bit)**

- SSD            : **be careful ! The Data of the SSD will be lost.**

### Connect your HW to the rPi

- USB 500 GB SSD
- USB mouse
- USB Keyboard
- Display (micro HDMI connector near to the USB C connector)
- Power up the rPi

### Basic configuration

- After first boot of the rPi you have to do some configuration
- System Configuration | Welcome: **Select you language (I chooseEnglish)**
- System Configuration | Keyboard layout: **I used "Detect Keyboard Layout" and ends up with German|German**
- System Configuration | Wireless: **select "Connect to this network" and then select your WiFi and press Connect. Then type your credentials**
- System Configuration | Where are you: **My selection was "Berlin"**
- System Configuration | Who are you: **fill in the information needed**
- System Configuration | The rPi will configure the system. **The graphic look terrible**

If you succeed you will get a window with: **Welcome to Ubuntu Noble Numbat**

### Next steps
- Ubuntu Pro | Enable Ubuntu Pro: **I choose Skip for now**
- Help improve Ubuntu: **I support Ubuntu and choose "Yes, share system data with the Ubuntu team"**
- Ready to go | Get started with more applications: **install what you like**

### Software update
- start "Software Update" not "Software & Updates"
- If updates available, install them
- If needed, perform a restart

### It's a rPi .... install raspi-config
```
sudo apt-get update
sudo apt-get install raspi-config
```

**!!! lets go now !!!**

### Troubleshooting
#### Firefox doesn't start
```
sudo killall firefox
sudo snap refresh
sudu shutdown -r now
```
### install additional apps features
#### keepass
```
sudo apt install libcanberra-gtk-module
sudo apt install keepass2
```
#### net-tools (ifconfig)
```
sudo apt install net-tools
```
#### enable screen sharing
```
sudo apt install gnome-remote-desktop 

sudo apt install vino
sudo vi /etc/gdm3/custom.conf
```
in this configuration remove the # from the following line:
```
# WaylandEnable=false
```







