# myfetch

A customized terminal system fetch tool that plays a video animation using [Anifetch](https://github.com/Notenlish/anifetch) before displaying extended system information via a modified [Neofetch](https://github.com/dylanaraps/neofetch) configuration.
---

[![Neofetch](https://img.shields.io/badge/Neofetch-yellow?logo=gnu-bash)](https://github.com/dylanaraps/neofetch)
[![Anifetch](https://img.shields.io/badge/Anifetch-yellow?logo=python)](https://github.com/Notenlish/anifetch)

---

## Installation

## neofetch
```bash
sudo apt install neofetch
```

### 1. Install dependencies

```bash
sudo apt update
sudo apt install -y python3 ffmpeg chafa curl lscpu pciutils
````

### 2. Clone Anifetch

```bash
sudo git clone https://github.com/Notenlish/anifetch.git
sudo chown -R $USER:$USER anifetch
```

> You can also replace the default video with your own: place it as `example.mp4` inside `~/anifetch/`.

---

## Setup `myfetch` script

### 3. Create and edit the script

```bash
sudo nano /usr/local/bin/myfetch
```

Paste the following contents:

```bash
#!/bin/bash
clear
cd /opt/anifetch/
python3 anifetch.py "example.mp4" -r 10 -W 70 -H 50 -c "--symbols wide --fg-only"
bash ~/.config/neofetch/config.conf
```

Make it executable:

```bash
sudo chmod +x /usr/local/bin/myfetch
```

Now you can run:

```bash
myfetch
```

---

## Credits

* [Anifetch](https://github.com/Notenlish/anifetch) – terminal video rendering
* [Neofetch](https://github.com/dylanaraps/neofetch) – base system info
* [wttr.in](https://github.com/chubin/wttr.in) – terminal weather
* [ipinfo.io](https://ipinfo.io) – server geolocation
* [Chick2D/neofetch-themes](https://github.com/Chick2D/neofetch-themes) – awesome Neofetch themes
