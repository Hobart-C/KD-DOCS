<!--
 * @Author: 关广强 ggq@jsszkd.com
 * @Date: 2022-04-26 10:41:17
 * @LastEditors: 关广强 ggq@jsszkd.com
 * @LastEditTime: 2022-05-18 16:01:47
 * @FilePath: \KD-API-DOCS\public\md\api\添加生命体对象UI跟踪事件.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
## 基础功能
### 底座事件

#### API名称：
添加生命体对象UI跟踪事件

#### 功能描述：
将指定生命体对象加入UI跟踪事件监听列表

#### 渲染示例：
![](../../image/example/添加生命体对象UI跟踪事件.webp)
#### 调用方法：

##### ES6 Modules
``` javascript
import { SceneModel } from 'kd-api/lib'

SceneModel.setUIFollow({
   uuid: ['xxxx_xxxx']
}).then((res) => {
    // 添加成功
    console.log(res)
}).catch((err) => {
    // 添加失败
    console.log(err)
})
```

##### Script 标签
``` javascript
window.KdApi.SceneModel.setUIFollow({
   uuid: ['xxxx_xxxx']
}).then((res) => {
    // 添加成功
    console.log(res)
}).catch((err) => {
    // 添加失败
    console.log(err)
})
```

##### 参数描述：
| 属性      | 类型   | 是否必填 | 说明                                   |
| --------- | ------ |------ | -------------------------------------- |
| uuid | Array[String] | Y  | 生命体ID集合

##### 回调参数描述：

| 属性      | 类型   | 说明                                   |
| --------- | ------ | -------------------------------------- |
| code | Number | 200: 成功，500：失败|
| message | String | 成功或者失败描述 |



