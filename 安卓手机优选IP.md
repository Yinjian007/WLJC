CF Workers搭建的免费代理节点，在windows电脑端可轻松实现高速IP的优选，来提高节点速度。那么如何在安卓设备上优先IP，来获得高速节点呢？这里介绍2个优选工具在安卓设备上的使用！

1.首先在我们手机端安装Termux

它是一个安卓手机模拟Linux环境，提供标准的命令行界面，让手机也能变身轻量化的DIY极客工具。软件开源且不需要root权限，可以安装其他Linux发行版，支持pkg、apt软件包管理，可以很方便找到安装软件包，也可以跑Nginx、PHP、MySQL、Python、NodeJS等。

官网下载：https://termux.dev/en/

注意：在开始优选前请确认关闭你的代理工具，否则导致测速不准。

2.优选步骤

badafans大佬的Better -cloudflare -ip 项目

1.打开termux,输入以下命令安装依赖

pkg update && pkg install wget curl

2.安装，运行命令，自动进入优选测速

第一次安装和运行

curl https://raw.githubusercontent.com/badafans/better-cloudflare-ip/master/shell/cf.sh -o cf.sh && chmod +x cf.sh && ./cf.sh

下一次直接输入以下命令运行

./cf.sh

3.ls命令查看文件，如果下载后无colo.txt、ips-v4.txt、ips-v6.txt和url.txt文件，那么可使用命令下载：

wget https://www.baipiao.eu.org/cloudflare/colo -O colo.txt

wget https://www.baipiao.eu.org/cloudflare/ips-v4 -O ips-v4.txt

wget https://www.baipiao.eu.org/cloudflare/ips-v6 -O ips-v6.txt

wget https://www.baipiao.eu.org/cloudflare/url -O url.txt

有关操作的命令大家可以自行查找，比如cat为打开txt文件命令。如果测速时没有反应，要先按8更新数据，然后再进行测速。

Xiu2大佬的Cloudflarest项目

1.安装依赖

pkg update && pkg install wget tar

2.下载安装文件

wget -N https://github.com/XIU2/CloudflareSpeedTest/releases/latest/download/CloudflareST_linux_arm64.tar.gz

如果wget命令运行失效或报错，可偿试curl命令

curl -z CloudflareST_linux_arm64.tar.gz -o CloudflareST_linux_arm64.tar.gz -L https://github.com/XIU2/CloudflareSpeedTest/releases/latest/download/CloudflareST_linux_arm64.tar.gz

两个命令目的一样，curl 命令会从给定的 URL 下载文件，并且仅在远程文件更新时才会下载新版本，达到类似于 wget -N 的效果。

然后依次运行下面两个命令即安装完成：

tar -xzvf CloudflareST_linux_arm64.tar.gz

chmod +x CloudflareST

3.优选测速

./CloudflareST -url https://download.parallels.com/desktop/v17/17.1.1-51537/ParallelsDesktop-17.1.1-51537.dmg -tl 250 -sl 5

-url是指定测速地址 -tl 250是最高延迟250，-sl 5是最低下载速度5MB。

因作者已说明软件自带测速失效，可指定测速地址或自已搭建测速地址。大家可在作者说明区找别人分享的测速地址。


