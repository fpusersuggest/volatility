# effetturare un dump di ram con lime

```
apt install make gcc gcc-7/unstable inux-headers-`uname -r`
wget https://github.com/504ensicsLabs/LiME/archive/master.zip
unzip master.zip
cd lime
cd src
make
```


# come creare un profilo per volatility
```
apt install subversion build-essential dwarfdump make gcc gcc-7/unstable linux-headers-`uname -r` zip -y
torify svn checkout https://github.com/volatilityfoundation/volatility/trunk/tools/linux
apt-get install -d --reinstall linux-image-`uname -r`
cd linux && make
zip vol-prof-tails-`uname -r`.zip module.dwarf /boot/System.map-`uname -r`
```
