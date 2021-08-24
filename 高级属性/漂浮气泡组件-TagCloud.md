# Schema

```json
{
  "type": "tagCloud",
  "frontendId": "fsgrf33kwg4rod4",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Jmfw",
  "postData": {},
  "refreshInterval": 5000,
  "width": 200,
  "height": 200,
  "left": 200,
  "top": 50,
  "config": {
    "speed": 2,
    "radius": 55,
  }
}
```

# Schema说明

## Schema
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| type | 组件类型 |  String | 是 | 固定：tagCloud |
| frontendId |  组件id，后端自动生成 | String | 是 |  |
| dataUrl | 接口地址 | string | 否 | |
| postData | 请求时的特定数据 | Object | 否 | 自定义 |
| refreshInterval | 定时刷新时间 毫秒，大于999 | Number |	否 | 1000 |
| width | 组件宽度 | String/Number | 否 | 100 |
| height | 组件高度 | String/Number | 否 | 100 |
| left | 组件离父极左边距离 | String/Number | 否 | 0 |
| top | 组件离父极顶部距离 | String/Number | 否 | 0 |
| zIndex | 组件层级 | Number | 否 | 99 |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| backgroundPic | 背景图 | String| 否 |  |
| color | 文本颜色 | String| 否 |  |
| speed | 移动速度 | Number| 否 | 1 |
| radius | 标签半径 | Number | 否 | 60 |

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
