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



## References

[^1]:https://apple.stackexchange.com/questions/340542/show-hidden-files-on-mac-os-x-mojave-using-terminal

[^2]:https://stackoverflow.com/questions/4833052/how-do-i-remove-the-extended-attributes-on-a-file-in-mac-os-x

