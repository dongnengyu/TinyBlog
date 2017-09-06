#### 折腾理由：因为我的学校的ipv6是免费用的，所以想在路由器上面搭建一个softether客户端来代替我的电脑，让路由器去连接我在搬瓦工买的vps上面的softether服务端，这样就能既有翻墙wifi又不需要电脑拨号了

	1. 准备工作：一个芯片最好是ar71xx（兼容性较好）的openwrt路由器（闪存与内存足够大，推荐网件3800）
	2. 准备好softether的依赖环境（依赖包可在openwrt官网下载）
	3. ssh软件以及scp软件（推荐putty和winscp）
	4.  开始：
		* softether不完全依赖包 (实际情况下有可能比这里少也有可能比这里多)
		* 上面图片里的softethervpn.ipk 是自己编译的，如有需要欢迎联系我
		* 使用winscp软件将ipk文件传输到路由器的tmp文件夹
		* 使用putty命令行进行ipk文件的安装
		* 安装完了之后，主要会有以下三条命令行：
			* /usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpnserver start  (启动服务端)
			* /usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpnclient start  (启动客户端)
			* /usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpncmd  (启动cmd)
本文未完，等我有空再补坑。(〃'▽'〃)

2017年08月31日前来填坑

 关于路由器如何获取ipv6的方法，本人使用的是6relay，虽然现在已经被openwrt官方抛弃了，但是依然能较好的满足需求，ps，官方的ipv6真的是狗屎~~
 	1. 配置服务端：
	 	1. 1. /usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpnserver start  (启动服务端)
	 	2. 运行上面那条启动服务端的命令之后，其实就可以在电脑上操作了，在softether服务器管理软件界面上输入路由器的ip地址即可，
	 	3. 没错。配置服务器并不需要在路由器里苦苦输入命令行了！！！！不过配置客户端就悲催了，gg。
	 	4.  至于怎么在管理软件上配置服务端，鉴于篇幅太长，建议Google一下，网上的前辈已经积累了足够多的经验了。ps：英文版教程更为详细
 	2. 配置客户端：
	 	1. 我曹这是我遇到的一个大坑，
	 	2. /usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpnclient start  (启动客户端)
	 	3. /usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpncmd  (启动cmd)，然后你就会进入softether的命令行管理界面
	 	4. 运行完之后，你就可以输入help来仔细学习了，里面好像有多达几十条命令，一个个查字典应该能翻译出来，233.
	 	5. 在路由器上配置softether客户端刚开始的时候是肥肠苦逼的，不过熟练之后就很简单了。建议自己摸索摸索！
	 	6. （有可能以后会填坑，把配置客户端的知识补充出来，当时这个操作坑了我一个星期的空闲时间，说明还是自己技术不行啊！！）
