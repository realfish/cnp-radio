# 使用方法



### 第 0 步：Mac 用户请先安装 Xcode
在 Mac App Store 中搜索 Xcode，安装或升级到最新版。完成后打开一次（之后可退出）。



### 第 1 步：安装 Git
- Mac 用户前往 <https://git-scm.com/download/mac> 下载
- Win 用户前往 <https://git-scm.com/download/win> 下载

如遇疑难，可参考官方教程：<https://git-scm.com/book/en/v2/Getting-Started-Installing-Git>



### 第 2 步：安装 Node.js 并升级 npm
1. 下载并安装 Node.js：<https://nodejs.org/en/download>
2. 安装完毕后，打开本机的终端（命令行）工具（[Mac][osx-terminal]/[Win][win-cmd]），输入：
	```shell
	sudo npm install npm -g
	```

3. 安装完毕 npm 后请尝试修复权限，以避免后续问题：<https://docs.npmjs.com/getting-started/fixing-npm-permissions>

[osx-terminal]: http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line
[win-cmd]: http://windows.microsoft.com/zh-cn/windows-vista/open-a-command-prompt-window

如遇疑难，可参考官方教程：<https://docs.npmjs.com/getting-started/installing-node>



### 第 3 步：安装 Hexo
在本机的终端 / 命令行工具（[Mac][osx-terminal]/[Win][win-cmd]）中，输入：
```shell
npm install -g hexo-cli
```

完成上述步骤后，可再输入：
```shell
hexo -h
```
若安装成功，则会出现一大屏的文字信息，包括一组命令说明（类似帮助文档）。

如遇疑难，可参考官方教程：<https://hexo.io/docs/index.html>



### 第 4 步：用 SourceTree 克隆（clone）测试 repo（`realfish/cnp-radio`）
1. 下载并安装 SourceTree：<https://www.sourcetreeapp.com>
2. 在 SourceTree 中添加自己的 GitHub 帐户（该帐户须成为 `realfish/cnp-radio` 这个 repo 的 collaborator）
	- 点击主界面右上角齿轮图标
	- 点击 Setting… > Add Account…
	- 依提示添加 GitHub 帐户
3. 点选「Remote」面板，在「GitHub」分组下找到 `realfish/cnp-radio` 并「Clone」（克隆）到本地



### 第 5 步：在本地安装播客发布程序
1. 在本机的终端中，通过 `cd` 命令进入到第 4 步所创建的目录
2. 输入：
	```shell
	npm install
	```

3. 待上述过程完成后，输入：
	```shell
	hexo server -s
	```

4. 完成后，理应获得 `INFO  Hexo is running at http://localhost:4000/` 的提示信息，在浏览器中输入 `http://localhost:4000/` 即可打开预览网站（本地服务器预览）
5. 预览完成后按 `Control+C`/`Ctrl+C` 则可关闭本地服务器，进行后续操作



### 第 6 步：发布帖子
1. 在第 4 步所创建的目录下，找到 `source/_posts/` 文件夹，其下分类保存的，即为各个节目的帖子
2. 用任意 Markdown 编辑器或纯文本编辑器，创建一个新的 `.md` 文件；文件命名方式和内容格式，可直接照搬现有的文件
3. 新帖子编辑 / 保存完毕后，在终端中输入
	```shell
	hexo g
	```

4. 理应看到生成了一个 `public/` 目录，然后再在终端中输入
	```shell
	hexo d
	```

5. 耐心等待一段时间（依网速而定），看到 `INFO  Deploy done: git` 信息出现后，表明布署完成
6. 打开[测试网站]，或在播客客户端中浏览测试 feed 的更新情况（更多请参见下文「播客订阅测试」）

[测试网站]: http://cnp-radio.laerhsif.com/



* * *



# 播客订阅测试

测试网站：<http://cnp-radio.laerhsif.com/>



### Feed 测试地址
- 政见电台（总）：<http://cnp-radio.laerhsif.com/feed.xml>
- 政记干货大排档：<http://cnp-radio.laerhsif.com/pub/feed.xml>
- 政好读书：<http://cnp-radio.laerhsif.com/read/feed.xml>



### 播客订阅方法

在通用播客客户端直接添加以上各 feed 地址即可订阅。

Apple 出品的 [Podcasts][podcasts]（播客），以及 [Castro][castro]、[Overcast][overcast] 是 iOS 平台常见的播客客户端。Android 用户可在各家应用市场搜索并免费获取 [AntennaPod][antennapod]。[Pocket Casts][pocketcasts] 则广泛地支持了三大移动操作系统。

[podcasts]: https://itunes.apple.com/app/podcasts/id525463029
[castro]: http://castro.fm/
[overcast]: https://overcast.fm/
[antennapod]: http://antennapod.org/
[pocketcasts]: http://www.shiftyjelly.com/pocketcasts
