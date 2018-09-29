# 服务器
* 处理浏览器请求
---
## 功能
> **httpserver**
> 1. 获取到请求
> 2. 解析请求
> 3. 将请求发送给WebFrame
> 4. 从WebFrame接收反馈数据
> 5. 将数据组织为Response格式发送给客户端
> ---
> **WebFrame**
> 1. 从httpserver接收具体请求
> 2. 根据请求进行逻辑和数据处理
> 		*静态页面
> 		*逻辑数据
> 3. 将需要的数据反馈给httpserver
>
## 目录图
'''graph
graph TD;
	project-->httpserver;
	project-->WebFrame;
	httpserver-->HttpServer.py;
	httpserver-->setting.py;
	WebFrame-->static;
	WebFrame-->views.py;
	WebFrame-->urls.py;
	WebFrame-->settings.py;
	WebFrame-->WebFrame.py
'''
