## 基础功能
### 生命体

#### API名称：
通过标签设置3D POI特效
#### 功能描述：

设置标签绑定的3D POI类型生命体样式；不存在不同类tag的生命体

#### 渲染示例：

#### 调用方法：

##### ES6 Modules
``` javascript
import { SceneModel } from 'kd-api/lib'

SceneModel.set3DPOIEffectsByTag(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```

##### Script 标签
``` javascript
window.KdApi.SceneModel.set3DPOIEffectsByTag(jsondata)
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
    asset_uuid: 'type_xxxx',
    color: [0,0,0,1],
    animate_speed: 1,
    scale_double: 1
}
```
##### 参数描述：

| 属性      | 类型     | 是否必填 | 说明     |
|---------|--------|------|--------|
| uuid   | String[] | Y    | 3D POI UUID |
| asset_uuid | String      | Y    | 资产库特效ID   |
| color | Number[]      | Y    | 特效颜色：RGBA   |
| animate_speed | Number      | Y    | 动画播放速度   |
| scale_double | Number      | Y    | 特效缩放   |

##### 回调参数描述：
| 属性      | 类型   | 说明                     |
|---------| ------ | ------------------------ |
| code    | Number | 200: 成功,500：失败  |
| message | String | 成功或者失败原因  |
