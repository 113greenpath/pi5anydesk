# pi5anydesk
Pi5 Anydesk Solution.

Download file: anydesk_FIX_P5_arm64.deb

Follow step by step

Install necesary dependecies:
sudo apt-get install -y libgtkglext1

Install Fixed installer:
sudo dpkg -i anydesk_FIX_P5_arm64.deb
sudo apt-get -f install

Apply binaries Fixes:
ldd /usr/bin/anydesk | grep "not found"
cd /usr/lib/aarch64-linux-gnu
sudo ln -s libudev.so.1 libudev.so.0

Enable Anydesk service:
anydesk
anydesk &
sudo systemctl enable anydesk.service
sudo systemctl start anydesk.service
systemctl status anydesk.service

ENJOY ANYDESK!

If you are using wayland composer incoming conections are not working.

