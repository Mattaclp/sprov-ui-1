Because the author deleted the code, I tried to make a script address with one click.
______________________________________________________________________________
user#:

wget -O /usr/bin/sprov-ui -N --no-check-certificate https://github.com/Mattaclp/sprov-ui-1/raw/master/sprov-ui.sh && chmod +x /usr/bin/sprov-ui && sprov-ui

Tested .It can be install on Ubuntu successful.

运行管理脚本：sprov-ui

如果提示 curl: command not found ，那是因为你的 VPS 没装 Curl
ubuntu/debian 系统安装 Curl 方法: apt-get update -y && apt-get install curl -y
centos 系统安装 Curl 方法: yum update -y && yum install curl -y
安装好 curl 之后就能安装脚本了

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
