# trojan
VPS搭建Trojan
bash <(curl -sL https://raw.githubusercontent.com/daveleung/hijkpw-scripts-mod/main/trojan_mod1.sh)

原文链接：https://v2xtls.org/trojan%E4%B8%80%E9%94%AE%E8%84%9A%E6%9C%AC/


本文转载自：https://v2raytech.com/trojan-one-click-scrip/，如文中内容有错误请到原文查看原始版(最新版)

如果你这周看到本站默默地在更新trojan客户端教程，是不是想到服务端一键脚本也快了？没错，今天正式完成了trojan一键安装脚本，支持CentOS 7/8和Ubuntu 16.04及以上版本，目前已经上传到 Github。

注意：

1. 如果服务器已经有运行网站，请联系网站运维再执行脚本，否则可能导致原来网站无法访问，本人不负责！

2. 对域名没有要求，不管国内还是国外注册的都可以，不需要备案，不会影响使用，也不会带来安全/隐私上的问题；

3. 根据 Namesilo购买域名详细教程 购买的域名，默认@和www在买之前都已经做了解析，因此尽管www已经改成了你服务器的ip，但执行本脚本时可能还会出现“主机未解析到当前服务器IP”的错误。这时只需要换个名称做解析即可，例如 www2；

4. 除非443端口被墙或另有它用，建议使用443！本脚本支持上传自定义证书，可用在NAT VPS上。

5. BBR换成魔改BBR/BBR Plus/锐速清参考：安装魔改BBR/BBR Plus/锐速(Lotserver)；

6. 刚搭建好trojan不要猛上流量，否则可能导致被限速、端口被墙，严重可能ip被墙。

trojan一键脚本使用教程
1. 请准备一台境外服务器和一个域名。想服务器速度快请参考 搬瓦工VPS购买教程 或从  CN2 GIA VPS商家推荐 选购 ，想ip被封后免费换请参考：购买vultr服务器超详细图文教程。对域名没有要求，国内/国外注册的都可以，不需要备案，不会影响使用，也不会带来安全/隐私上的问题。购买域名可参考：Namesilo购买域名详细教程；

值得一提的是本V2ray一键脚本支持ipv6 only服务器，但是不建议用只有ipv6的VPS用来科学上网。

2. 如果vps运营商开启了防火墙（阿里云、Ucloud、AWS、GCP等默认开启，搬瓦工/hostdare/vultr默认关闭），请先登录vps管理后台放行80和443端口，否则会导致获取证书失败；此外，本脚本支持上传自定义证书，可跳过申请证书这一步，也可用在NAT VPS上。

3. ssh登录到服务器（windows请参考 Bitvise连接Linux服务器教程，mac用户请参考 Mac电脑连接Linux教程），在终端（黑框框）输入如下命令：

bash <(curl -sL https://raw.githubusercontent.com/daveleung/hijkpw-scripts-mod/main/trojan_mod1.sh)
按回车键，将出现如下操作菜单。如果菜单没出现，CentOS系统请输入 yum install -y curl，Ubuntu/Debian系统请输入 sudo apt install -y curl，然后再次运行上面的命令：

trojan一键脚本菜单
trojan一键脚本菜单
根据菜单选择操作，其中安装时会要求输入一些信息，请根据提示输入，或者直接回车使用默认值。

接下来脚本会自动疯狂运行，如果安装过程卡住，请耐心等待几分钟；期间网络断开（windows上表现为黑框框中或者顶部标题出现disconnected字样，mac表现为终端出现“closed by remote host”或”broken pipe”），请重新连接后再次执行命令。脚本运行成功会输出配置信息，截图如下：

trojan一键脚本输出结果

trojan一键脚本输出结果

到此服务端配置完毕，服务器可能会自动重启（没提示重启则不需要），windows终端出现“disconnected”，mac出现“closed by remote host”说明服务器成功重启了。

trojan一键脚本注意事项
1. . 脚本默认使用BBR加速技术，BBR换成魔改BBR/BBR Plus/锐速清参考：安装魔改BBR/BBR Plus/锐速(Lotserver)；

2. 部署好后伪装建站请参考：trojan建站教程；

3. 刚搭建好trojan不要猛上流量，否则可能导致被限速、端口被墙，严重可能ip被墙。

trojan客户端下载
接下来是科学上网最后一步：

下载  trojan客户端，按照其中的配置教程配置客户端。

一切顺利的话，就可以愉快的上外网了！
