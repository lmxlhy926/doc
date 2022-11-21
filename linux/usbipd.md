Convenience commands for attaching and detaching devices to Windows Subsystem for Linux

**powershell下操作**

```powershell
#查看帮助
usbipd wsl --help

#list USB devices
usbipd wsl list

#attach a usb device to a wsl instance
usbipd wsl attach --busid 4-3

#detach a usb device from a wsl instance
usbipd wsl detach --busid 4-3
```



**wsl下操作**

```
#变更权限
sudo chmod a+rw /dev/ttyUSB0
```



### 串口查询

```bash
#向串口发送数据
echo yaoxu > ttyUSB0

#查看串口输出
cat ttyUSB0

#查看串口
ls -l /dev/ttyS*

#查看串口驱动
cat /proc/tty/driver/serial

#查看串口设备
dmesg | grep ttyS*

```

