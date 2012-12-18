autogo
======

Go语言是静态语言，修改源代码总是需要编译、运行，如果用Go做Web开发，修改一点就要编译、运行，然后才能看结果，很痛苦。
autogo就是为了让Go开发更方便。在开发阶段，做到修改之后，立马看到修改的效果，如果编译出错，能够及时显示错误信息！

使用说明
======

1、下载
将源代码git clone到任意一个位置

2、修改config/project.json文件
  该文件的作用是配置需要被autogo管理的项目，一个项目是一个json对象（{}），包括name、root和depends，
  其中depends是可选的，name是项目最终生成可执行文件的文件名（也就是main包所在的目录）；root是项目的根目录。

3、执行make(linux)/make.bat(windows)，编译autogo

4、运行autogo：bin/autogo
  注意，运行autogo时，当前目录要切换到autogo所在目录
  
注：为了方便编译出错时看到错误详细信息，当有错误时autogo会在项目中新建一个文件，将错误信息写入其中。
因此建议测阶段，在被监控的项目中加入如下一段代码：


使用的第三方库
======

为了方便，autogo中直接包含了第三方库，不需要另外下载。

1、[fsnotify](https://github.com/howeyc/fsnotify)，File system notifications

2、[simplejson](https://github.com/bitly/go-simplejson)，解析JSON，我做了一些改动

LICENCE
======

The MIT [License](https://github.com/polaris1119/autogo/master/LICENSE)
