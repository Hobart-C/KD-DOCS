<!--
 * @Author: 关广强 ggq@jsszkd.com
 * @Date: 2022-05-09 20:32:35
 * @LastEditors: 关广强 ggq@jsszkd.com
 * @LastEditTime: 2022-05-11 13:58:37
 * @FilePath: \KD-API-DOCS\public\md\api\批量导入2D3DPOI资源.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
## 仿真功能
### 生命体

#### API名称：
批量导入2D3DPOI资源
#### 功能描述：

批量导入2D/3DPOI资源

#### 渲染示例：

#### 调用方法：

##### ES6 Modules
``` javascript
import { SceneModel } from 'kd-api/lib';

SceneModel.importData(param)
.then((res)=>{
    // 初始化场景成功
    console.log(res)
})
.catch((err)=>{})

```

##### Script 标签
``` javascript
window.KdApi.SceneModel.importData(param)
.then((res)=>{
    // 设置开启/关闭日志成功
    console.log(res)
})
.catch((err)=>{})
```


#### 数据格式：

```javascript
let jsondata = {
    asset_uuid: 'xxxx_xxxx';
    type: 'xxxx_xxxx';
    color: [1,1,0,1];
    tag_uuid: ['xxxx_xxxx'];
    list: [{
        name: 'xxxx';
        text: 'xxxx';
        coord: {
            longitude: '1';
            latitude: '2';
            height: '1';
        };
    }];
}
```

##### 参数描述：

| 属性      | 类型  | 是否必填 | 说明                                   |
| --------- | ------| ------ | ------ |
| asset_uuid | String | Y | 资产ID    |
| type | String | Y | 生命体类型：3DPoi、2DPoi;    |
| color | String | N | 颜色RGBA    |
| tag_uuid | String[] | N | 标签ID    |
| list | Object[listModel] | Y |     |

##### listModel参数描述：
| 属性      | 类型  | 是否必填 | 说明                                   |
| --------- | ------| ------ | ------ |
| name | String | Y | POI名称    |
| text | String | N | POI文本内容    |
| coord | Object | Y |     |

##### coord参数描述：
| 属性      | 类型  | 是否必填 | 说明                                   |
| --------- | ------| ------ | ------ |
| longitude | String | Y | 位置信息：经度    |
| latitude | String | Y | 位置信息：纬度    |
| height | Object | Y | 位置信息：高度    |



##### 回调数据参数描述：

| 属性    | 类型   | 说明                     |
| ------- | ------ | -------- |
| code    | Number | 200: 成功，500：失败  |
| message    | String | 成功或者失败描述  |
