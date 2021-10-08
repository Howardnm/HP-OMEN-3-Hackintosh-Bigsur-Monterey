## 二、前置
### 1、准备U盘固件写入 | Write in
- 将准备好的U盘插入电脑，然后打开TransMac

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633671474274.png)
![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633671488864.png)
- 选择你下载好的DMG镜像，进行刷写

### 2、硬盘分区 | Partition the hard disk
- 打开DiskGenius，选择自己想要安装Mac OS的硬盘，这里我随便演示
- 点击拆分分区，大小自己调整

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633671657649.png)
![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633671667834.png)
- 选择刚拆分的新建分区，选择APFS格式，确定

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633671824586.png)

### 3、修改BIOS选项 | Configured BIOS options
- 将电脑重启，点击重启后，反复点击键盘上的F10，直到进入BIOS

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633671935308.png)
- 选择 “安全启动模式”，将它禁用，按F10保存

## 三、安装 macOS Big Sur| Install macOS Big Sur
- 插入u盘开机，反复按F9后，会进入UEFI界面，选择我们的U盘然后进入引导界面，选择“install macOS bigsur”，回车进入

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672144892.png)
- 接下来跑一堆代码（约等待5分钟）
- 选择 磁盘工具，点击右下角的 “继续”

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672203116.png)
- 选中我们刚刚分的区，点右上角“分区”

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672218893.png)
- 选择格式为apfs，名称自己命名

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672264588.png)
![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672293638.png)
- 返回首页点击安装，安装完后会自动重启

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672364152.png)
- 这期间电脑会反复重启多次，每次重启都要按F9选择u盘启动，这里进入clover引导界面只需按ENTER（即选择刚刚命名的分区盘）其它的按键不要动，等待代码自动跑完
- 跑完后会出现以下注册页面，证明安装成功了

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672481775.png)

## 四、覆盖适合的EFI | Overwrite EFI
- 重新开机进入到win界面，打开DiskGenius，选择你安装黑苹果的硬盘打开ESP分区下的EFI文件夹

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672626713.png)
- 接着将你下载解压好的EFI文件夹里面的所有文件移动到此处
- 选择全部替换，之后重启就可以进入我们的黑苹果了

![file](http://howard115.synology.me:520/wp-content/uploads/2021/10/image-1633672639575.png)

### *至此，黑苹果安装步骤全部完成。*