# ❖ Linux命令下 通过代理连接网络 [DRAFT]

> 没有（或者非常困难）什么方法能在终端里全局走代理的。

[参考：Mac OSX终端走shadowsocks代理](https://github.com/mrdulin/blog/issues/18)

Mac或Linux下，在`~/.bash_profile`或`~/.zshrc`中（根据你的shell而定），加入以下设定：
```
alias proxy='export all_proxy=socks5://127.0.0.1:1080'
alias unproxy='unset all_proxy'
```
这样做的好处是，只有你需要的时候，输入`proxy`，才会开始走代理。
以上的代理ip和端口，根据你自己的http代理设置。

这个方法适用的只有curl, wget这种builtin程序，其它程序的话都会根据自身的设计而各不相同。


## apt走代理

[参考：Configure proxy for APT?](https://askubuntu.com/questions/257290/configure-proxy-for-apt)


编辑（或新建）`/etc/apt/apt.conf`，并加入如下代理设置：
```
Acquire::http::Proxy "http://USERNAME:PASSWORD@SERVER:PORT";
Acquire::https::Proxy "https://USERNAME:PASSWORD@SERVER:PORT";

# 如
Acquire::http::Proxy "http://127.0.0.1:1080";
Acquire::https::Proxy "https://127.0.0.1:1080";
```

但是，
> 亲测，本机用的Shadowsocks，开放1080端口，可以用作curl代理，但是在执行`apt-get update`时，卡住不能更新。

![image](https://user-images.githubusercontent.com/14041622/45930417-a2aa4b80-bf92-11e8-8641-63679720ee19.png)

