[return](debianinstall)

:sources.list:

When debian is installed from an unofficial stable DVD image with 
non-free firmwares included. There is no need to batch install
non-free firmwares. System, system security and package downloading
updating can simply be done by editing the /etc/apt/sources.list
with one of the following scripts.

deb http://deb.debian.org/debian bullseye main contrib non-free
deb-src http://deb.debian.org/debian bullseye main contrib non-free

deb http://deb.debian.org/debian-security/ bullseye-security main contrib non-free
deb-src http://deb.debian.org/debian-security/ bullseye-security main contrib non-free

deb http://deb.debian.org/debian bullseye-updates main contrib non-free
deb-src http://deb.debian.org/debian bullseye-updates main contrib non-free


Or,

deb https://deb.debian.org/debian bullseye main contrib non-free
deb-src https://deb.debian.org/debian bullseye main contrib non-free

deb https://deb.debian.org/debian-security/ bullseye-security main contrib non-free
deb-src https://deb.debian.org/debian-security/ bullseye-security main contrib non-free

deb https://deb.debian.org/debian bullseye-updates main contrib non-free
deb-src https://deb.debian.org/debian bullseye-updates main contrib non-free

Or,

deb tor+http://vwakviie2ienjx6t.onion/debian bullseye main contrib non-free
deb-src tor+http://vwakviie2ienjx6t.onion/debian bullseye main contrib non-free

deb tor+http://sgvtcaew4bxjd7ln.onion/debian-security bullseye-security main contrib non-free
deb-src tor+http://sgvtcaew4bxjd7ln.onion/debian-security bullseye-security main contrib non-free

deb tor+http://vwakviie2ienjx6t.onion/debian bullseye-updates main contrib non-free
deb-src tor+http://vwakviie2ienjx6t.onion/debian bullseye-updates main contrib non-free












