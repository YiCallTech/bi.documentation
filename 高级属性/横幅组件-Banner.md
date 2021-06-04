# Schema

```json
{
  "type": "banner",
  "frontendId": "ka3s324543333kwg4rod4",
  "width": 700,
  "height": 150,
  "left": 500,
  "top": 120,
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Duty",
  "postData": {},
  "refreshInterval": 5000,
  "config": {
    "align": "center",
  }
}
```
# 说明

# Schema说明

## Schema
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| type | 组件类型 |  String | 是 | 固定：banner |
| frontendId |  组件id，后端自动生成 | String | 是 |  |
| width | 组件宽度 | String/Number | 否 | auto |
| height | 组件高度 | String/Number | 否 | 100 |
| left | 组件离父极左边距离 | String/Number | 否 | 0 |
| top | 组件离父极顶部距离 | String/Number | 否 | 120 |
| zIndex | 组件层级 | Number | 否 | 99 |
| center | 对其方式 | String | 否 | center |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| align | 对其方式 center | String| 否 | center |

# 接口数据
```json
[{
  "title": "今日值班社工",
  "values": ["范苏毅", "黄佳霏"]
}]
```