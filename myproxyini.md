# myproxy.ini配置文档 #
## 注：本文档只适用于greatagent1-ga，[greatagent2-ga用户请点击这里](proxymyini.md) ##

---

  * ## 功能说明 ##
    * 这个功能是提供给希望使用自己Appid以及自定义一些配置的同学使用，不受自动更新影响。
    * 本功能需要执行一次自动更新之后方可使用。
    * 本功能暂时仅支持greatagent-ga，尚且没有计划支持greatagent-wp。

---

  * ## 使用方法 ##
    1. 打开goagent-local目录，将其中的myproxy.ini.sample重命令为myproxy.ini(需要显示文件后缀名之后操作)。
    1. 参照下面文档修改配置即可。

---

  * ## 文件配置说明 ##
```
#有关于程序监听方面的配置。
[listen]
#监听ip，如果需要允许局域网/公网使用，设为0.0.0.0即可。
ip = 127.0.0.1
#使得wwqgtxx-goagent默认工作在8087端口，如有需要你可以修改成其他的  (请注意修改浏览器设置)。
port = 8087
#启动后wwqgtxx-goagent窗口是否可见，0为不可见（最小化到托盘），1为可见(不最小化到托盘)  。
visible=0
#是否显示详细debug信息，没有什么意义，不建议开启。
debuginfo = 0   

#GAE服务端的配置。
[gae]   
#是否使用你自己的APPID，设置0时使用只带公共appid。
enable = 1 
#填入你的AppID，配置多ID用|隔开。
appid = yourappid1|yourappid2|yourappid3
#密码,没有请留空。
password =   yourpassword
#服务端路径,一般不用修改,如果不懂也不要修改。
path = /2 
#是否开启防中间人攻击，开启之后会对服务器证书进行验证
validate = 0
#是否开启流量混淆
obfuscate = 0
#是否开启IPV6上网（需要你的本地网络支持）
ipv6 = 0

#代理自动配置脚本(Proxy auto-config)设定
[pac]  
#是否启用，若启用，浏览器代理自动配置地址填http://127.0.0.1:8086/proxy.pac
enable = 0 
#监听ip，如果需要允许局域网/公网使用，设为0.0.0.0即可。
ip = 127.0.0.1
#监听端口。
port = 8086
#PAC文件名
file = proxy.pac
#规则订阅地址
gfwlist = http://autoproxy-gfwlist.googlecode.com/svn/trunk/gfwlist.txt 

#二级代理，一般内网会用到，公网用户无视。
[proxy]  
#是否启用。
enable = 0 
#自动监测，不建议开启，功能并不完善，可能会引发未知问题。
autodetect = 0
#代理服务器地址。
host = 10.64.1.60  
#代理服务器端口。
port = 8080   
#代理服务器登录用户名。
username = username
#代理服务器登陆密码  。
password = 123456

#DNS模块，可以用来防止DNS劫持/污染
[dns]
enable = 0
#DNS监听地址，使用时将系统DNS设置为127.0.0.1
listen = 127.0.0.1:53
#远程DNS查询服务器
remote = 8.8.8.8
#缓存大小
cachesize = 5000
#超时时间
timeout = 2
```

---

# 请不要尝试增加本文档未提及的参数，本程序不会自动处理其他goagent参数的 #

---

### by wwqgtxx ###