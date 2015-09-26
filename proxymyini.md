# proxy.my.ini配置文档 #

---

  * ## 功能说明 ##
    * 这个功能是提供给希望使用自己Appid以及自定义一些配置的同学使用，不受自动更新影响。
    * 本功能需要执行一次自动更新之后方可使用。
    * 本功能暂时仅支持greatagent2-ga，不支持greatagent1-ga（[可以点击这里查看greatagent1-ga自定义文档](myproxyini.md)）或其他版本。

---

  * ## 使用方法 ##
    1. 打开goagent-local目录，将其中的proxy.my.ini.sample重命令为proxy.my.ini(需要显示文件后缀名之后操作)。
    1. 参照下面文档修改配置即可。

---

  * ## 文件配置说明 ##
```
[listen]
#监听ip，如果需要允许局域网/公网使用，设为0.0.0.0即可
ip = 127.0.0.1
#使用GAE服务端的默认8087端口，如有需要你可以修改成其他的 
port = 8087
#启动后goagent窗口是否可见，0为不可见（最小化至托盘），1为不最小化 
visible = 1
#是否显示详细debug信息
debuginfo = 0

#GAE服务端的配置
[gae]
#你的Google app engine AppID,也就是服务器部署的APPID，配置多ID用|隔开
appid = goagent
#密码,默认为空,你可以在server目录的wsgi.py设定,如果设定了,此处需要与wsgi,py保持一致
password = 123456
#服务端路径,一般不用修改,如果不懂也不要修改.
path = /2
#使用http还是https(SSL加密传输)连接至GAE
mode = https
#填ipv6则使用[ipv6/hosts][ipv6/http]，默认ipv4使用[ipv4/hosts][ipv4/http]设置
#此项设置意义与之前版本不同。非IPv6环境无需考虑，请勿随意修改
profile = ipv4
#ip评优算法每次选出的ip数量
window = 4
crlf = 1
#是否开启流量混淆
obfuscate = 0
#是否对服务器证书进行验证
validate = 0
# 如果设置为 rc4 则开启rc4加密，需在password设置密码，否则不开启，一般mode为https时无需开启
options =

#代理自动配置脚本(Proxy auto-config)设定
[pac]
#是否启用，若启用，浏览器代理自动配置地址填http://127.0.0.1:8086/proxy.pac
enable = 1
# pacserver的监听地址
ip = 127.0.0.1
port = 8086
# pac文件的名称
file = proxy.pac
#被墙规则订阅地址
gfwlist = http://autoproxy-gfwlist.googlecode.com/svn/trunk/gfwlist.txt
#广告拦截规则订阅地址
adblock = http://adblock-chinalist.googlecode.com/svn/trunk/adblock.txt
#自动更新间隔时间
expired = 86400

#二级代理，一般内网会用到，公网用户无视。
[proxy]  
#是否启用。
enable = 0 
#自动监测，不建议开启，功能并不完善，可能会引发未知问题。
autodetect = 0
#代理服务器地址
host = 10.64.1.63  
#代理服务器端口
port = 8080   
#代理服务器登录用户名
username = username
#密码  
password = 123456 

#DNS模块，可以用来防止DNS劫持/污染
[dns]
enable = 0
#DNS监听地址，使用时将系统DNS设置为127.0.0.1
listen = 127.0.0.1:53
#远程DNS查询服务器
remote = 8.8.8.8|8.8.4.4|114.114.114.114|114.114.115.115
#缓存大小
cachesize = 5000
#超时时间
timeout = 2

```

---

# 可以尝试增加本文档未提及的参数，本程序可以自动处理其他goagent参数的 #

---

### by wwqgtxx ###