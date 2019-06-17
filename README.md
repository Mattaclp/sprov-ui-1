Because the author deleted the code, I tried to make a script address with one click.
______________________________________________________________________________
user#:

wget -O /usr/bin/sprov-ui -N --no-check-certificate https://github.com/Mattaclp/sprov-ui-1/raw/master/sprov-ui.sh && chmod +x /usr/bin/sprov-ui && sprov-ui

Tested .It can be install on Ubuntu successful.

This script collection BBR,BBR Magic,BBR Plus,Lotserver

If you install TCP Accelerate you must manusal open acceleration

code:
./tcp.sh

You can use   # sysctl net.ipv4.tcp_available_congestion_control   # to see if it‘s started

return "net.ipv4.tcp_available_congestion_control = bbr cubic reno"  or net.ipv4.tcp_available_congestion_control = reno cubic bbr

You can use   # net.ipv4.tcp_congestion_control = bbr   # to see if it‘s started

return net.core.default_qdisc = fq

You can use   #  lsmod | grep bbr # to see if it‘s started

return tcp_bbrplus            20480  8

If any of the above items occur, the startup is successful.
______________________________________
Statement: Anyone who uses this script in illegal ways has nothing to do with me and I am not liable for any major legal responsibility.
