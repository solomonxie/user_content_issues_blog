# ❖ 通过SSH Tunnel隧道端口转发 [DRAFT]

> SSH Tunnel是一个非常老的技术：只要能连接服务器的SSH，就能翻墙，就能SFTP，就能。。。各种方便，而且不用服务器额外安装任何东西

## 作为代理
> 主要用了`-D`参数的动态端口功能。

在可以连接服务器的情况下，只要简单一句话即可创建一个隧道（代理）：
```sh
$ ssh -vND localhost:2080 <user>@<IP>
```
其中：-v是输出详细信息，-N是不执行任何命令只创建和服务器的连接，-D是最重要的即创建Socks5的proxy连接。
如果需要后台执行（不用一直挂着），那就用-f参数。但是不推荐这种做法，换到后台就不容易知道当前连接状况怎么样，要知道SSH连接很难长期维持的。

创建好本地监听端口`2080`后，就像一切代理一样，直接在浏览器或者各个地方选择通过`localhost:2080`访问网络。记得选择`socks5`协议。

关闭的话，就用`ps aux | grep ssh`找到那个进程kill掉即可。

> 建议是在本机的tmux中建一个小窗口，前台执行，而不是后台执行，这样一来一往很清楚，也可控。用的时候就打开。


主要体验：
- 速度：经过最重要的网速测试：Youtube测试，我的本地连接速度3000+ k/s，几乎和Shadowsocks一样。
- 稳定性：比Shadowsocks, R2Ray等都要稳定。由于本质上就是SSH，所以掉包率不会太大。不像其它特征性强的代理容易被识别。

需要注意的有这些：
- 必须要本机开着SSH连接才行，电脑关机、睡眠等，都会断开连接。

## 作为本地映射
> 主要用了`-L`参数，把服务器的端口映射为本地的端口，直接`localhost:1234`就能访问服务器的端口。
```
-L <local-port>:<host-ip>:<host-port>
```

一般作为测试非常好用，比如我在服务器上搭建Wordpress/Jekyll/PHP等，可以把服务器上端口映射到本机来，然后访问本地的端口就能看到网页了。虽然你也可以用`服务器IP:1234`来访问同样的东西，但是在一些特殊场景里，比如有加密需求，有权限需求（不允许外部访问），这种端口转发是必要的。

案例：
服务器(192.168.1.111)上运行了Jekyll网站服务，它开启了`http://localhost:4000`作为地址，但是不允许外部访问只允许本地访问。
要想在本机访问那个网站，只能把它的端口映射到我的本机端口，这样就不会识别为外部访问了：
```sh
$ ssh -vN -L 4444:192.168.199.111:4000 pi@192.168.199.111
```
这样一来，服务器上的`4000`端口就映射为了我本机的`4444`端口，直接打开浏览器访问`localhost:4444`即可显示出Jekyll提供的网站。

## 作为远程映射
> 主要用了`-R`参数，将本地端口映射到服务器上的端口，服务器会把我的端口当成它自己的端口来访问。


## 作为内网穿透


## 作为长隧道（许多点连接）

