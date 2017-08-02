# vps的相关操作

* [vps申请地址](#vps申请地址)
* [vpn搭建](#vpn搭建)
* [wdcp安装](#wdcp安装)
* [ftp登陆](#ftp登陆)


## vps申请地址

[https://bandwagonhost.com/clientarea.php?action=products](https://bandwagonhost.com/clientarea.php?action=products "搬瓦工网站")

使用连接vps软件是Shell 5

## vpn搭建

启动shell，添加ip，用户名默认是root，密码从账户中可以查看到

在运行窗口输入一下三段代码：
```
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```
按照要求添加vpn相关的参数，等待安装
安装的版本是Shadowsocks-Go 版
安装成功的标识
```
Congratulations, your_shadowsocks_version install completed!
Your Server IP        :your_server_ip
Your Server Port      :your_server_port
Your Password         :your_password
Your Encryption Method:your_encryption_method

Welcome to visit:https://teddysun.com/486.html
Enjoy it!
```
参考网址

[https://teddysun.com/486.html](#https://teddysun.com/486.html "vpn安装参考地址")

## wdcp安装
安装wdcp面板
```
wget http://banwagong.cn/tools/wdcp.sh
```
安装nginx+apache+php+mysql环境
```
sh wdcp.sh
```

安装成功的标识
```
============  lanmp_wdcp install OK  ==============



          configuration ,lamp or lnmp,wdcp install is finshed
          visit http://ip
          wdcp visit http://ip:8080
          more infomation please visit http://www.wdlinux.cn

```

登陆wdcp面板地址http://ip:8080
登录名是admin
密码是wdlinux.cn

进入后可以先修改wdcp和mysql的密码
创建一个站点和一个ftp用户
站点的域名没有可以直接添加default
ftp创建时要关联站点

参考地址

[http://banwagong.cn/install-wdcp.html](#http://banwagong.cn/install-wdcp.html "wdcp安装参考地址")

## ftp登陆
下载软件WinSCP
选择的端口号是21，用户名和密码填写wdcp上创建的就可以

