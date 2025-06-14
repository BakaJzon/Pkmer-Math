---
tags:
  - 数学
dlink:
  - "[[-高等数学-]]"
---
# Pkmer-Math

基于Obsidian建立公开共享的数学知识库！
PKMer知识管理交流群(QQ): 825255377
PKMer-Math开发者交流群(QQ): 782017903

## 前言

本库亦在用通俗的语言描述 梳理高等数学的主要内容, 整理为Obsidian风格的markdown文件, 内容上会使用大量Obsidian特色风格语法, 包括但不限于: 
- 使用Obsidian双链语法, 组织目录和相关内容, 构成一个Obsidian的数学知识网络.
- 使用Callout语法, 为重点内容制作简易美观的词条卡片. 
- 使用块引用语法, 引用原子化的内容组织更高层文章

**本库需要使用dataview插件**,用于浏览Home页和章节目录. 但不是必须的, 因为词条内容没有使用dataview查询. 

由于开发者精力有限, 如有内容疏漏/错误 欢迎补充和指出. 
希望共同开发的场合, 请联系开发者. 

## 内容主要来源:
1. 国内高数等主流教材
2. Wikipedia
3. ChatGPT
4. 开发者们的学识

## 其他数学库
1. ~~[基于Obsidian的新型考研数学笔记原子分子树的构建](https://www.bilibili.com/video/BV1dp4y1d7NQ)(复杂且没用)~~
2. [MathWiki](https://github.com/zhaoshenzhai/MathWiki)(非常高深)
3. [09-22年考研数学一真题](https://www.bilibili.com/video/BV1ta4y1Q75u)(没什么好说的)
4. [数学 (insile.github.io)](https://insile.github.io/my-notes/%E7%AC%94%E8%AE%B0/%E5%BD%A2%E5%BC%8F%E7%A7%91%E5%AD%A6/%E6%95%B0%E5%AD%A6/%E6%95%B0%E5%AD%A6)(内容较基础)
5. [OI Wiki](https://oi-wiki.org/math)(算法竞赛)
6. [香蕉空间](https://www.bananaspace.org/wiki/%E9%A6%96%E9%A1%B5)


---
# 内容
本库中的markdown文档内容按等级从上到下分为三种: 
- [[#目录]]
- [[#文档]]
- [[#词条]]

## 目录

包含章节列表的文件, 有时还会包含简要说明

总目录的导航页为[[Home]], 包含了以下目录
目录以树状图形式组织, 名称两边加上目录等级数的"-"符号
- 一级为总目录 -高等数学-
- 二级为--微积分--, --线性代数--, --概率论--等具体学科分支 
- 三级为学科分支的章节划分, 如极限, 导数与微分
- 最下级为具体的原子化词条和由其组织的文章

## 文档
为了阐述某概念而按逻辑顺序书写的文章, 有时会引用词条. 
文档的内容根据教材pdf总结

## 词条
原子化的某一概念, 使用一段话概括. **不允许使用标题**, 可以使用Callouts卡片

---
# 关于合作开发

本项目在GitHub开源，为了更好地进行和合作开发，计划在此做一些教程和规范, 目前开发原则和内容规范都在拟定中, 随时会变化, 如有更好的建议欢迎提案. 

## 开发原则
- 尽可能简洁, 让人能够快速理解重点
- 对自己写的东西的正确性负责, 多改几次也没有关系
- 奥卡姆剃刀原理：如无必要 勿增实体. 尽可能在Obsidian的原生功能基础上进行开发
- 如果是时间来不及则先将文件放到对应的一级文件夹下, 有时间再做整理

## 关于插件和配置
设计理念允许不同的配置, 以适应不同的人的使用体验. 其中有必要的相同插件, 有适应不同人群使用习惯的插件. 
### 个性化配置原则
- 推荐插件
	- dataview 只能在章节目录中使用, 同时保留手写的目录
	- Templater 方便新建笔记
	- [[#ObsidianGit]] 方便Github合作开发, 当然你也可以用vscode
- 允许使用轻量级插件(如快捷表格操作, 数学公式等)
	 - Force note view mode
	 - No more flickering inline math
 - 不推荐使用任何破坏性插件(quickadd,Linter等需要谨慎操作, 每次用完后需要关闭插件), 但如果熟悉的话,允许使用
	- Linter
	- QuickAdd
 - 知识词条页面严禁使用html, css, javascript

## 内容规范
- 所有词条都要按层级顺序添加上级目录的双链, 如:
	- 积分表属于微积分的不定积分章节, 则需要添加名为dlink的property, 类型为list, 内容为所属的最近一层目录, `dlink: [[不定积分]]`
- 最底层的内容应该尽量使用词条来原子化, 即每一个篇章都由单个最基本的概念组成, 如果需要整合多个词条内容, 需要使用内容引用语法: `![[向量]]` 
	- 词条主要内容放在开头, 不使用标题. 
	- 词条间接介绍部分使用多级标题(如性质, 推广, 例子...)
- 文档内容结构(历史内容待完善)
	- 简介: 可以引用词条, 或使用文档名作为一级标题
	- 定义: 可以引用词条
	- 推导
	- 性质
	- 例题
	- 推论
	- 应用
- 头部YAML配置项(property)
	- tags: 数学, AI(仅限gpt生成词条)
	- dlink: 双链, 记录父级目录和相关词条
	- aliases: 别名, 简写, 英语, 日语
	- chapter: 章节序号, 根据参考教材决定
	- urlink: 外部引用, 如Wikipedia
	- author: 作者, 可以是多个
	- datetime: 创建时间, 可以不写

## 准备条件
大致分为几个部分: 
1. 如果在国内需要首先解决科学问题
2. 确保你要有个GitHub账号
3. 向开发者申请权限，有权限才能提交修改
4. 安装Git命令行工具
5. 在Obsidian配置Obsidian Git插件设置
6. 从GitHub第一次拉取项目， 使用clone命令

## ObsidianGit
建议在本项目使用Obsidian第三方git插件: **Obsidian Git**
1. 在Commit Author中设置好自己的Github账号
2. `ctrl+p`输入`obsidian git open source control view` 打开Obsidian Git工具的GUI界面, 在此GUI界面点按钮就行

## 开发步骤
分为拉取同步，提交修改, 推送，冲突处理等
### 1. 拉取(Pull)
从GitHub拉取(pull)别人的修改
### 2. 提交(commit)
将你的修改提交到GitHub
### 3. 推送(Push)
本地的多个修改保存后
### 4. 冲突处理
这个比较麻烦, 日后有空再写, 简单说一下就是如果发生了冲突就是你本地文件新改动的某行和其他人新改动并提交到云端的这行不一样, 你们又都是从同一个版本衍生来的, 所以合并冲突就是你们商量怎么改动, 商量好了你先把你的改动保存下来然后放弃自己的改动, 从云端拉取他人的改动, 你在他的新改动的基础上再做修改

上述提到的**修改**指的是 文件以及文本内容的增删改, 而文本内容的增删改是以行为单位进行的




---
# 一些技术经验

## 合并分支

如果有多个分支需要合并, 以下是合并步骤:

1. 首先切换到自己主要开发的分支, 比如我在main开发, 就先切换到master
2. 执行命令 `git pull origin master` 将master合并到main (大概吧,我也没太搞懂谁合并到谁= =)
3. 解决冲突, 这个如果有的话比较麻烦, 没有就不管
4. 将合并后的内容推送到指定分支main,  `git push origin master` 

## 子模块

如果你想把Math库作为子文件夹放在自己的库中使用, 并且希望Math能够实时更新, 不影响你自己的库, 则可以创建子模块submodule
比如你的笔记目录为Note, 这个Note已经与GitHub上的仓库绑定, 你希望把Math库放到Note/Math位置并且能够实时更新, 则
### 情况一
Note库存在且已经是GitHub仓库, 本地Math库不存在
1. **添加一个新的子模块**
```shell
cd "E:\Note"
git submodule add https://github.com/PKM-er/Pkmer-Math.git Math
```
2. **初始化和更新子模块**
```shell
git submodule init
git submodule update --init
```
3. 提交更改
```shell
git add .
git commit -m "Add Math submodule"
git push
```

### 情况二
Note库还不存在, Math库已克隆至本地
上传你的 `E:\Note` 仓库到 GitHub 需要以下步骤：

1. **创建一个新的 GitHub 仓库**:
    - 登录你的 GitHub 账户。
    - 在 GitHub 的首页或仓库页面，点击“New repository”（新建仓库）。
    - 为你的仓库命名（例如 `Note`），可以选择添加描述。
    - 选择仓库的可见性（公开或私有）。
    - 点击“Create repository”（创建仓库）。
2. **连接本地仓库到 GitHub 仓库**:
    - 在创建的 GitHub 仓库页面，找到“Quick setup”区域，复制提供的 URL（HTTPS 或 SSH）。
    - 回到命令行界面，在 `E:\Note` 目录下运行以下命令，将你的本地仓库与 GitHub 仓库关联起来（这里以 HTTPS URL 为例）：
        `git remote add origin https://github.com/your-username/Note.git`
        把 `https://github.com/your-username/Note.git` 替换成你的 GitHub 仓库 URL。
3. **上传你的仓库到 GitHub**:
    - 首先，上传你的本地更改：
        `git push -u origin master`
        这个命令会将你的 `master` 分支的内容推送到 GitHub 仓库。
4. **处理子模块**:
	1. **初始化Note仓库**
	```shell
	cd "E:\Note"#改成你自己Note的路径
	git init
	```

	2. **将 Math 仓库添加为子模块**
	```shell
	git submodule add ./Math Math
	```
	这里的 `./Math` 是 `Math` 仓库的本地路径
	`Math` 是你希望在 `Note` 仓库中显示的子模块目录名
	
	3. **提交更改**
	```shell
	git add .
	git commit -m "Add Math as a submodule"
	```
	`Math` 文件夹已经被正确地添加为子模块。但是这个地址只是你本地的Math文件夹位置, 你的Note项目的GitHub端并不知道这个路径, 所以需要告诉它从哪找到这个Math项目
	
	4. 修改Math作为子模块的url
	将 `Note/.gitmodules` 文件中的 URL 改为这个地址：
	```gitmodules
	[submodule "Math"]
	 	path = Math	
	 	url = https://github.com/PKM-er/Pkmer-Math.git
	```
	这里的配置说明：
	- **[submodule "Math"]**: 表示这是一个名为 "Math" 的子模块。
	- **path = Math**: 指定了子模块在 `Note` 仓库中的相对路径，这里是 `Math` 目录。
	- **url = ./Math**: 指定了子模块的源 URL。在这个例子中，使用了相对路径 `./Math`。
	这个配置通常用于当子模块仓库位于与父仓库相同的物理位置时。
	然而，当你准备将 `Note` 仓库推送到 GitHub 时，这里可能需要更改。
	
	这样，当其他人克隆你的 `Note` 仓库并初始化子模块时，Git 会知道从哪里克隆 `Math` 子模块。
	
	5. 提交更改
	完成更改后，记得在 `Note` 仓库中提交这些更改：
	```
	git add .gitmodules git commit -m "Update Math submodule URL" git push
	```
	这会确保 `.gitmodules` 文件中的更改被推送到你的远程 `Note` 仓库。
	
	这样，`Math` 仓库就作为一个子模块被添加到了 `Note` 仓库中。你可以在 `Note` 仓库中看到一个名为 `.gitmodules` 的文件，这个文件会记录子模块的相关信息。

## .gitignore构建

由于每个人的配置都不一样, 个人可能有需要用到某些插件和主题外观, 所以如有必要请使用.gitignore根据自己的情况来配置, 如果什么额外的插件都不用, 则不用管

```.gitignore
# 首先排除自己, 因为每个人情况不一样,单独配置
.gitignore

# 同步.obsidian文件夹下指定的子文件夹, 这些插件都暂时没有用到, 将来找机会剔除
.obsidian/*
.obsidian/app.json
.obsidian/snippets
.obsidian/community-plugins.json
.obsidian/graph.json
.obsidian/bookmarks.json

.obsidian/plugins
.obsidian/plugins/*
.obsidian/plugins/dataview/
.obsidian/plugins/obsidian-git/
.obsidian/plugins/obsidian-linter/
.obsidian/plugins/quickadd/
.obsidian/plugins/obsidian-outliner/
.obsidian/plugins/table-editor-obsidian/
.obsidian/plugins/obsidian-latex-suite/
.obsidian/plugins/templater-obsidian
.obsidian/v2ray/
.obsidian/Clash/

# 其他ob相关文件夹
.history
.trash

# 针对Mac系统的忽略
.DS_Store

# 子模块相关, 暂时没有用到
.gitmodules

# vscode配置文件夹
.vscode
```
