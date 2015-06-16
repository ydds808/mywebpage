#Sublime Text 3 学习笔记
![Sublime Text 3](sublime-logo.jpg)
##1.介绍
优势：拿起就能用，多点编辑，强大的包管理功能，速度快，深度可定制，快速文件切换Ctrl+P，Ctrl+Shift+P命令面板，可启用Vim模式，快捷键成标准，社区活跃。

##2.安装
[下载地址：](http://www.sublimetext.com/3)

##3.少用鼠标多用键盘
命令面板 Ctrl+Shift+P 和菜单都有快捷键提示

##4.快捷键
常用快捷键
Ctrl+N
Ctrl+Tab
Ctrl+J
Ctrl+[/]
Ctrl+l
Ctrl+c/v
Ctrl+Shift+Enter
操作粒度
Alt+方向键
Ctrl+Shift+方向键
绑定快捷键
Ctrl+`输入sublime.log_commands(True)可以看到操作的精确命令名字

##5.Package Control安装包
复制下面代码
```
import urllib.request,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```
Ctrl+` 粘贴->回车->等待提示重启软件就好
Ctrl+Shift+P 输入install回车 -> 输入你要安装的包名，等下就安装成功了

##6 快速查找文件或字符
Ctrl+P @ #
Ctrl+F 下一个：回车 上一个：Shift+回车 找到位置退出查找：Esc 多选：Ctrl+D
Ctrl+Alt+F 文件夹查找，在文件夹上右键查找F4下一个
回退到上一动作位置 Alt+-

##7.web开发者必备插件emmet
!+Tab 新建标准html文档
具体可参考[这里] (http://docs.emmet.io/cheat-sheet/)

##8. 批处理任务build
Tool->Build System->New Build System
```
{
  "cmd": ["C:\\Users\\Administrator\\AppData\\Local\\Google\\Chrome\\Application\\chrome.exe", "$file"],
  "selector": "text.html"
}
```
保存到User目录即可，以后可以用Ctrl+B预览调试
具体可参考[这里](http://sublime-text-unofficial-documentation.readthedocs.org/en/latest/reference/build_systems.html)
