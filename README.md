# [am-serv00-nezha](https://github.com/amclubs/am-serv00-nezha)
免费serv00服务器上部署nezha-dashboard哪吒面板和nezha-agent哪吒探针监控

#
▶️ **新人[YouTube](https://youtube.com/@AM_CLUB)** 需要您的支持，请务必帮我**点赞**、**关注**、**打开小铃铛**，***十分感谢！！！*** ✅
</br>🎁 不要只是下载或Fork。请 **follow** 我的[GitHub](https://github.com/amclubs)、给我所有项目一个 **Star** 星星（拜托了）！你的支持是我不断前进的动力！ 💖
</br>✅**解锁更多内容请进入 YouTube频道[【@AM_CLUB】](https://youtube.com/@AM_CLUB) 、[【个人博客】](https://am.809098.xyz)** 、TG群[【AM科技 | 分享交流群】](https://t.me/AM_CLUBS) 、获取免费节点[【进群发送关键字: 订阅】](https://t.me/AM_CLUBS)
</br>✅点击观看[免费节点教程](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbrY0Pk8gm3T7m8MZ-InquF) | [免费服务器教程](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaVlrHP9Du61CaEThYCQaiY) | [免费域名教程](https://www.youtube.com/playlist?list=PLGVQi7TjHKXZGODTvB8DEervrmHANQ1AR) | [免费VPN教程](https://www.youtube.com/playlist?list=PLGVQi7TjHKXY7V2JF-ShRSVwGANlZULdk) | [免费IPTV教程](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbkozDYVsDRJhbnNaEOC76w) | [Mac和Win工具教程](https://www.youtube.com/playlist?list=PLGVQi7TjHKXYBWu65yP8E08HxAu9LbCWm) | [AI分享教程](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaodkM-mS-2Nwggwc5wRjqY)

# 在serv00服务器上部署nezha监控

- V0演示地址：https://nezhe.amclubs.us.kg
- V0版本部署视频教程：[小白教程](https://youtu.be/vXNpooT7N-k)
- V1演示地址：https://nezha.amclubs.nyc.mn
- V1版本部署视频教程：[小白教程]( https://youtu.be/Ga2ucHxsaJM)

## 一、需要准备的前提资料
### 1、首先注册一个Serv00账号，建议使用gmail邮箱注册，注册好会有一封邮箱上面写着你注册时的用户名和密码
- 注册帐号地址：https://serv00.com
- 注册帐号请查看下面视频：<a href="https://youtu.be/NET1FTlfDTs">[点击观看视频教程]</a>

![image](https://github.com/user-attachments/assets/b3b3733b-3553-45dd-9346-c4664251755f)
  
### 2、加下群发送关键字 ssh 获取连接工具
Telegram频道：https://t.me/AM_CLUBS

## 三、安装前需准备好以下工作
- 1、登入邮件里面发你的 DevilWEB webpanel 后面的网址，进入网站后点击 Change languag 把面板改成英文
- 2、然后在左边栏点击 Additonal services ,接着点击 Run your own applications 看到一个 Enable 点击
也可以ssh连接用命令设置，设置成功要退出ssh再重新连接
```
devil binexec on
```
- 3、找到 Port reservation 点击后面的 Add Port 新开二个端口，随便写，也可以点击 Port后面的 Random随机选择Port tybe 选择 TCP
- 4、然后点击 Port list 你会看到二个端口
![image](https://github.com/user-attachments/assets/7060edbc-25f7-4add-a0fc-219a002c4048)

- 5、找到左边栏 WWW websites 点击 Add nwe websites 填写你的域名，也可以用别的域名映射到Serv00里 
![image](https://github.com/user-attachments/assets/0c40ef42-2c19-4ac2-aacf-801e39a3d3d6)

- 6、如果想用域名要解析你添加到serv00里面的A记录即可。找到 WWW websites 点击后面的 Mange SSL 就可以看到二个IP，一般添加第一个IP就可以了。
- 7、添加自己的域名开启DNS的话 在左边栏 DNS zones也可以看到A记录
- 免费us.kg域名申请教程：<a href="https://youtu.be/cI36vtXuQrM">[点击观看视频教程]</a>
- 免费dynv6域名申请教程：<a href="https://youtu.be/Nl0BV2ocYb8">[点击观看视频教程]</a>

## 四、 准备Github里面的三个东西，按照以下步骤后保存到一边
- 1、进入Gihub点击右上角头像找到 Settings 点击后往下拉找到左边栏下面的 Developer settings 点击
- 2、然后会看到三个应用点击 OAuth Apps 找到 New OAuth App点击后 按照下图所填，然后点击 Register application
![image](https://github.com/user-attachments/assets/a10dc421-7fe2-4234-a6bb-2200562a912d)

- 3、进入后会看到下图
![image](https://github.com/user-attachments/assets/5357bbeb-42d9-4cf4-89a5-8acc88e27c4e)

- 4、看到 Client ID下面的ID Client secrets 点击左边的 Generate seceet 后你会得到一个密码保存好后面会用到。
- 5、这里的Application name 可以随便写
callback URL的填成改成你的域名。
```
https://xxx.com/
```
 Authorization callback URL的代码复制下面的,记得前面的网址改成你的。
```
https://xxx.com/oauth2/callback
```
- 也可以这样输入,上面的的第2步里面的URL 也可以这样填防止登录不到面板端
```  
http://ip:9888/oauth2/callback
```

- 如果解析的域名登录不上面板记得改成 Github 的第2步 。如下图
![image](https://github.com/user-attachments/assets/8fe58fbc-e148-4190-84f2-8bc75850b412)

## 五、开始安装
- 1、用我们前面下载的工具登入SSH(有些工具 第一次连接还是会弹出输出密码记得点X 然后再添加密码 )
```
ssh <username>@<panel>.serv00.com
```

- 2、进入到面板后复制下面代码到面板安装（与 V1 版本不兼容，对应agent探针也要 V0 版本）
```
bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/install-dashboard.sh)
```

- 3、指定版本下载安装(把VERSION=自己修改对应要安装的版本号)
```
VERSION=v0.20.13 bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/install-dashboard.sh)
```

- 4、然后按照以下提升输入
  
| 变量 | 值 | 
|--------|---------|
|请输入 OAuth2 提供商(github/gitlab/jihulab/gitee，默认 github):	|回车就行
|请输入 Oauth2 应用的 Client ID	|前面页面里面保存的ID
|请输入 Oauth2 应用的 Client Secret	|右边保存的密码
|请输入 GitHub/Gitee 登录名作为管理员，多个以逗号隔开	|页面头像后面的用户名
|请输入站点标题	|随便写
|请输入站点访问端口	|前面网站设置的第一个端口
|请输入用于 Agent 接入的 RPC 端口	|第二个端口

- 5、这样我们面板端就安装好了,接着去浏览器里面输入p安装成功后输出的里面的链接如下图所示
  <img width="1497" alt="nezha" src="https://github.com/user-attachments/assets/460f08ba-4c73-49e9-a334-690012b025d3">

- 6、登入到面板端后点击右边用户名的管理后台找到设置里面的未接入CDN的面板服务器域名/IP
  
  <img width="1260" alt="nezha-1" src="https://github.com/user-attachments/assets/82767233-8010-439a-8e9d-39f26ed9f788">

填入解析的IP或者域名后保存

点击服务器新增服务器，名称随便填点击下面的的新增

下来会看到一个服务器后面的密钥下面我们会用到

<img width="1223" alt="serv00-3" src="https://github.com/user-attachments/assets/8a430a9d-3d55-47d7-846d-6eb5a8caca1a">

- 7、dashboard保活

保活视频教程：[点击观看](https://youtu.be/zkGGklEaO2I?si=Ssqkk2fUM6fif8tO)

- 8、dashboard卸载命令(卸载完就执行第3步的安装命令重新安装)
```
pgrep -f 'dashboard' | xargs -r kill
rm -rf ~/.nezha-dashboard
```

--------------------------------------------------------------------------------------------------------
- 9、V1 版本面板安装（与 V0 版本不兼容，对应agent探针也要V1版本）
```
bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/install-dashboard-v1.sh)
```
- 4、指定版本下载安装(把VERSION=自己修改对应要安装的版本号)
```
VERSION=v1.5.1 bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/install-dashboard-v1.sh)
```


## 六、把serv00服务器添加到nezha上面(其它要监控和多台服务器都是此命令安装就可以)
- 1、安装命令 V0版本 （与 V1 版本不兼容，对应面板也要V0版本）
```
bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/install-agent.sh)
```
- 2、指定版本下载安装(把VERSION=自己修改对应要安装的版本号)
```
VERSION=v0.20.5 bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/install-agent.sh)
```

- 根据提示填写以下内容   
| 变量 | 值 | 
|--------|---------|
|请输入 Dashboard 站点地址	|解析的IP或者域名
|请输入面板 RPC 端口：	|第二个端口
|请输入 Agent 密钥	|面板服务器后面的密钥(面板新加的服务器配置)

- 2、接下来直接回车就行了。然后我们去到网址点击服务器前面的图像就会看到我们的服务器在线了。
<img width="959" alt="serv00-4" src="https://github.com/user-attachments/assets/693d4297-b777-41b8-9f66-2323edecca0b">
<img width="1239" alt="serv00-5" src="https://github.com/user-attachments/assets/289746b1-5bbf-494a-b38a-72329a104195">

- 3、agent保活命令
```
  (crontab -l; echo "*/12 * * * * pgrep -x "nezha-agent" > /dev/null || nohup /home/${USER}/nezha-agent/start.sh >/dev/null 2>&1 &") | crontab -
```
重启
```
bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/am_restart_dashboard.sh)
```

- 4、agent卸载命令(卸载完就执行第1步的安装命令重新安装)
```
pgrep -f 'nezha-agent' | xargs -r kill
rm -rf ~/.nezha-agent
```

--------------------------------------------------------------------------------------------------------
- 5、V1 版本面板安装（与 V0 版本不兼容，对应面板也要V1版本）
```
bash <(curl -s https://raw.githubusercontent.com/lg-yyds/am-serv00-nezha/refs/heads/main/install-agent-v1.sh)
```
- 6、指定版本下载安装(把VERSION=自己修改对应要安装的版本号)
```
VERSION=v1.5.1 bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/install-agent-v1.sh)
```
重启
```
bash <(curl -s https://raw.githubusercontent.com/amclubs/am-serv00-nezha/main/am_restart_agent.sh)
```

## 备注
保活和重启项目教程：https://github.com/amclubs/am-serv00-github-action
保活视频教程：[点击观看](https://youtu.be/zkGGklEaO2I?si=Ssqkk2fUM6fif8tO)

# 
 <center><details><summary><strong> [点击展开] 赞赏支持 ~🧧</strong></summary>
 *我非常感谢您的赞赏和支持，它们将极大地激励我继续创新，持续产生有价值的工作。*
  
 - **USDT-TRC20:** `TWTxUyay6QJN3K4fs4kvJTT8Zfa2mWTwDD`
  
 </details></center>

#
 免责声明:
 - 1、该项目设计和开发仅供学习、研究和安全测试目的。请于下载后 24 小时内删除, 不得用作任何商业用途, 文字、数据及图片均有所属版权, 如转载须注明来源。
 - 2、使用本程序必循遵守部署服务器所在地区的法律、所在国家和用户所在国家的法律法规。对任何人或团体使用该项目时产生的任何后果由使用者承担。
 - 3、作者不对使用该项目可能引起的任何直接或间接损害负责。作者保留随时更新本免责声明的权利，且不另行通知。
 
