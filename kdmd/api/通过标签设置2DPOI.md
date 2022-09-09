<!--
 * @Author: 关广强 ggq@jsszkd.com
 * @Date: 2022-05-07 14:43:30
 * @LastEditors: 关广强 ggq@jsszkd.com
 * @LastEditTime: 2022-05-23 22:07:50
 * @FilePath: \KD-API-DOCS\public\md\api\通过标签设置2DPOI.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
## 基础功能
### 生命体

#### API名称：
通过标签设置2D POI位置
#### 功能描述：
设置标签绑定的2D POI对象；

#### 渲染示例：

#### 调用方法：

##### ES6 Modules
``` javascript
import { SceneModel } from 'kd-api/lib'

SceneModel.set2DPOIByTag(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```

##### Script 标签
``` javascript
window.KdApi.SceneModel.set2DPOIByTag(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```


#### 数据格式：

```javascript
let jsondata = {
    uuid: 'xxxx_xxxx',
    asset_uuid: 'type_xxxx',
    text: '江苏数字看点科技有限公司',
    style: {
        fontFamily: '微软雅⿊', // 字体
        fontSize: 14, // 字号
        fontWeight: 1, // 是否加粗
        fontItalic: 1, // 是否斜体
        fontUnderline: 1, // 是否下划线
        color: [0,0,0,1]
    }

}
```
##### 参数描述：

| 属性      | 类型     | 是否必填 | 说明     |
|---------|--------|------|--------|
| uuid   | String | Y    | 标签ID |
| asset_uuid | String      | Y    | 资产ID   |
| text | String   | N    | 文本内容   |
| style | Object   | N    | 文本样式   |

##### style参数描述：

| 属性    | 类型            | 是否必填 | 说明        |
| ------- |---------------|------|-----------|
| fontFamily    | String | N    | 字体     |
| fontSize    | String        | N    | 字号 |
| fontWeight    | Number        | N    | 是否加粗,1：是，0：否 |
| fontItalic    | Number        | N    | 是否斜体,1：是，0：否 |
| fontUnderline    | Number        | N    | 是否下划线,1：是，0：否 |
| color    |Array        | N    | 字体颜色：rgba |


##### 回调参数描述：
| 属性      | 类型   | 说明                     |
|---------| ------ | ------------------------ |
| code    | Number | 200: 成功,500：失败  |
| message | String | 成功或者失败原因  |
