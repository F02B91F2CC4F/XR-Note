## 1.重启CentOS系统，到系统选择界面

<img src="image/1673244172419.png" alt="1673244172419" style="zoom:67%;" />

## 2.按下`e`键，进入Grub编辑页面

<img src="image/1673244239534.png" alt="1673244239534" style="zoom:67%;" />

## 3.往下翻，找到 **crashkernel** 字样

将 **crashkernel** 前的 ==ro== 修改为以下内容

```shell
rw init = /sysroot/bin/sh
```

<img src="image/1673244359624.png" alt="1673244359624" style="zoom:67%;" />

## 4.按下 `Ctrl+X` 启动

如果配置错误，可以按下 `Ctrl+C` 取消保存并退出

![img](image/84b24e34ec25a07f930894d3035451228c7e3f03.png@897w_117h_progressive.webp)

此时进入了emergency mode

<img src="image/d2ee4f4177a3e3f86b5ecf846971f75803d6b5a1.png@942w_240h_progressive.webp" alt="img" style="zoom: 80%;" />

## 5.修改 root 密码

```shell
# 1.切换至系统根目录
chroot /sysroot
# 2.修改密码
passwd
# 3.应用 root 密码
touch /.autorelabel
# 4.退出编辑
exit
# 5.重启系统，可能会多次重启，等待最终进入系统即可
reboot
```

<img src="image/1673244859282.png" alt="1673244859282" style="zoom:67%;" />