### mgbus

**MgbusRequest:**

* 接收请求和响应数据（构造器）
* 产生callid
* 通知超时
* 复制数据到response中

**MgReqeustQueue：**

* 建立2张表：<callid MgbusRequest* >表，<时间点 vector(callid)>表
* 接收参数：callid, MgbusRequest*.添加条目入表
* 根据callid检索出MgbusRequest*
* 创建<时间点 vector(callid)>表，定期清理超时请求



**ChannelOperator：** 纯虚类

* 数据发送
* 数据加入队列
* 处理阻塞请求

**MgDataChannel:** 纯虚类

* 接收数据收发类（ChannelOperator）
* 发送数据函数

**SocketClient：**

* 按照给定地址，建立连接
* 开启线程池，监听创建的socket，读取接收的消息并进行处理。（开启线程池进行处理）
* 发送消息

**MgbusJsonClient:**

* 设置uri，reg，default处理函数
* 接收socket接收的消息，解析字段，调用相应的处理函数；发送数据



**MgBusHolder:**

* 包含的类：请求队列，json客户端

---

**JMqttMessageDeliver：**

* 设置topic对应的handler
* 依据给定的topic，找到相应的Handler，然后处理该topic对应的消息
* 设置sn，获取sn

**JMqttOperator:**

* 初始化Mqtt连接消息
* 订阅topic
* 发布消息
* 绑定topic-handler
* 处理订阅的消息



### gaffic:

* 设置sn
* start
* 添加主题
* （处理函数，主题，服务器地址）







```
tcp://www.park.cdhxcc.com:9532
http://localhost:8081/simple
```



```
"server": "tcp://www.park.cdhxcc.com:9532",
"username": "test",
"password": "testpass",
"cid": "gaffic",
"sn": "abcdefg",

"offline": "ga/%s/off",
"down_message": "Gaffic gate %s offline.",
"timeout": 5000,
```







纯虚函数类无法创建对象

如果类包含纯虚函数类，























