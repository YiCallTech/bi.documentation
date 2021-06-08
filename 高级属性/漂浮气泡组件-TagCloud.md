# Schema

```json
{
  "speed": 2,
  "radius": 55
}
```

# 请求结果
```Json
[{
  "id": "a901b15c773f48b9b64b039884876fb3",
  "count": 15,
  "name": "暴雨"
}, {
  "id": "ad80313232c844b5a9ae6731a441d731",
  "count": 1,
  "name": "消防安全"
}, {
  "id": "31f20d2db7d34f39a9c398c90b453ce9",
  "count": 1,
  "name": "环境卫生"
}]
```

#### Schema说明:
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| speed | 移动速度 | Number| 否 | 1 |
| radius | 标签半径 | Number | 否 | 60 |

## 返回数据说明：
接口返回为数组对象，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 默认值 |
|--|--|--|--|--|
| id | 气泡id | 否 | string |  |
| count | 气泡排序 | 否 | number |  |
| name | 气泡显示名称 | 否 | string |  |