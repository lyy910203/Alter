
## Alter是什么?  
是一个python3开发的发送信息模块  
## Alter支持信息？  
   
* 支持非ssl和ssl的EMAIL  
    *  直接把一个markdown的文本文件拖放到当前这个页面就可以了  
    *  导出为一个html格式的文件，样式一点也不会丢失  
* 钉钉webhook机器人  
* 企业微信自定义应用  
 
### 安装  
下载Alter.py到你的项目，建议Alter.py的目录有一个__init__.py的空白文件  
### 使用  
* ##### 钉钉webhook机器人  
``` python  
import Alter
dtack = Alter.DinTalk("e897e8fec**********") #webhook地址，只需要webhook=后面的值
ret = dtack.sendmessage("13996438187","消息") #发送的用户，以及发送的消息，多用户使用"user1|user2|user3"
if ret["errcode"]:
    print("发送成功")
else:
    print(ret["errmessage"])
```
* ##### EMAIL  
``` python  
import Alter
smtp = Alter.Email("发件人账号","发件人密码",smtp = "smtp地址",smtp_port="smtp端口 int",smtp_ssl=False)#默认ssl是True
ret = smtp.sendmessage("收件人账号",'标题','内容')
if ret["errcode"]:
    print("发送成功")
else:
    print(ret["errmessage"])
```  
* ##### 企业微信自定义应用   
``` python
import Alter
corpid = "企业的ID"
secret = "自定义应用secret"
agentid = "自定义应用agentid"
webcat = Alter.WeiXin(corpid,secret,agentid)
ret = webcat.sendmessage("消息接受者（在企业微信后台查看的账号）", "发送内容")
if ret["errcode"]:
    print("发送成功")
else:
    print(ret["errmessage"])
```

## 有问题反馈  
在使用中有任何问题，欢迎反馈给我，可以用以下联系方式跟我交流  

* 邮件(351937287#qq.com, 把#换成@)  
* QQ: 351937287  


## 关于作者  

```javascript
  var ihubo = {
    nickName  : "Tommy Lin",
    site : "https://www.iyunw.cn"
  }
```
