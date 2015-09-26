# GreatAgent2-GA 傻瓜式教程：[https://code.google.com/p/greatagent/wiki/greatagent2ga](greatagent2ga.md) #

---

# 旧版图文教程 #
## 使用客户端 ##
  1. 下载greatagent-ga，[https://code.google.com/p/greatagent/wiki/downloads](downloads.md)，并解压
  1. 运行文件夹中的greatagent-ga.bat
    * 设置浏览器或其他需要代理的程序代理地址为127.0.0.1:8087
    * 注意：使用过程中要一直运行greatagent-ga.bat
    * 提醒：刚启动时出现网页无法显示属于正常情况，程序需要完成自动更新以及寻找配置服务端的任务，请耐心等待。
    * 代理地址127.0.0.1:8087；如需使用PAC，设置pac地址为http://127.0.0.1:8086/proxy.pac；如需配合SwitchySharp/AutoProxy等浏览器扩展（SwitchySharp用户可从local文件夹中的SwitchyOptions.bak文件导入配置）
  1. 导入证书
    * 使用管理员身份运行goagent.exe会自动向系统导入IE/Chrome的证书，你也可以双击local文件夹中的CA.crt安装证书；Firefox需要单独导入证书，打开FireFox?->选项->高级->加密->查看证书->证书机构->导入证书, 选择local\ca.crt, 勾选所有项，导入。

---

## 附：浏览器详细设置方法 ##
  1. ### IE浏览器设置 ###
    * IE有两种方式，分别为全部使用goagent代理和是pac自动代理
    * 工具->Internet选项->连接，局域网用户单击局域网设置，宽带用户选择宽带连接之后单击设置
      1. 设置代理为127.0.0.1:8087，全部使用goagent代理
> > > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/001.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/001.png)
        * 不使用时要将IE恢复无代理状态
      1. 使用PAC自动代理
> > > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/002.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/002.png)
  1. ### 谷歌chrome配合Proxy  SwitchySharp扩展 ###
    1. 安装扩展
      * 打开扩展管理页chrome://chrome/extensions/ ，将local文件夹中的SwitchySharp-0.9-beta-[r48](https://code.google.com/p/greatagent/source/detail?r=48).crx拖拽到该页面之后点击确定即可安装，扩展也可以从chrome应用商店获得[https://chrome.google.com/webstore/detail/proxy-switchysharp/dpplabbmogkhghncfbfdeeokoefdjegm](https://chrome.google.com/webstore/detail/proxy-switchysharp/dpplabbmogkhghncfbfdeeokoefdjegm)
    1. 导入设置
      * 点击 Proxy  SwitchySharp图标->选项->倒入/导出->![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/003.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/003.png)
      * 浏览到SwitchyOptions.bak，点击确定导入设置
      * 更新自动切换规则（先运行goagent再更新规则）
        * 在扩展设置页点击“切换规则”，点击“立即更新列表”，最后点击“保存”。![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/004.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/004.png)
      * 单击地址栏右侧Proxy  SwitchySharp图标即可进行模式选择
> > > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/005.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/005.png)![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/006.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/006.png)
        1. GoAgent模式  除匹配proxy.ini中sites的外，全部通过GAE
        1. GoAgent PAAS模式   无需理睬
        1. GoAgent Socks5模式   无需理睬
        1. 自动切换模式 根据切换规则自动选择是否进行代理，自动选择使用何种代理
        * 遇到规则中没有的，可以使用扩展的“新建规则”按钮自行添加
  1. ### Firefox配合FoxyProxy扩展 ###
    1. 安装扩展[https://addons.mozilla.org/zh-cn/firefox/addon/foxyproxy-standard/](https://addons.mozilla.org/zh-cn/firefox/addon/foxyproxy-standard/)
    1. 设置

> > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/007.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/007.png)
      * 右击foxyporxy图标即可选择代理模式
> > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/008.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/008.png)
  1. ### Firefox配合AutoProxy扩展 ###
    1. 安装扩展[https://addons.mozilla.org/zh-cn/firefox/addon/autoproxy/](https://addons.mozilla.org/zh-cn/firefox/addon/autoproxy/)
    1. 设置
      1. 添加代理服务器
> > > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/009.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/009.png)![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/010.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/010.png)![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/011.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/011.png)
      1. 添加规则订阅
> > > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/012.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/012.png)![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/013.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/013.png)
      1. 选择自己需要的模式
> > > > ![https://raw.github.com/greatagent/wikiphoto/master/goagent.files/014.png](https://raw.github.com/greatagent/wikiphoto/master/goagent.files/014.png)
        1. 自动模式   根据规则自行选择是否使用代理
        1. 全局模式   全部使用代理
        1. 禁用代理   全部不使用代理
    1. 或者直接使用使用已安装好autoproxy的Firefox便携版本：[下载](firefox.md)

## wwqgtxx-goagent适用环境 ##
  * 适用：浏览器，下载软件等
  * 不适用：游戏客户端等需要稳定网络的程序，QQ，tor（验证证书）。

---

# ﹡﹡﹡请勿到本页提交软件使用问题﹡﹡﹡ #
  * bug反馈等请到[issues](https://code.google.com/p/greatagent/issues/list)页提交
  * 可以在本页提出有关本wiki的建议等，请勿提交无关内容

---

### by wwqgtxx ###