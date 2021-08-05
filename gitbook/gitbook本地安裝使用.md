# gitbook安装使用

## 1. gitbook安装

gitbook是一个基于Node.js的命令行工具，所以要先安装Node.js(下载地址：[https://nodejs.org/en/](https://links.jianshu.com/go?to=https%3A%2F%2Fnodejs.org%2Fen%2F)，找到对应平台的版本安装即可)。

Node.js都会默认安装npm（node包管理工具），所以不需要单独安装npm，打开命令行，执行以下命令安装GitBook:

```shell
npm install -g gitbook-cli
```

## 2. 编辑工具的安装

这里给大家介绍两个编辑工具：gitbook editer和typora

**gitbook editer**

这个编辑工具对新手来说是个不错的选择，它集成了gitbook，git，Markdown等功能，可以将书籍同步到gitbook.com网站和github。但是gitbook editor的注册和登录需要翻墙，而且这东西的官网进不去，所以还下不到.

**typora**

这个工具是我目前在使用的,一直都很喜欢使用这个工具

[下载地址](https://www.typora.io/)

## 3. gitbook本地使用

### 3.1 建议使用的插件

在你想要初始化的目录下，添加文件book.json

```json
{
  "plugins": [
	"summary",
	"expandable-chapters"
  ]
}
```

**使用以下命令安装**

```cmd
gitbook install # summary主要用来自动生成目录，expandable-chapters用于生成目录树
# summary 存在bug，我每次等生成之后再做一下调整
```

### 3.2 初始化工作目录

* README.md（书籍的介绍在这个文件里，在初始化钱必须有这个文件）
* SUMMARY.md（书籍的目录结构在这里配置，summary插件帮助我们生成，可以不要）

### 3.3 生成书籍记录

```shell
gitbook init
```

## 4. 常用命令

```shell
gitbook serve #将书籍生成为一个网站
gitbook install #安装插件
gitbook init #为章节设置和创建文件
```

## 5. 问题

* 使用node 14时存在问题，换成12后问题都解决了



* 参考博客
  * [gitbook安装](https://www.jianshu.com/p/0388d8bb49a7)
  * [gitbook安装报错1](https://www.cnblogs.com/cyxroot/p/13754475.html)
  * [gitbook安装报错1](https://blog.csdn.net/qq_36742720/article/details/89406212)
