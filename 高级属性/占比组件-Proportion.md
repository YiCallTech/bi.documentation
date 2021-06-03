# schema
```
{
 "name": "string,
 "nameStyles": {},
 "totalUnit": "string",
 "totalStyles": {},
 "colors": ["#0fb6d9", "#01ffff"],
}
```
# 返回数据
```
[{
    "id": "string",
    "name": "string",
    "value": 123,
}]
```

## schema说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--| -- |
| name | 占比数据的名称 | 否| string |  |
| nameStyles | 名称样式 | 否 | object | react-css |
| totalUnit | 总数的单位 | 否 | string |  |
| totalStyles | 总数的样式 | 否 | object | react-css |
| colors | 颜色取值范围 | 否 | array | 默认['#0fb6d9', '#01ffff', '#f7c73f', '#ff9742'] |

#### 返回数据说明:
接口返回为数组对象，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| id | id | 是 | string | 有点击事件且点击为弹出列表时，id会传入列表的postData中 |
| name | 每条占比数据的名称 | 是 | string | 有点击事件且点击为弹出列表时，name会显示为弹出框的标题 |
| value | 每条占比数据的数量 | 是 | number | 自动累加value，算出总数和占比数 |
