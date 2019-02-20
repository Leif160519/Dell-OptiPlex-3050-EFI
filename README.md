# 注意事项
### 1.本EFI-1/EFI-2适用于macOS High Sierra 10.13.6
### 2.添加下列三个参数，否则 *`-v`* 的时候会出现 *`MACH Reboot`* 错误
![](/Images/1.png)

### 3.驱动声卡
![](/Images/Audio.png)
> 声卡的 *`layout-id`* 随便写了，因为我用的 *`Voodoo`* 万能声卡驱动，给 *`AppleALC`* 打补丁的方式是在太麻烦，不搞了（此机器的声卡为瑞昱的ALC255，有兴趣的可以自己试试打补丁）


### 4.驱动显卡
#### 方法一
(EFI-1)显卡的 *`id`* 通过查表可得 *`HD630`* 用 *`0x59120000`* ,好像也只能用这一个 *`id`* ，其他的会无限重启，与此同时， *`SMBIOS`* 必须设置为 *`18.1`* ，否则会出现进桌面后闪屏的情况
![](/Images/驱动列表1.png)
![](/Images/Graphics.png)
![](/Images/SMBIOS.png)

#### 方法二
(EFI-2)显卡驱动只通过whateverGreen.kext驱动进行自动检测，配合FB-Patcher(现改名Hackintool)给显卡打补丁即可
![](/Images/驱动列表2.png)
![](/Images/General.png)
![](/Images/Patch-General.png)
![](/Images/Patch-Advanced.png)
> 注意：kext文件夹里有关显卡驱动必须全部删除，仅留下whatevergreen.kext驱动即可，另外clover中有关显卡补丁也全部删除
> FB打补丁点击Generate Patch，之后导出覆盖原先的config.plist文件即可

### 5.处理器变频
处理器变频安装完系统之后自动实现变频功能，不需要在 *`config.plist`* 中设置其他参数了

### 6.修改显示器识别
运行Tools文件夹里的MonitorFace软件之后，插拔显示器就OK了

![](/Images/MonitorFace.png)
> 这里非常感谢[lihaoyun6](https://github.com/lihaoyun6)大佬的开源项目 [macOS-Displays-icon](https://github.com/lihaoyun6/macOS-Displays-icon)

# 效果图
### 1.系统信息
![](/Images/系统信息.png)
> 显存1536MB(EFI-1)
> 
![](/Images/系统信息2.png)
> 显存2048MB(EFI-2)

### 2.显示器
![](/Images/显示器.png)
![](/Images/显示器2.png)

### 3.硬件
![](/Images/硬件.png)

### 4.USB总线
![](/Images/USB总线.png)
> 总线可能不正确，USB2.0设备无论插在2.0上还是3.0上和USB3.0设备插在2.0上都显示在3.0总线上

### 5.以太网卡
![](/Images/以太网卡.png)

### 6.显卡
![](/Images/显卡.png)

### 7.音频
![](/Images/音频.png)

### 8.音频输出设备(输入设备无)
![](/Images/音频输出设备.png)

### 9.声音调节
![](/Images/声音调节.png)

### 10.变频效果(晃动鼠标不会出现突然的高频现象)
![](/Images/变频.png)