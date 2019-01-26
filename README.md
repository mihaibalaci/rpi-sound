# Linux-Audio
Debian Based RPi tweaks for improved sound.

I've tested it on both Volumio and Moode Audio

 To improve the sound of the Raspberry Pi using Debian and other distributions of Linux several parameters can be adjusted.
 1) Improving the priority of the Audio group
 2) Imroving the audio thread priority
 3) Improving the latency of the Operating System with Kernel adjustments
 4) Improve network latency
 ______________________________________________________________________________________________________________________________
 ## Prerequisites
 1) vi file editor; apt install vi


**Should work on any SBC running Debian based OS, has been tested on:**

- Raspberry Pi (v1) model B
- Raspberry Pi 2 model B
- Raspberry Pi 3 model B and B+
- ASUS Tinkerboard
- Odroid C2
 ______________________________________________________________________________________________________________________________
 ## Automated Install
 curl -sSL https://github.com/mihaibalaci/rpi-sound/blob/master/basic-install.sh | bash

 ##### Optional method:
 - wget https://github.com/mihaibalaci/rpi-sound/blob/master/basic-install.sh
 - chmod 755 basic-install.sh
 - sudo ./basic-install.sh
 ## Automated Removal
 curl -sSL https://github.com/mihaibalaci/rpi-sound/blob/master/remove.sh | bash

 ##### Optional method:
 - wget https://github.com/mihaibalaci/rpi-sound/blob/master/remove.sh
 - chmod 755 remove.sh
 - sudo ./remove.sh

 ______________________________________________________________________________________________________________________________
 ## Kernel Adjustments and Audio Thread Priority - manual install
 1) Create file in /usr/bin called Sound.sh with the text editor nano; nano Sound.sh
 2) Copy and past the contents of Sound.sh into the file, change permissions to 755
 3) Create a service in /etc/systemd/system called sound.service with nano; nano sound.service
 4) Copy and paste the contents of sound.service into the file
 5) enable the service; systemctl enable sound.service
 6) start the service; systemctl start sound.service

 ## Audio Group Priority - manual install
 1) Copy and past the contents of limits.conf into /etc/security/limits.conf, above the last line that says #End of file.

 ## Network Latency - manual install
 1) Copy and past the contents of sysctl.conf into /etc/sysctl.conf


_____________________________________________________________________________________________________________________________
