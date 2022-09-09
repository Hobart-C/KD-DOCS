
## 基础功能
### 底座事件

#### API名称：
UI跟踪事件监听

#### 功能描述：
发送需要绑定UI跟踪功能的生命体对象三维场景位置所对应的屏幕坐标信息

#### 渲染示例：

#### 调用方法：

##### ES6 Modules
``` javascript
import { EventSubscribe } from 'kd-api/lib'

EventSubscribe.UIFollowListen((res) => {
    // 当前生命体的缩放信息
    console.log(res)
})
```

##### Script 标签
``` javascript
window.KdApi.EventSubscribe.UIFollowListen((res) => {
    // 当前生命体的缩放信息
    console.log(res)
})
```

##### 回调参数描述：

| 属性      | 类型   | 说明                                   |
| --------- | ------ | -------------------------------------- |
| uuid | String | 生命体名称 |
| x | Number | video视图距离左边的边距 |
| y | Number | video视图距离下边的边距 |



