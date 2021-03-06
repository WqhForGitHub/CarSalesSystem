# 汽车销售平台
这是一个基于java web搭建的汽车销售的交易平台,用户可以进行登录之后即可选择自己的喜欢的车型进行购买。        
管理员登录可以进行对整个车行销售情况的查看,包括对用户、车类型、车辆、订单进行管理。   
# 项目截图
### 首页概览
![HomePage](http://pdi3m4use.bkt.clouddn.com/Home1png.png)
![HomePage1](http://pdi3m4use.bkt.clouddn.com/listcar.png)
### 登录
![Login](http://pdi3m4use.bkt.clouddn.com/Login.png)
### 地图
![map](http://pdi3m4use.bkt.clouddn.com/map.png)
### 天气
![weather](http://pdi3m4use.bkt.clouddn.com/weather1.png)
### 购车界面
![ShopUI](http://pdi3m4use.bkt.clouddn.com/ShopUI.png)
### 订单确认
![ShopOrder](http://pdi3m4use.bkt.clouddn.com/ShopOrder.png)
### 用户管理
![usermanager](http://pdi3m4use.bkt.clouddn.com/UserManager.png)
### 车类型管理
![CarTypemanager](http://pdi3m4use.bkt.clouddn.com/CayType.png)
### 车辆管理
![Carmanager](http://pdi3m4use.bkt.clouddn.com/CarManager.png)
### 订单管理
![ordermanager](http://pdi3m4use.bkt.clouddn.com/ordermanager.png)
### 查看我的订单
![Order](http://pdi3m4use.bkt.clouddn.com/Order.png)
# 技术框架
该平台所涉及Web前端基本语法，页面的框架基本是layui和Bootstrap，适合初学Web前端用于练手的项目
* HTML/CSS/Javascript (基本语法)
* Ajax、JSON (调用API获取得到JSON数据)
* JQuery、Bootstrap (基本框架)
* layui (模块化前端框架)
# 特点
- [x] 首页、登录、注册、地图显示、天气预报
- [x] 不同车品牌的官网
- [x] 购车界面、汽车介绍、评价
- [x] 订单、我的订单
- [x] 管理员对用户、车类型、车辆、订单的管理
- [x] 用户密码修改和信息修改
# 接口说明
* 地图接口：该地图的显示是用到了高德地图JS API，使用AMap.Map类创建和展示地图对象。
* IP定位接口：该IP定位功能是调用高德地图API，通过也是Ajax的xmlHttpRequest请求，key是同样也是直接给出的，注册也是免费版本，接口同样有限制。
* 天气接口:  该天气的数据是调用和风天气API,通过是Ajax的xmlHttpRequest请求，key是直接给出的，由于注册的是免费版本，接口数据的调用次数是有限的。
# 项目总结
## 解决跨域和跨页面通信的问题
我使用的是window.postMessage函数
`Window.postMessage(message, targetOrigin, [transfer]);`
### 通信监听方法
```
window.addEventListener("message", receiveMessage, false);
function receiveMessage(event)
{
  // For Chrome, the origin property is in the event.originalEvent
  // object.
  var origin = event.origin || event.originalEvent.origin; 
  if (origin !== "http://example.org:8080")
    return;

  // ...
}
```
