# GoogleIPRange
整合自以下gogo tester、checkgoogleip、gscan等的IP库，特别感谢各位开发者。

* [https://github.com/azzvx/gogotester/blob/2.3/GoGo%20Tester/Resources/InnerIpSet.txt](https://github.com/azzvx/gogotester/blob/2.3/GoGo%20Tester/Resources/InnerIpSet.txt)
* [https://github.com/moonshawdo/checkgoogleip/blob/master/checkip.py](https://github.com/moonshawdo/checkgoogleip/blob/master/checkip.py)
* [https://github.com/yinqiwen/gscan/blob/master/iprange.conf](https://github.com/yinqiwen/gscan/blob/master/iprange.conf)
* [https://github.com/yinqiwen/gscan/blob/master/example/iprange.conf](https://github.com/yinqiwen/gscan/blob/master/example/iprange.conf)
* [https://github.com/yinqiwen/gscan/blob/master/example/huge_iprange.conf](https://github.com/yinqiwen/gscan/blob/master/example/huge_iprange.conf)

另补了一些根据ASN反查得来的Google/Youtube IP段，全部转成了CIDR格式。
不足/24条件的也以/24处理了，故存在误差。

##建议使用[CheckGoogleIP](https://github.com/moonshawdo/checkgoogleip/)，快速且结果精准。

1、下载[CheckGoogleIP](https://github.com/moonshawdo/checkgoogleip/archive/master.zip)，解压其中的checkip.bat和checkip.py到goagent的local文件夹

2、下载[googleip.txt](https://raw.githubusercontent.com/CNMan/GoogleIPRange/master/googleip.txt)到goagent的local文件夹

3、运行checkip.bat，等待运行结束生成ip.txt，其中的IP即为筛选出的可用Google IP。

首次使用CheckGoogleIP时[checkip.py](https://github.com/moonshawdo/checkgoogleip/blob/master/checkip.py) 中参数修改建议:

* 第66行:g_maxhandleipcnt = 50 修改为9999999，否则扫到50个可用IP就自动结束了。

其他参数无需改动，ip_tmperror.txt、ip_tmpno.txt请保留，下次扫描会自动略过其中的IP，加快扫描速度。

更多说明见：[https://github.com/moonshawdo/checkgoogleip/blob/master/README.md](https://github.com/moonshawdo/checkgoogleip/blob/master/README.md)

##批量PING可用[PingInfoView](http://www.nirsoft.net/utils/multiple_ping_tool.html)。

##需要补充请直接提交[Pull Request](https://github.com/CNMan/GoogleIPRange/pulls)。
注意剔除以下保留IP地址：

```python
 0.0.0.0/8
 10.0.0.0/8
 100.64.0.0/10
 127.0.0.0/8
 169.254.0.0/16
 172.16.0.0/12
 192.0.0.0/24
 192.0.2.0/24
 192.88.99.0/24
 192.168.0.0/16
 198.18.0.0/15
 198.51.100.0/24
 203.0.113.0/24
 224.0.0.0/4
 240.0.0.0/4
 255.255.255.255/32
```

* [BandwagonHost年付3.99$：64M内存、100GB流量/月、1.5GB HDD硬盘](https://bandwagonhost.com/aff.php?aff=1366&pid=19)
* [BandwagonHost年付4.99$：96M内存、200GB流量/月、2GB HDD硬盘](https://bandwagonhost.com/aff.php?aff=1366&pid=20)
* [BandwagonHost年付5.99$：128M内存、300GB流量/月、3GB HDD硬盘](https://bandwagonhost.com/aff.php?aff=1366&pid=21)
* [BandwagonHost年付9.99$：512M内存、500GB流量/月、5GB SSD硬盘](https://bandwagonhost.com/aff.php?aff=1366&pid=22)
* [BandwagonHost年付11.99$：512M内存、1000GB流量/月、10GB SSD硬盘](https://bandwagonhost.com/aff.php?aff=1366&pid=27)
* [BandwagonHost年付18.99$：1024M内存、2000GB流量/月、20GB SSD硬盘](https://bandwagonhost.com/aff.php?aff=1366&pid=28)

##[Debian/Ubuntu VPS 安装 shadowsocks](http://goo.gl/QtpSGD)
##[Debian/Ubuntu VPS 安装 PPTP VPN](http://goo.gl/dxVBLB)
