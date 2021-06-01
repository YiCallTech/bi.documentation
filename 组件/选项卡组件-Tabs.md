# Schema

```json
{
  "type": "tabs",
  "frontendId": "ka3s545432323545433kwg4rod4",
  "width": 20,
  "height": 60,
  "left": 10,
  "top": 10,
  "config": {
    "direction": "column",
    "tabStyle": {
    },
    "items": [
      {
        "name": "本周",
        "frontendId": []
      },
      {
        "name": "本年",
        "frontendId": []
      },
      {
        "name": "累计",
        "frontendId": []
      }
    ]
  }
}
```

# Schema说明

## Schema
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| type | 组件类型 |  String | 是 | 固定：tabs |
| frontendId |  组件id，后端自动生成 | String | 是 |  |
| width | 组件宽度 | String/Number | 否 | 100 |
| height | 组件高度 | String/Number | 否 | 100 |
| left | 组件离父极左边距离 | String/Number | 否 | 0 |
| top | 组件离父极顶部距离 | String/Number | 否 | 0 |
| zIndex | 组件层级 | Number | 否 | 99 |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| direction | tab排布 row，column | String | 否 | row |
| tabsType | tab类型 type1，type2，type3 | String | 否 | type1 |
| tabStyle | tab样式 | Object | 否 |  |
| tabActiveStyle | tab高亮时的样式 | Object | 否 |  |
| defaultTab | 默认当前显示tab 下标 | number | 否 | 1 |
| tabsType | tab的类型(type1、type2) | string | 否 | type1 |
| autoHeight | 自动高度 | bool | 否 | false |
| items | 子组件（参考items说明） | Array | 是 |  |

### Schema.config.items
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| iconType | 图标类型 img，antd | String | 否 | |
| iconStyle | 图标样式 | Object | 否 |  |
| activeIconStyle | tab高亮时的图标样式 | Object | 否 |  |
| icon | iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| activeIcon | tab高亮时的icon， iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| name | tab名称 |  String |  |
| formatter | 格式化字符串 | String | 否 |  |
| frontendId | 子组件 id | Array | 是 |  |
| postDataList | 子组件传参 | Array | 否 |  |

### Schema.config.items.postDataList.postDataMap
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| frontendId | 子组件 id | Array | 是 |  |
| updateData | frontendId对应子组件的传参 | object | 否 |  |


# 备注
