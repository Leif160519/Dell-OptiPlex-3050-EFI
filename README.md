# 注意事项
## 1.添加下列三个参数，否则-v的时候会出现`MACH Reboot`错误
![](/Images/1.png)

![](/Images/MACH Error.jpg)
## 2.声卡的`layout-id`随便写了，因为我用的`Voodoo`万能声卡驱动，给`AppleALC`打补丁的方式是在太麻烦，不搞了（此机器的声卡为瑞昱的ALC255，有兴趣的可以自己试试打补丁）
![](/Images/Audio.png)

### 3.显卡的`id`通过查表可得`HD630`用`0x59120000`,好像也只能用这一个`id`，其他的会无限重启，与此同时，`SMBIOS`必须设置为`18.1`，否则会出现进桌面后闪屏的情况
![](/Images/Graphics.png)