# notes
modprobe fbtft_device custom name=fb_ili9488 busnum=0 cs=0 gpios=reset:110,dc:68,led:71 rotate=270 speed=65000000 bgr=1 txbuflen=65536

modprobe fbtft_device custom name=fb_ili9341 gpios=dc:3,reset:0,led:6 speed=16000000 busnum=1

modprobe fbtft_device custom name=fb_ili9486 gpios=dc:18,reset:2 speed=16000000 busnum=1 rotate=90

modprobe fbtft_device custom name=fb_ili9486 gpios=dc:18,reset:2 speed=16000000 busnum=1

dmesg | tail

apt update

apt -y install fbi

fbi -vt 1 -noverbose -d /dev/fb8 /boot/boot.bmp

con2fbmap 1 8
