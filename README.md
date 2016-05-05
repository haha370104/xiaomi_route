# xiaomi_route
非官方小米路由器远程下载

全部封装在mi_route类中，使用范例放在最下面三行中
```python
route = mi_route('你的账号', '你的密码')
result = route.download('http://v.gorouter.info/20131204/100个梦想的赞助商（微电影）.mp4')
print(result)
```

如果print结果类似于
```json
{
  "S":"OK",
  "R":"{\"decodedUrl\":\"http://v.gorouter.info/20131204/100个梦想的赞助商（微电影）.mp4\",\"fileName\":\"100个梦想的赞助商（微电影）.mp4\"}"
}
```
则说明下载成功
python版本3.5.1，依赖requests库

PS1：因为一个账号可能对应着多个设备，所以需要在49行自己填写deviceId【抓包可得】  

PS2：26以及29两行两个参数不知道与什么相关，手上没有多个测试账号，需要用户自己抓包看  

PS3：userId其实不需要抓包看……可以从cookie中拿出来，有空再调试……
