# 公众号版本ChatGPT



![](pic/ailogo.png)

效果

![](pic/s2.jpg)







项目基于Java  + springboot + maven

1.本地运行
IDEA 打开工程，修改main-resources-application-dev.yml 下的KEY LIST， 按照实例一行一个，自动轮询 ， 
修改微信公众号配置 mp

## 公众号配置相关问题
登陆微信公众平台https://mp.weixin.qq.com

在菜单[设置与开发]-[基本配置]的服务器配置中预先填好token跟aesKey

在本项目的yml中配置好这些信息先部署到服务器上，验证本项目部署在服务器上的http://xxx.xxx.xxx.x/wx/portal/{appId} 接口能正常返回时后再填写到[服务器配置]的url输入框提交。

消息加解密方式可以先选明文模式，有需要自己再改。

运行ChatgptOnlineJavaApplication即可



1.服务器
打包
mvn package

之后将jar放服务器上，安装Java8，运行
java -jar chatgptmp.jar
即可


免费用户的KEY大概有45万汉字，120万英文可以用
APIKEY获取教程https://mp.weixin.qq.com/s/rghonm6oG7S7gNC6HzhW6A
