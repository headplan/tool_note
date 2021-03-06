# PHPStrom Tips

根据Laracasts的视频记录的一些笔记.

#### 简单使用

打开工具之后的基本设置.键盘习惯, IDE皮肤, 字体颜色.

尝试打开一个项目Open.

第一个快捷键.**开启和关闭边栏 Command+1.**快捷键在第一次按下时跳转选中当前文件,之后再次按时关闭边栏.

**快速查找文件代码工具\(Navigate的前五个工具\)**

工具中会有一个"Include non-project"包含非项目的选项和文件筛选选项,还有一个展示所有匹配内容的按钮

> 快捷连续按两次会选中"Include non-project"

* Class... - Command + O - 搜索Class类名\(这里会有一些图标,例如C表示Class,I表示Interface等\)

* File... - Command + Shift + O - 搜索文件名\(这里会有一些图标,代表文件类型\)

* Symbol... - Command + Option + O - 搜索方法名\(这里会有一些图标,例如m代表方式,f代表函数等\)

快速全局搜索 - Shift+Shift

#### 隐藏IDE中的一些模块

* View中的Toolbar等等

* 隐藏编辑器顶部的面包削导航

  * 使用快捷键进入Preferences偏好设置\(Command+,\),搜索breadcrumbs\(面包削导航\),把General中的面包削去掉

  * show breadcrumbs

* 隐藏编辑器上方的Tab标签

  * 设置Tabs placement为None

#### 修改编辑器配色及字体等

使用快捷键进入Preferences偏好设置\(Command+,\),进入Editor下的Color&Font.

一般情况下会新建一个副本样式,然后在进行字体和配色的设置.

安装其他皮肤

更多配色下载地址 : [http://daylerees.github.io/](http://daylerees.github.io/)

个人使用 : [https://github.com/dracula/dracula-theme](https://github.com/dracula/dracula-theme)

```
cd ~/Library/Preferences/PhpStorm2016.3/colors
wget https://raw.githubusercontent.com/dracula/jetbrains/master/Dracula.icls
```

#### 修改边栏和编辑器底色为相同颜色

这里可以在偏好设置中设置,也可以使用快速搜索操作和配置工具 : Command + Shift + A

搜索Plugins然后回车.软化在插件中搜索Color Ide插件并安装.

重启IDE之后颜色相同了

#### 快捷键绑定

首先进入偏好设置,这里可以使用Command+,和Command + Shift + A

设置Keymap快捷键偏好.第一步还是备份.点击Copy按钮,以Default创建自己的快捷键偏好.

**快捷键组合**

* Command + Shift + O - 搜索文件名 - 改为Command + P

* Command + F12 - 文件信息列表\(方法函数列表\) - 改为Option + R

这两个快捷键的修改和重组,可以快速的打开文件并且查看文件都有哪些内容.

#### 快速创建文件

又是两个快捷键的组合

选择路径Command + ↑打开工具,按任意字符进入搜索模式,回车选择目录

Command + N打开创建文件工具,即可快速创建文件在指定的目录中.

#### 创建自定义模板文件

全局搜索快捷键 - Shift+Shift

或者使用前面学习过的快捷键搜索 - Command + Shift + A

> 这里再记录一个快捷键Command + E 打开最近编辑过的文件的列表

搜索file template回车,进入配置项File and Code Templates

点击➕或者Copy按钮,可以自定义需要的模板

导入Includes中的代码

```
#parse("Copy of PHP File Header.php")
```

创建一个自定义的模型文件

```php
# 注意,这里的php代码的变量需要转义
<?php
#parse("Copy of PHP File Header.php")

#if (${NAMESPACE})

namespace ${NAMESPACE};

#end

class ${NAME} extends Elquent
{
    protected \$fillable = [];
}
```

#### 创建代码片

进入默认配置Command + ,搜索进入Live Templates默认配置,点击右侧的➕,添加Template Group组,然后添加自定义模板,这里的模板可以选择使用快捷键Tab或者其他Space等.点击蓝色的Define或Change可以选择要做的.

模板文件里可以使用$VAR$作为变量参数,点击Edit variables还可以编辑变量的处理方式以及默认值.

#### 代码格式化\(自定义格式\)





