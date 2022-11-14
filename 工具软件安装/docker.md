启用或关闭windows功能，勾选Hyper-V选项。

在管理员模式下的命令提示符中输入：bcdedit /set hypervisorlaunchtype Auto，然后重启电脑



```
启用或关闭windows功能，取消Hyper-V选项。
“win+ R“打开运行，输入gpedit.msc，计算机配置-管理模板-系统-device Guard-打开基于虚拟化的安全
bcdedit /set hypervisorlaunchtype off
```

