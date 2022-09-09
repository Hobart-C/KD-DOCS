<!--
 * @Author: 关广强 ggq@jsszkd.com
 * @Date: 2022-05-17 13:55:18
 * @LastEditors: 关广强 ggq@jsszkd.com
 * @LastEditTime: 2022-05-23 22:07:25
 * @FilePath: \KD-API-DOCS\public\md\api\设置标签3DPOI生命体文本.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
## 基础功能
### 生命体

#### API名称：
设置标签3DPOI生命体文本
#### 功能描述：

设置标签3DPOI生命体文本

#### 渲染示例：
#### 调用方法：

##### ES6 Modules
``` javascript
SceneModel.set3DPoiTextByTag(jsondata)
.then((res)=>{
    // 设置标签⽣命体⽂本成功
    console.log(res)
})
.catch((err)=>{})
```

##### Script 标签
``` javascript
window.KdApi.SceneModel.set3DPoiTextByTag(jsondata)
.then((res)=>{
    // 在场景中创建⽣命体成功
    console.log(res)
})
.catch((err)=>{})
```


#### 数据格式：

```javascript
let jsondata = {
    uuid: 'tag_xxxx',
    text: '江苏数字看点科技有限公司',
    style:{
        fontFamily: '微软雅⿊', // 字体
        fontSize: 14, // 字号
        fontWeight: 1, // 是否加粗 1：是，0：否
        fontItalic: 1, // 是否斜体 1：是，0：否
        fontUnderline: 1,// 是否下划线 1：是，0：否
        color: [0,0,0,1] // 字体颜⾊
    }
}
```
##### 参数描述：

| 属性    | 类型            | 是否必填 | 说明        |
| ------- |---------------|------|-----------|
| uuid    | String | Y    | 生命体Id     |
| text    | String        | Y    | 文本内容 |
| style    | Object        | Y    | 文本样式 |

##### style参数描述：

| 属性    | 类型            | 是否必填 | 说明        |
| ------- |---------------|------|-----------|
| fontFamily    | String | N    | 字体     |
| fontSize    | String        | N    | 字号 |
| fontWeight    | Number        | N    | 是否加粗。1：是；0：否 |
| fontItalic    | Number        | N    | 是否斜体。1：是；0：否 |
| fontUnderline    | Number        | N    | 是否下划线。1：是；0：否 |
| color    |Array        | N    | 字体颜色：rgba |


##### 回调参数描述：
| 属性    | 类型   | 说明                     |
| ------- | ------ | ------------------------ |
| code    | Number | 0: 成功  |
| message    | String | 成功或者失败原因  |
