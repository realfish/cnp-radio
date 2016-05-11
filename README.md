## 准备工作
准备工作包括：安装 Git、Node.js、npm、Hexo CLI 这四个基本工具，并下载和安装政见专用的播客发布工具。

### 第 1 步：安装 Git
[下载并安装][git-download]，更多信息可参考[官方指南][git-get-start]。

### 第 2 步：安装 Node.js 和 npm
1. [下载并安装 Node.js][node-download]
2. 打开本机的终端（命令行）工具，输入以下命令升级 npm（[官方指南含视频][npm-get-start]）：
	```shell
	sudo npm install npm -g
	```

3. 修复 npm 权限（[内含教程教程][fixing-npm-permissions]）

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

### 第 4 步：用 SourceTree 下载播客发布工具
1. [下载并安装 SourceTree](https://www.sourcetreeapp.com)
2. 按软件使用引导注册 Atlassian 帐户并登录
3. 添加自己的 GitHub 帐户
	- 点击主界面右上角齿轮图标
	- 点击 Setting… > Add Account…
	- 依提示添加 GitHub 帐户
4. 点选「Remote」面板，在「GitHub」分组下找到 `realfish/cnp-radio` 并「Clone」到本地，生成一个新的文件夹

### 第 5 步：安装播客发布工具
1. 在终端中，通过 `cd` 命令进入到第 4 步所生成的文件夹
2. 输入以下命令安装：
	```shell
	npm install
	```

3. 待上述过程完成后，输入以下命令启动本地服务器：
	```shell
	hexo server
	```

4. 完成后将出现提示信息 `Hexo is running at http://localhost:4000/`，在浏览器中打开 <http://localhost:4000> 即可预览由本地服务器虚拟的网站
5. 在终端中按 Control+C (Mac) 或 Ctrl+C (Win) 可关闭本地服务器，进行后续操作



* * *



## 订阅播客

### 订阅方法
在通用播客客户端直接添加播客 feed 地址即可订阅：

- 政见电台（总）：<http://cnp-radio.laerhsif.com/feed.xml>
- 政记干货大排档：<http://cnp-radio.laerhsif.com/pub/feed.xml>
- 政好读书：<http://cnp-radio.laerhsif.com/read/feed.xml>

### 通用播客客户端
Apple 出品的 [Podcasts][podcasts]（播客），以及 [Castro][castro]、[Overcast][overcast] 是 iOS 平台常见的播客客户端。Android 用户可在各家应用市场搜索并免费获取 [AntennaPod][antennapod]。[Pocket Casts][pocketcasts] 则广泛地支持了三大移动操作系统。



* * *



## 发布新节目
发布流程为：添加新节目，**生成**可供发布的节目内容，预览（并按需修订），确认无误后**布署**。

1. 在准备工作第 4 步所创建的目录下，找到 `source/_posts/` 文件夹（其下分文件夹保存的，是各频道、各期节目的发布内容，以 `.md` 文件形式存在）
2. 复制任一 `.md` 文件（更新文件名，与节目期号一致），用 Markdown 编辑器打开并更新内容（模仿既有格式）
3. 更新后保存以上 `.md` 文件，并在终端中输入**生成**命令（generate）：
	```shell
	hexo g
	```

4. 在终端中启动本地服务器（`hexo server`），打开 <http://localhost:4000> 预览播客网站的更新情况
5. 若在预览中发现节目信息有误，可重复上述 2、3、4 项以修订
6. 确认无误后在终端内关闭本地服务器（Control+C / Ctrl+C），并输入**布署**命令（deploy）：
	```shell
	hexo d
	```

7. 待布署完毕（时长依网速而定，可看到 `INFO  Deploy done: git` 信息出现），打开[测试网站][cnp-radio]或在播客客户端中浏览测试节目更新情况

免费的 Markdown 编辑器：Mac 的 [MacDown][macdown]，Win 的 [MarkdownPad][markdownpad]。






[git-download]: https://git-scm.com/download
[git-get-start]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[node-download]: https://nodejs.org/en/download
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
