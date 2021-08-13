```
echo -e "nameserver 2001:67c:2b0::4•\nnameserver 2001:67c:2b0::6" > /etc/resolv.conf
echo "deb http://deb.debian.org/debian/ unstable main" > /etc/apt/sources.list.d/unstable.list
printf 'Package: *\nPin: release a=unstable\nPin-Priority: 150\n' > /etc/apt/preferences.d/limit-unstable
apt update
apt-get install dnsutils -y
```
