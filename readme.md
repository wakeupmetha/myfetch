# myfetch

sudo apt update
sudo apt install -y python3 python3-pip ffmpeg chafa curl lscpu pciutils

cd /opt
sudo git clone https://github.com/Notenlish/anifetch.git
sudo chown -R $USER:$USER anifetch
cd anifetch

sudo nano /usr/local/bin/myfetch


#!/bin/bash
clear
cd /anifetch/
python3 anifetch.py "example.mp4" -r 10 -W 70 -H 50 -c "--symbols wide --fg-only"


myfetch