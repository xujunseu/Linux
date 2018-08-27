安装python2： 

```
sudo apt-get install python
```
安装python3： 

```
sudo apt-get install python3（只安装了python3.4，可以用sudo apt-get install python3.5升级到python3.5）
```

卸载python2： 

```
sudo apt autoremove
```

卸载python3： 

```
sudo apt-get remove python3
```

**Ubuntu下安装Tensorflow(CPU)（原生pip安装）**

* 1.确定python3已经在Ubuntu中安装 

* 2.安装pip3： sudo apt-get install python3-pip

* 3.安装TensorFlow： pip3 install tensorflow

**Ubuntu下如何安装keras**

1）先按照上述方法安装Tensorflow

2）然后使用sudo pip3 install keras

注意：以上所有安装都是基于python3

**Ubuntu下如何在pycharm中导入tensorflow**

按照tensorflow的官方文档安装完成tensorflow之后可以再终端（Terminal）下激活python环境并使用，但是当你在pycharm下import tensorflow的时候却会发现报错no this module，以下是解决方案：
其实无法在pycharm下导入tensorflow的原因是你是将tensorflow安装在了你终端默认的python路径下，而当你使用pycharm创建一个项目时它会默认给你新建一个python虚拟环境，而不会去使用你本地默认的（这就是为什么在终端下可以import tensorflow而在pycharm中却报错的原因），所以解决这个问题的方法就是在你pycharm的项目中将python环境和你终端默认的python环境设置为同一个。

步骤：

1）which python3查看终端默认的python3环境；

2） File–>setting–>Project:**–>Project Interpreter ，然后在选择框中选中你终端下查询出来的那一个python路径即可。

可能遇到的问题：  在Project Interpreter中选中正确的Python环境后可能会报如下错误： pycharm please specify a different SDK name

这个的原因是你当前列表存在与你选中的python环境重名的python环境（一般是你pycharm之前项目建立的python环境），解决方法是删除列表里现有的python环境，直接show all,，然后点击“-”删除就好，删除后再添加你的本地python环境即可import成功。
