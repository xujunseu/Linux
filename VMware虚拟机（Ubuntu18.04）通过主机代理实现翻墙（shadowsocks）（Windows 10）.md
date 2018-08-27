VMware虚拟机（Ubuntu18.04）通过主机代理实现翻墙（shadowsocks）（Windows 10） 参考链接：https://www.ctolib.com/topics-114336.html

在这里，我假定大家已经在本机（Windows 10 ）上安装好了翻墙软件和虚拟机，并且能够在本机实现了翻墙。接下来我就讲解具体的配置方法：

1）虚拟机设置中网络适配器中将网络连接设置为NAT模式

2）配置主机的Shadowsocks：右键单击Shadowsocks应用图标，勾选上“允许来自局域网的连接”

3）获取本机IPv4地址：cmd中输入ipconfig

4）配置Ubuntu：在Settings->Network中设置Network Proxy

然后就可以用Chrome翻墙啦。如果想用Firefox翻墙，只需要在Firefox的Settings->General->Network Proxy->Settings中使用系统代理设置，然后选择ok即可。
