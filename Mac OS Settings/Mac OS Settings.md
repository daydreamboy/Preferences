# Mac OS Settings

[TOC]

## 1、显示所有隐藏文件[^1]

```shell
$ defaults write com.apple.finder AppleShowAllFiles -boolean true; killall Finder
```



## 2、允许安装不明身份软件

```shell
$ sudo spctl --master-disable
```



在Security&Privacy面板

![](images/1.png)



## 3、文件的@属性



### （1）查看@属性

```shell
$ ls -l@
```



### （2）移除@属性

```shell
$ xattr -c <file>
```



## 4、禁用System Integrity Protection



- 重启macOS，屏幕变黑时，按住⌘+R直到出现Logo
- Utilities -> Terminal，输入csrutil disable; reboot



## 5、修复系统屏幕截图不保存到桌面的问题[^3]



![](images/2.png)



命令行执行下面命令

```shell
defaults write com.apple.screencapture location ~/Desktop
defaults write com.apple.screencapture target file
killall SystemUIServer
```



## 6、制作Finder中文件夹或文件的右键菜单[^4]



* Open Applications -> Automator
* File -> New in the menu bar
* Chose a document type of Service



```shell
$ brew install p7zip
```



TODO





## References

[^1]:https://apple.stackexchange.com/questions/340542/show-hidden-files-on-mac-os-x-mojave-using-terminal

[^2]:https://stackoverflow.com/questions/4833052/how-do-i-remove-the-extended-attributes-on-a-file-in-mac-os-x

[^3]:https://apple.stackexchange.com/a/348043

[^4]:https://davidwalsh.name/mac-context-menu



