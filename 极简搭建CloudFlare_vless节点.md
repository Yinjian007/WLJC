

1.注册域名托管到CloudFlare，点击Workers和Pages,部署搭建works并修改成下面代码

复制下面链接里面的代码到wokers.js

https://github.com/zizifn/edgetunnel/blob/main/src/worker-vless.js

压缩包里有一个wokers.js备用

修改第四行，uuid 和  第九ip填写  103.200.112.108

运行下面的网站，获取5个uuid，随便选一个

https://1024tools.com/uuid

点击下面网址ip获取地址。

https://t.me/cf_push


获取测速工具，参照工具教程进行ip优选

https://github.com/XIU2/CloudflareSpeedTest

测速命令

获取的ip贴入ip.txt开始测速


CloudflareST.exe -url https://cfspeed1.kkiyomi.top/200mb.bin -tl 250 -sl 10 -tlr 0.10 -f ip.txt


测速网址问题解决网址

https://github.com/XIU2/CloudflareSpeedTest/issues


优选节点，填写到ip处，端口80，tls处置空


部署后后面加上 /自己的uuid   获取vless节点信息


如果自定义域添加后可以执行， 自定义域/自己的uuid  获取vless节点信息


如下：


################################################################
v2ray
---------------------------------------------------------------
vless://84670a50-ef6a-4cd1-ba1c-c72939acbbfb@worker-broad-disk-2ec8.zgdlxxj.workers.dev:443?encryption=none&security=tls&sni=worker-broad-disk-2ec8.zgdlxxj.workers.dev&fp=randomized&type=ws&host=worker-broad-disk-2ec8.zgdlxxj.workers.dev&path=%2F%3Fed%3D2048#worker-broad-disk-2ec8.zgdlxxj.workers.dev
---------------------------------------------------------------




clash-meta
---------------------------------------------------------------
- type: vless
  name: worker-broad-disk-2ec8.zgdlxxj.workers.dev
  server: worker-broad-disk-2ec8.zgdlxxj.workers.dev
  port: 443
  uuid: 84670a50-ef6a-4cd1-ba1c-c72939acbbfb
  network: ws
  tls: true
  udp: false
  sni: worker-broad-disk-2ec8.zgdlxxj.workers.dev
  client-fingerprint: chrome
  ws-opts:
    path: "/?ed=2048"
    headers:
      host: worker-broad-disk-2ec8.zgdlxxj.workers.dev
---------------------------------------------------------------
################################################################

