Dear Tumbleweed users and hackers,

The last two weeks were quite busy with snapshots: if you keep up at full pace, you received 7 new snapshots: 1116, 1118, 1120,  1122, 1126, 1128 and 1129.
These snapshots brought these updates (and many more, as usual):

* KDE Frameworks 5.52.0
* FFmpeg 4.1
* systemd 239
* Linux kernel 4.19.2 & 4.19.4
* Mozilla Firefox 63.0
* openSSH 7.9p1: default config no longer permits root access using password auth

Changes that are currently being staged and tested:

* glibc 2.28, Python 3.7, openssl 1.1.1: the three all interdepend on each other and cause a bunch of new failures – See Staging:C
* LLVM7 / Mesa 18.2.x (rust fails to build with LLVM7)
* Installer redesign: the sidebar is coming back (showing where in the installation workflow one is currently)
* PostgreSQL 11
* KDE Plasma 5.14.4

