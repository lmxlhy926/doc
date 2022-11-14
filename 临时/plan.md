**mqttclient:**

* 连接到mqtt服务器
* 订阅主题
* 处理订阅的主题的payload，即增加相应的处理函数
* 发布主题

**httpclient:**

* 配置方法，网址，请求头，发送体
* 发送
* 处理响应



`config.json`

```Json
{
  "server": "tcp://mqtt.mymlsoft.com:1883",
  "username": "ExampleClientSub",
  "password": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJ0YW8xLmppYW5nIiwidXNlciI6InRhb3RhbyJ9.fyndraLgsvKwBDegakaFVIfA_knGg8koAfHtTHXQMC0",
  "sn": "DCH201951420091234500004",
  "cid": "gaffic",
  "mgbus_host": "localhost",
  "mgbus_port": 8000,


  "offline": "ga/%s/off",
  "down_message": "Gaffic gate %s offline.",
  "timeout": 5000,
  "thread_cnt": 3
}
```