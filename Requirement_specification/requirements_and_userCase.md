#### requirements


|  ID  |       requirements        |
|:--:|:--:|
|  1   |   customer enter syetem   |
|  2   |        order meal         |
|  3   |   customer manage order   |
|  4   |            pay            |
|  5   | Intellgent recommendation |
|  6   |     cook enter system     |
|  7   |    cook manager order     |


#### Use Case Diagram

![userCaseDiagram](../pic/mealUML.png)

Use Case:点餐

Actors：客人，订餐系统，支付接口

Porpose：支持用户选餐并提交订单、支付

Type：primary

Overview：顾客进入点餐系统进行点餐。

1、选择添加想要点的菜，同样的菜可以选择多次。

2、已选的菜会出现在底部的订单中（包括菜名，数量，价格和总价）

3、可以在底部订单中增加或减少每一道菜的数量。

4、点击确定按钮生成订单，弹出支付窗口。

Use Case: 管理订单  
Actors: 客人，支付网关, 订餐系统  
Porpose: 捕捉客人管理订单的过程  
Type；primary  
Overview: 一个顾客下订单后，进行支付，之后订餐系统后端接受到订单，厨师开始准备菜式。  

1.客人选好菜后，在页面上点击订单结算。  
2.客人在订单详情界面看到自己点的菜式及数量，价格，备注等信息。  
3.客人点击确认，选择支付网关。  
4.客人通过支付网关付款。  
5.订餐系统收到订单，订单详情显示在供厨师使用的后端上。  

Variation：  
2.1如果客人不想要一道菜，可以在界面上取消。其他信息也可以更改。  
4.1如果客人中途终止，则退回到订单详细页面，显示未支付。  
4.2如果支付网关异常，则退回到订单详细页面，显示未支付，并提示支付网关异常。  

Use Case: 处理订单 </br>
Actors: 厨师, 订餐系统 </br>
Porpose: 供厨师处理和管理订单 </br>
Type: primary </br>
Overview: 该界面显示用户已提交的订单,厨师完成一个订单后点击完成,后台提示用户订单已完成并传入下一个用户的菜单 </br>

1.厨师完成一个用户订单后，在页面上点击完成按钮。</br>
2.订餐系统收到完成信息,给已完成订单的用户发送消息并传入下一个订单 </br>
