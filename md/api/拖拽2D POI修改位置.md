<!--
 * @Author: 关广强 ggq@jsszkd.com
 * @Date: 2022-05-07 14:40:32
 * @LastEditors: 关广强 ggq@jsszkd.com
 * @LastEditTime: 2022-05-07 14:41:47
 * @FilePath: \KD-API-DOCS\public\md\api\拖拽2D POI修改位置.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
## 基础功能
### 生命体

#### API名称：
拖拽2D POI修改位置
#### 功能描述：
通过拖拽动作修改2D POI屏幕位置

#### 渲染示例：

#### 调用方法：

##### ES6 Modules
``` javascript
import { SceneModel } from 'kd-api/lib'

SceneModel.change2DPOIPositionByDrag(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```

##### Script 标签
``` javascript
window.KdApi.SceneModel.change2DPOIPositionByDrag(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```


#### 数据格式：

```javascript
let jsondata = {
    uuid: ['xxxx_xxxx'],
    open: 1
}
```
##### 参数描述：

| 属性      | 类型     | 是否必填 | 说明     |
|---------|--------|------|--------|
| uuid   | String[] | Y    | 3D POI UUID |
| open | Number      | Y    | 1：开启，0：关闭   |

##### 回调参数描述：
| 属性      | 类型   | 说明                     |
|---------| ------ | ------------------------ |
| code    | Number | 200: 成功,500：失败  |
| message | String | 成功或者失败原因  |
