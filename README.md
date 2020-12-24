# Raspi_AliDNS_DDNS
## 描述
本脚本用于在通过wifi联网（通过有线连接也可以），由DHCP分配IP的情况下，自动更新阿里云上用于访问树莓派的域名解析  
只适用于内网，非公网IP  
## 用法
关于脚本内的详细用法详见原脚本：https://github.com/h46incon/AliDDNSBash  
如果以Systemd方式使用此脚本，以下为在树莓派4B上可用的service文件示例：  
```ini
[Unit]
Description=Internal network DDns
After=dhcpcd.service
[Service]
Type=oneshot
ExecStart=/bin/bash path/to/ddns.sh
KillSignal=SIGINT
[Install]
WantedBy=multi-user.target
```
## 其它
本项目来自https://github.com/h46incon/AliDDNSBash 对原作者表示感谢  
本脚本在树莓派4B上测试通过，理论上也可用于其它设备  
