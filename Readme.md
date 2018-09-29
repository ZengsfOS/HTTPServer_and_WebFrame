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
```flow
st=start:Start
i=inputoutput:输入年份n
cond1=condition:n能否被4整除？
cond2=condition:n能否被100整除？
cond3=condition:n能否被400整除？
o1=inputoutput:输出非闰年
o2=inputoutput:输出非闰年
o3=inputoutput:输出闰年
o4=inputoutput:输出闰年
e=end

st-i-cond1
cond1(no)-o1-e
cond1(yes)-cond2
cond2(no)-o3-e
cond2(yes)-cond3
cond3(yes)-o2-e
cond3(no)-o4-e
```
