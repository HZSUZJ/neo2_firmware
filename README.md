# neo2_firmware
这里的固件都是没有oled驱动的，所以有屏幕版本的neo2可以用这里的固件，但是屏幕是不亮的
## 固件升级方法
进入系统 -> 备份/升级 -> 刷写新的固件 ->  选择文件 -> 更新固件  （建议不保留配置升级）  
![image](https://github.com/HZSUZJ/neo2_firmware/blob/master/images/1.jpg)
![image](https://github.com/HZSUZJ/neo2_firmware/blob/master/images/2.png)

**升级后，一般还是原来的ip去访问。倘若不行，去路由器（或光猫）后台查看分配给neo2的ip，neo2的主机名为openwrt**  

## 可能遇到的问题
单臂路由模式下，如果无法访问国内网站，尝试在网络防火墙自定义规则添加这条规则（请注意要求eth0为LAN口）：  
iptables -t nat -I POSTROUTING -o eth0 -j MASQUERADE  
或者这条规则（有桥接存在的情况下）：  
iptables -t nat -I POSTROUTING -o  br-lan  -j MASQUERADE



## 固件地址
固件ip默认DHCP  
[历史固件](https://github.com/HZSUZJ/neo2_firmware/releases)

## 如果帮助到您，能给颗star鼓励下嘛~~
