



#### 1. 跑通已有key的情形下的加密解密：

* 生成一个key，加密数据，不上传
* 用这个key，解密数据

#### 上传key，再获取数据，是否需要解密？



connect_success

msg_arrived

_send_command

**mqtt_manager_add_device_key**

upload_thread



```c
typedef struct _mdevice_t{
	device_t sdev;
	char isSecrect;	//是否加密设备； 1-加密设备、 0-不加密设备
	char isOnline;	//是否上线；1-上线、0-不在线
}mdevice_t;
```



链表的作用？

```c
//mqtt_init

mqtt->recvMsg = list_create();		//订阅主题后接收到的message
mqtt->managerDevs = list_create();
mqtt->addDevs = list_create();
```



* 连接成功后操作相应的链表

**msg_arrived**：将接收到的主题，payload用`topic_and_payload_t`数据结构存储起来，然后存入链表中



**mqtt_send_command**：

* 加密数据

* 发送：

  ​	构造payload：用户名长度，用户名，加密后的数据
  ​	构造topic：依据sn
  ​	发送

**mqtt_manager_add_device_key**：

​	依据sn和新的secretkey更改设备的key。



















