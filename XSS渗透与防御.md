# XSS渗透与防御

## 	1.客户端的cookie

​			**什么是cookie**：因为每个https对话都是独立的，所以为了避免重复操作，我们设计了一个代码叫做cookie。

​			**cookie是怎么产生的：**

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230312182650713.png" alt="image-20230312182650713" style="zoom:66%;" />

​			

​			**cookie的特点：**

​				1.明文 2.可修改 3.大小受限（视浏览器不同不同）

​			**cookie的用途：**

​				1.记录登录状态2.跟踪用户行为

## 2.服务器的session

​			**session是什么**：是针对每个用户的，只有客户端才能访问，程序为该客户添加一个 session。session中主要保存用户的登录信			息、操作信息等等。此 session将在用户访问结束后自动消失(如果也是超时)。

​			**session和cookie的区别：**

![image-20230313093811593](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230313093811593.png)

![image-20230313093833362](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230313093833362.png)

![image-20230313093847281](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230313093847281.png)

![image-20230313093904087](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230313093904087.png)

​			**为什么有了cookie还需要session？**

​				cookie和session是相辅相成的session的出现是为了更好的服务于cookie

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230313094349603.png" alt="image-20230313094349603" style="zoom:67%;" />



## 3.JS脚本注入

​			反射型XSS：用户输入了具有恶意的js代码。（<script>alert(1)</script>）

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230313115555697.png" alt="image-20230313115555697" style="zoom:50%;" />

​			存储型XSS:和文件绑定在数据库。

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230313115515798.png" alt="image-20230313115515798" style="zoom: 50%;" />