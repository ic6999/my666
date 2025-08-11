

【BPB面板最新版本】

https://github.com/bia-pain-bache/BPB-Worker-Panel/releases

-手动更新：

https://github.com/ic6999/p1/actions/workflows/update-worker.yml

-v3.2.7之前稳定版本已收录在本项目release目录

-修改过的同步代码：release/iworkflows.yml:每月更新一次；只删除旧版worker.js,保留主目录下其他文件。

【v3.2.3】

-PROXYIP环境变量重命名为PROXY_IP 

-从现在开始，多个IP/域可以用ENTER而不是逗号分隔。

【Pages搭建教程】

1.GitHub建项目库

.github/workflows/update-worker.yml

代码地址:
https://github.com/xiaobaikeji831/cfDAIMA/blob/main/bpb%20%E4%BB%A3%E7%A0%81

2.Cloudflare项目设置

创建pages-连接到git

添加自定义域名：
https://p1.ic666.ddns-ip.net/panel

添加变量:
UUID：
PROXY_IP：
TR_PASS：
KV空间:kv/p1

3.配置 BPB 面板参数

VLESS - Trojan基础设置
Fake DNS:
Enabled
Proxy IPs / Domains:
141.147.156.68、cdn-xx-b6gac.acu.org
Clean IPs / Domains:
104.17.212.246、104.19.19.167
Protocols
VLESS 和 Trojan 都勾选
TLS Ports
勾选：443、8443、2053、2083、2087、2096


@GitHub Actions 使⽤ 5 字段 Cron 语法字段顺序为：

分钟 ⼩时 ⽇期 ⽉份 星期

示例：

• 0 2 * * * 每天 UTC 时间 2:00 运⾏ 北京时间 10:00

• */15 * * * 每 15 分钟运⾏⼀次｡

• 0 0 * * 1 每周⼀次， UTC 时间 周一0:00 北京时间 8:00

0 0 1 * * 每月一次，1日0时运⾏

0 0 1 1 * 每年一次，1月1日0时运⾏

https://crontab.guru #详细参数说明





## 使用方法[视频教程](https://youtu.be/sWy9gCBA5Lo)
1. 新建一个私人仓库，项目可随意命名，但要避开 BPB 敏感词。
2. 在该项目创建`.github/workflows/Obfuscate.yml`。
3. 复制`创建仓库源码.js`的代码，粘贴到项目，保存。
4. 点击`Obfuscate.yml`旁边的小黄点同步到 BPB 代码，同步完成生成`_worker.js`与`origin.js`，前者是混淆代码，后者是明文代码。如果找不到小黄点，请前往：`你的项目`→`Actions`→左边的`Build Obfuscate BPB Panel`→中间的`Build Obfuscate BPB Panel`的工作流文件是否有效。
7. 到`Cloudflare`里创建`Pages+github`，找到刚刚的 github 项目，用其创建 Pages 项目，并修改下面的变量及绑定 kv 空间。
8. 引用请注明出处：[SO启程Github](https://github.com/Setout8/Book-Pen-Book)。

## 变量的使用
1. `UUID`，[在线生成](https://1024tools.com/uuid)。
2. `PROXYIP`，来源于网络分享：`proxy.xxxxxxxx.tk`、`edgetunnel.anycast.eu.org`、`ts.hpc.tw`、`cdn.xn--b6gac.eu.org`、`cdn-all.xn--b6gac.eu.org`、`bestproxy.onecf.eu.org`。
3. `TR_PASS`，默认要修改的密码。
4. `kv`，绑定`KV命名空间`。
5. `/panel`，部署成功后，在 url 后面增加/panel来进行访问面板，访问面板修改的密码将会保存在`kv`对里。

## IP优选工具的使用
1. win 电脑下载`IP优选工具/CF优选官方IP[win电脑版].7z`，解压后，退出VPN，运行本软件。
2. 下载[CloudflareScanner](https://github.com/bia-pain-bache/Cloudflare-Clean-IP-Scanner/releases/tag/v2.2.5)，解压后，退出VPN，运行本软件。

# 特别感谢
[bia-pain-bache](https://github.com/bia-pain-bache)
