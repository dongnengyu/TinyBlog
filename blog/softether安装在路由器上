# 折腾理由：因为我的学校的ipv6是免费用的，所以想在路由器上面搭建一个softether客户端来代替我的电脑，让路由器去连接我在搬瓦工买的vps上面的softether服务端，这样就能既有翻墙wifi又不需要电脑拨号了
<ul>
 	<li><strong>准备工作：</strong>- 一个芯片最好是ar71xx（兼容性较好）的openwrt路由器（闪存与内存足够大，推荐网件3800）
- 准备好softether的依赖环境（依赖包可在openwrt官网下载）
- ssh软件以及scp软件（推荐putty和winscp）</li>
 	<li><strong>开始：</strong>
<ol>
 	<li>softether不完全依赖包 (实际情况下有可能比这里少也有可能比这里多)
<ol>
 	<li><img class="alignnone size-medium wp-image-30" src="http://dongnengyu.com/wp-content/uploads/2017/05/1-300x150.png" alt="" width="300" height="150" /></li>
</ol>
</li>
 	<li>上面图片里的softethervpn.ipk 是自己编译的，如有需要欢迎联系我</li>
 	<li>使用winscp软件将ipk文件传输到路由器的tmp文件夹</li>
 	<li>使用putty命令行进行ipk文件的安装</li>
 	<li>安装完了之后：</li>
 	<li>主要会有以下三条命令行：
/usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpnserver start  (启动服务端)
/usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpnclient start  (启动客户端)
/usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpncmd  (启动cmd)</li>
</ol>
</li>
 	<li>本文未完，等我有空再补坑。(〃'▽'〃)</li>
</ul>
&nbsp;
<ul>
 	<li>2017年08月31日前来填坑
<ul>
 	<li>关于路由器如何获取ipv6的方法，本人使用的是6relay，虽然现在已经被openwrt官方抛弃了，但是依然能较好的满足需求，ps，官方的ipv6真的事狗屎~~</li>
 	<li>配置服务端：
<ul>
 	<li>运行上面那条启动服务端的命令之后，其实就可以在电脑上操作了，在<strong>softether服务器管理软件</strong>界面上输入路由器的ip地址即可，没错。配置服务器并不需要在路由器里苦苦输入命令行了！！！！不过配置客户端就悲催了，gg，</li>
 	<li>至于怎么在管理软件上配置服务端，鉴于篇幅太长，建议Google一下，网上的前辈已经积累了足够多的经验了。ps：英文版教程更为详细</li>
</ul>
</li>
 	<li>配置客户端：
<ul>
 	<li>我曹这是我遇到的一个大坑，</li>
 	<li>/usr/bin/env LANG=en_US.UTF-8 /usr/bin/vpncmd  (启动cmd)</li>
 	<li>先运行这条代码，然后你就会进入softether的命令行管理界面，（好像进去之前是要先开softether客户端来着，时间过了太长忘了）</li>
 	<li>运行完之后，你就可以输入help来仔细学习了，里面好像有多达几十条命令，一个个查字典应该能翻译出来，233.</li>
 	<li>在路由器上配置softether客户端刚开始的时候是肥肠苦逼的，不过熟练之后就很简单了。建议自己摸索摸索！
<ul>
 	<li><img class="alignnone size-medium wp-image-71" src="http://dongnengyu.com/wp-content/uploads/2017/08/Snip20170901_6-300x186.png" alt="" width="300" height="186" /></li>
</ul>
</li>
 	<li>黄色圈圈的是要手动新建一个接口的
<ul>
 	<li><img class="alignnone size-medium wp-image-72" src="http://dongnengyu.com/wp-content/uploads/2017/08/Snip20170901_7-300x176.png" alt="" width="300" height="176" /></li>
</ul>
</li>
</ul>
</li>
</ul>
</li>
</ul>
