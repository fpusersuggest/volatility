# volatility

# creare profile per volatility
apt install subversion -y
torify svn checkout https://github.com/volatilityfoundation/volatility/trunk/tools/linux
apt install build-essential dwarfdump
apt install make gcc
apt install gcc-7/unstable
apt install linux-headers-`uname -r`
cd linux
make
apt-get install -d --reinstall linux-image-`uname -r`
apt install zip -y
zip vol-prof-tails-`uname -r`.zip module.dwarf /boot/System.map-`uname -r`

