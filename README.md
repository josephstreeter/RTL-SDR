# RTL-SDR
Software Defined Radio using RTL-SDR dongle on Ubuntu Linux

[More information](https://ranous.files.wordpress.com/2016/03/rtl-sdr4linux_quickstartv10-16.pdf)

### RTL-SDR 
A package for Ubuntu: [[https://launchpad.net/ubuntu/bionic/+...](https://launchpad.net/ubuntu/bionic/+package/rtl-sdr)]

### RTL_FM 
A cli demodulation tool: http://kmkeen.com/rtl-demod-guide/

### GQRX
graphical spectrum analyzer: http://http://gqrx.dk    
To install: sudo apt-get install gqrx

### ACARS DECODER 
A realtime aircraft message decoding: https://github.com/TLeconte/acarsdec
Check ACARS frequency here: https://www.acarsd.org/ACARS_frequencies.html

### DUMP1090 
ADS-B airplane messages DECODER: https://github.com/antirez/dump1090 / https://www.ads-binfo.com/

### RTL_433
Decoding Low Power devices on unlicensed bands 433MHz/315 MHz/ 868MHz / 915MHz - like keyfobs, meteo/weather stations, sensors sniffer: https://github.com/merbanan/rtl_433

### MULTIMON-NG
A multi system DECODER: https://github.com/EliasOenal/multimon-ng
APRS (Automatic Packet Reporting System) decoding video using MULTIMON-NG  here [https://www.youtube.com/watch?v=Cfnrr... ](https://www.youtube.com/watch?v=CfnrrJwwNU8&t=4s)

CAPTURING & DECODING SATELLITES with NOAA-APT with simple dipole antenna  - see my other video here : [https://www.youtube.com/watch?v=Fk0WU...](https://www.youtube.com/watch?v=Fk0WUWd73O8&t=218s)

# UBUNTU 18.04 and RTL-SDR Dongle Setup
RTLSDR installation on Ubuntu:

Check if USB RTLSDR is detected and what are Product_ID and Vendor_ID (f.ex. idVendor=0bda, idProduct=2832 )

```
lsusb
```

Blacklist ordinary DVB-T drivers in Linux Kernel not to interfere with rtlsdr library

```
vi /etc/modprobe.d/blacklist.conf
```

add in this file  following lines (add line respectively to ProductID value) :

```
blacklist dvb_usb_rtl28xxu 
blacklist rtl2832 
blacklist rtl2830
```

Restart Computer

Install the RTL-SDR package: [https://launchpad.net/ubuntu/bionic/+...](https://launchpad.net/ubuntu/bionic/+package/rtl-sdr)
```
sudo apt-get install rtl-sdr
```
