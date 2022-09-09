<!--
 * @Author: your name
 * @Date: 2022-3-30 14:46:09
 * @LastEditTime: 2022-05-23 22:07:18
 * @LastEditors: 关广强 ggq@jsszkd.com
 * @Description: 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
 * @FilePath: /KD-API-DOCS/public/md/api/获取场景列表.md
-->
## 基础功能
### 生命体

#### API名称：
设置2D POI二维文本
#### 功能描述：

设置底座场景中2D POI类型生命体的文本

#### 渲染示例：
![](../../image/example/设置2DPOI二维文本.webp)
#### 调用方法：

##### ES6 Modules
``` javascript
import { SceneModel } from 'kd-api/lib'

SceneModel.setSceneModelTextByUuid(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```

##### Script 标签
``` javascript
window.KdApi.SceneModel.setSceneModelTextByUuid(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```


#### 数据格式：

```javascript
let jsondata = [{
    uuid: ['xxxx_xxxx'],
    text: '江苏数字看点科技有限公司',
    style:{
        fontFamily: '微软雅⿊', // 字体
        fontSize: 14, // 字号
        fontWeight: 500, // 是否加粗
        color: [0,0,0,1] // 字体颜⾊
    }
}]
```
##### 参数描述：

| 属性      | 类型           | 是否必填 | 说明        |
|---------|--------------|------|-----------|
| uuid    | Array[String] | Y    | 生命体id    |
| text    | String        | Y    | 文本内容 |
| style    | Object        | Y    | 文本样式 |

##### style参数描述：

| 属性    | 类型            | 是否必填 | 说明        |
| ------- |---------------|------|-----------|
| fontFamily    | String | N    | 字体     |
| fontSize    | String        | N    | 字号 |
| fontWeight    | Number        | N    | 加粗 |
| color    |Array        | N    | 字体颜色：rgba |

##### 回调参数描述：
| 属性      | 类型   | 说明                     |
|---------| ------ | ------------------------ |
| list    | Array[String] | 新创建的生命体ID列表  |
