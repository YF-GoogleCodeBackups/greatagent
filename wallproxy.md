# GreatAgent2-WP 傻瓜式教程：[https://code.google.com/p/greatagent/wiki/greatagent2wp](greatagent2wp.md) #

---

# 旧版图文教程 #


---

## 第一步：下载greatagent-wp ##
## 使用客户端 ##
  1. 下载greatagent-wp，[https://code.google.com/p/greatagent/wiki/downloads](downloads.md)，并解压
  1. 运行文件夹中的greatagent-wp.bat
    * 设置浏览器或其他需要代理的程序代理地址为127.0.0.1:8087
    * 注意：使用过程中要一直运行greatagent-wp.bat
  1. 代理地址127.0.0.1:8087；如需使用PAC，设置http://127.0.0.1:8087/proxy.pac；如需使用`SwitchySharp/AutoProxy`等浏览器扩展（`SwitchySharp用户可导入配置local\misc\SwitchyOptions.bak`），见图文教程（GUI应该选择“禁用切换”）；如需使用智能代理（使无法使用PAC或扩展的程序也做到该走代理走代理，不该走就不走），设置127.0.0.1:8086为代理即可。
  1. 导入http://127.0.0.1:8086/CA.crt为浏览器根证书可消除浏览器证书警告（cmd窗口提示时间与导入后查看到的时间相同基本就是导入成功了，升级版本时请保留cert目录，以免需要再次导入）
  1. 可通过http://127.0.0.1:8086或http://wallproxy访问Web配置界面

## 第二步：运行客户端 ##
  1. 运行local文件夹下`greatagent-wp.bat`，完成自动更新后可显示下图
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image011.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image011.png)
> > 双击托盘图标，可出现控制台窗口
  1. 托盘左键菜单用于配置代理，右键菜单配置程序。
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image013.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image013.png)
    1. 直接连接：强制浏览器不使用代理；
    1. GAE代理：强制浏览器使用127.0.0.1:8087作为代理（除部分google网站外，大部分网站都走GAE）；
    1. 智能代理：强制浏览器使用127.0.0.1:8086作为代理，由wallproxy智能判断是否需要走GAE，如果直连失败，可自动改走GAE；
    1. 自动代理：由浏览器通过PAC判断是否需要走GAE，与智能代理相比性能损失小，但无法做到在直连失败时改走GAE；
    1. 禁用切换：强制IE不使用代理；以上4个选择在每次运行`WallProxy.exe`时都会去修改IE代理为所选择项，而选择“禁用切换”后下次运行不会对IE代理做任何修改。**使用`SwitchySharp/AutoProxy`等浏览器扩展管理代理的用户，请选择此项** 。
  1. 如果需要自定义这些菜单，可以选择“设置代理”菜单项：
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image014.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image014.png)
> > 勾选“退出时恢复无代理”可在退出`WallProxy.exe`时将IE代理修改为无代理，以免影响正常使用；勾选“禁用代理切换”效果类似于“禁用切换”菜单。
> > 如果使用如图所示的拨号上网方式，将连接名称填入上图“连接名称”，例如下图“连接 宽带连接”，将“宽带连接”填入即可。
> > > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image015.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image015.jpg)
  1. 打开浏览器输入：http://www.facebook.com，并成功访问。

> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image016.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image016.jpg)
  1. 自定义代理规则，访问http://wallproxy/或者http://127.0.0.1:8086/，再点击“自定义规则”，输入要走GAE的规则后保存即可：
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image017.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image017.jpg)
## 附录 ##
### 附录一：浏览器简便设置方法 ###
  1. 直接下载[wwqgtxx-wallproxy-Release-withFirefox版本](https://code.google.com/p/wwqgtxx-goagent/wiki/downloads?tm=2)，打开不用配置，可以直接使用

### 附录二：`Firefox + WallProxy` ###
  1. 使用系统代理
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image019.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image019.jpg)
  1. 导入根证书
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image020.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image020.jpg)
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image021.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image021.png)
  1. 检查导入是否正确（可选），时间相同，说明没有导错：
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image022.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image022.jpg)
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image023.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image023.jpg)

### 附录三：配合`Chrome + SwitchySharp`使用方法 ###

> [.md](.md)**GUI左键菜单选择“禁用切换”** ，按下图导入配置，之后“直接连接”、“GAE代理”、“智能代理”、“自动代理”作用与`WallProxy.exe`相同。
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image024.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image024.jpg)
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image025.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image025.png)

### 附录四：配合`Firefox + FoxyProxy`使用方法 ###

> [.md](.md)**GUI左键菜单选择“禁用切换”** ，如图所示依次添加“GAE代理”127.0.0.1:8087，“智能代理”127.0.0.1:8086，“自动代理”http://127.0.0.1:8087/proxy.pac。
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image026.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image026.jpg)
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image027.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image027.jpg)
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image028.jpg](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image028.jpg)

### 附录五：配合`Firefox + AutoProxy`使用方法 ###

> [.md](.md)**GUI左键菜单选择“禁用切换”** ，相比之下`AutoProxy`是比个强大的代理扩展，如果找不到以下对话框从哪些菜单找出来，还是改用配置好的[firefox](https://code.google.com/p/greatagent/wiki/firefox)吧。
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image029.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image029.png)
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image030.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image030.png)
> > ![https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image031.png](https://raw.github.com/greatagent/wikiphoto/master/wallproxy.files/image031.png)


---

### by wwqgtxx ###