# 注意事项
### 1.添加下列三个参数，否则 *`-v`* 的时候会出现 *`MACH Reboot`* 错误
![](/Images/1.png)

### 2.声卡的 *`layout-id`* 随便写了，因为我用的 *`Voodoo`* 万能声卡驱动，给 *`AppleALC`* 打补丁的方式是在太麻烦，不搞了（此机器的声卡为瑞昱的ALC255，有兴趣的可以自己试试打补丁）
![](/Images/Audio.png)

### 3.显卡的 *`id`* 通过查表可得 *`HD630`* 用 *`0x59120000`* ,好像也只能用这一个 *`id`* ，其他的会无限重启，与此同时， *`SMBIOS`* 必须设置为 *`18.1`* ，否则会出现进桌面后闪屏的情况
![](/Images/Graphics.png)
![](/Images/SMBIOS.png)

# 效果图
### 1.系统信息
![](/Images/系统信息.png)

### 2.硬件
![](/Images/硬件.png)

### 3.USB总线
![](/Images/USB总线.png)

### 4.以太网卡
![](/Images/以太网卡.png)

### 5.显卡
![](/Images/显卡.png)

### 6.音频
![](/Images/音频.png)

### 7.音频输出设备(输入设备无)
![](/Images/音频输出设备.png)

### 8.声音调节
![](/Images/声音调节.png)