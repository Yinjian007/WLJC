__大佬都在用的VPS神级一键脚本 内核版本在提升 TCP性能调优一应俱全__

 

一键脚本
apt update -y && apt install -y wget sudo


wget --no-check-certificate -O tcpx.sh https://raw.githubusercontent.com/ylx2016/Linux-NetSpeed/master/tcpx.sh


chmod +x tcpx.sh


./tcpx.sh


以后运行
./tcpx.sh




注意
更新内核需要谨慎 使用后台运行模式最稳妥，我在SSH自动中断后失联了一台服务器。

tmux后台工具使用介绍
https://youtu.be/-PUGYFlV0_g


