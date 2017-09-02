### 安装本地 Jekyll 环境
 1. 安装 ruby
 	- 查看当前 ruby 版本 `$ ruby -v`
 	- 如果版本高于 **2.2.0**，可以跳过这一步；低于所需版本使用 rvm 升级，[rvm 升级 ruby ](http://www.jianshu.com/p/8b13987f392a)
 2. 安装 Jekyll
  	- [Jekyll 中文文档](http://jekyllcn.com/docs/quickstart/)
  	- 按照文档完成后，使用 `$ jekyll s` 启动成功就可以在浏览器中输入 `http://127.0.0.1:4000` 看到效果了
 3. 问题处理
 	- 安装包下载慢或无法下载，尝试科学上网或更换镜像源。查看当前镜像`$ gem source`
 	- 权限问题，在命令前加 `sudo` 解决
 	-  ` bundle: command not found` 问题，使用 `sudo gem install bundle` 解决
 	-  mac 升级 10.11 后，会出现的 xcrun: error: invalid active developer path, missing xcrun 错误
[参考解决方案](http://elfxp.com/mac-xcrun-error/)


### 模板使用

	**文件名不能包含中文**

	**每篇文章 category 使用英文**
1. 主要结构

 - _posts 文件夹下放 *.md 文章， 文件名

	 - 必须使用日期格式`YYYY-MM-DD`开头
	 `2017-06-21-sharing-cx.md`
	 - 不能保含 `/` `.`

 - _data 文件夹存放每篇文章对应的数据， 文件名

	 - 必须为英文
	 - 格式：分类名（英文，与文章 .md 文件头信息 category 字段相同）+ 文章名（日期开头）
	 `category-2017-06-21-sharing-cx.yml`


2. 数据文件(*.yml)规范：

- includeType 指定使用的模板，禁止修改；其它字段数据可以按需要编辑

- 缩进最好使用两个空格，禁用 tab

- 包含特殊字符的文本使用 单引号`''` 或 双引号 `""` 包围，如 `'[美] 威廉厄姆'`


### DEMO:
 - [demo.md](https://github.com/iBrainBaby/Age-template/blob/master/_posts/2017-08-19-demo.md)
 - [demo.yml](https://github.com/iBrainBaby/Age-template/blob/master/_data/example-2017-08-19-demo.yml)



#### TODO: 模板字数限制