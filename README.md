## 准备工作



### 第 1 步：下载并安装 Git
[下载并安装](https://git-scm.com/download)，更多信息可参考[官方指南][git-get-start]。

### 第 2 步：安装 Node.js 和 npm
1. [下载并安装 Node.js](https://nodejs.org/en/download)
2. 打开本机的终端（命令行）工具，输入以下命令升级 npm（[官方指南含视频][npm-get-start]）：
	```shell
	sudo npm install npm -g
	```

3. 修复 npm 权限（[内含教程教程][fixing-npm-permissions]），以避免后续问题。

关于终端（命令行）工具可参考：[Mac][osx-terminal] 或 [Win][win-cmd]。

### 第 3 步：安装 Hexo CLI（命令行工具）
1. 在终端中输入以下命令安装 hexo-cli：
	```shell
	npm install -g hexo-cli
	```

2. 安装完毕后，可输入以下命令进行测试：
	```shell
	hexo -h
	```

若安装成功，会出现一组说明性文案。更多信息可参考[官方指南][hexo-doc]。

### 第 4 步：用 SourceTree 下载播客发布程序
1. [下载并安装 SourceTree](https://www.sourcetreeapp.com)
2. 按软件使用引导注册 Atlassian 帐户并登录
3. 添加自己的 GitHub 帐户
	- 点击主界面右上角齿轮图标
	- 点击 Setting… > Add Account…
	- 依提示添加 GitHub 帐户
4. 点选「Remote」面板，在「GitHub」分组下找到 `realfish/cnp-radio` 并「Clone」到本地，生成一个新的文件夹

### 第 5 步：在本地的测试 repo 中重建播客发布程序
1. 在终端中，通过 `cd` 命令进入到第 4 步所生成的文件夹
2. 输入：
	```shell
	npm install
	```

3. 待上述过程完成后，输入：
	```shell
	hexo server
	```

4. 完成后将出现提示信息 `Hexo is running at http://localhost:4000/`，在浏览器中打开 <http://localhost:4000> 即可预览（本地虚拟）网站
5. 在终端中按 `control+C` (Mac) 或 `Ctrl+C` (Win) 可关闭本地服务器，进行后续操作



* * *



## 订阅测试版播客

测试版播客网站：<http://cnp-radio.laerhsif.com/>

### Feed 地址
- 政见电台（总）：<http://cnp-radio.laerhsif.com/feed.xml>
- 政记干货大排档：<http://cnp-radio.laerhsif.com/pub/feed.xml>
- 政好读书：<http://cnp-radio.laerhsif.com/read/feed.xml>

### 订阅方法
在通用播客客户端直接添加以上各 feed 地址即可订阅。

Apple 出品的 [Podcasts][podcasts]（播客），以及 [Castro][castro]、[Overcast][overcast] 是 iOS 平台常见的播客客户端。Android 用户可在各家应用市场搜索并免费获取 [AntennaPod][antennapod]。[Pocket Casts][pocketcasts] 则广泛地支持了三大移动操作系统。



* * *



## 尝试发布新节目

1. 在第 5 步所创建的目录下，找到 `source/_posts/` 文件夹（其下分类保存的，即为各个节目的帖子）
2. 复制任一现有的 `.md` 文件（并更新文件名），用 Markdown 编辑器打开更新内容（参照既有格式）
3. 编辑并保存新帖子，完成后在终端中输入内容生成命令（generate）：
	```shell
	hexo g
	```

4. 待命令执行完毕（`public/` 目录生成），再于终端中输入内容布署命令（deploy）：
	```shell
	hexo d
	```

5. 待命令执行完毕（时长依网速而定，可看到 `INFO  Deploy done: git` 信息出现），打开[测试网站][cnp-radio]或在播客客户端中浏览测试节目更新情况

推荐 Markdown 编辑器：Mac 的 [MacDown][macdown]，Win 的 [MarkdownPad][markdownpad]。






[git-get-start]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[npm-get-start]: https://docs.npmjs.com/getting-started/installing-node
[fixing-npm-permissions]: https://docs.npmjs.com/getting-started/fixing-npm-permissions
[osx-terminal]: http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line
[win-cmd]: http://windows.microsoft.com/zh-cn/windows-vista/open-a-command-prompt-window
[hexo-doc]: https://hexo.io/docs/index.html
[podcasts]: https://itunes.apple.com/app/podcasts/id525463029
[castro]: http://castro.fm/
[overcast]: https://overcast.fm/
[antennapod]: http://antennapod.org/
[pocketcasts]: http://www.shiftyjelly.com/pocketcasts
[cnp-radio]: http://cnp-radio.laerhsif.com/
[macdown]: http://macdown.uranusjr.com/
[markdownpad]: http://markdownpad.com/
