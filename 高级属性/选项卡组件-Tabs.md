# Schema

```json
{
  "tabsType": "type1",
  "direction": "row",
  "tabStyle": {},
  "tabActiveStyle": {},
  "defaultItem": 1,
  "carouselInterval": 3,
  "transition": {
    "mode": "fadeInAndOut",
    "duration": 500
  },
  "items": [
    {
      "frontendId": [
        "tt3llivwvsw0"
      ],
      "iconStyle": {},
      "activeIconStyle": {},
      "name": "1"
    },
    {
      "frontendId": [
        "tt3lq4q1p8g0"
      ],
      "iconStyle": {},
      "activeIconStyle": {},
      "postDataList": [],
      "name": "2"
    }
  ],
  "defaultTab": 1,
  "hasTransition": true,
  "carousel": false
}
```

## schema说明:
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| direction | tab排布 row，column | string | 否 | row |
| tabsType | tab类型 type1，type2 | string | 否 | type1 |
| tabStyle | tab样式 | object | 否 |  |
| tabActiveStyle | tab高亮时的样式 | object | 否 |  |
| defaultItem | 默认当前显示tab 下标 | number | 否 | 1 |
| tabsType | tab的类型(type1、type2) | string | 否 | type1 |
| autoHeight | 是否高度自适应 | bool | 否 | false |
| hideTabs | 是否隐藏选项卡 | bool | 否 | false |
| carousel | 是否开启轮播功能 | boolean | 否 | false | |
| carouselInterval | 轮播时间间隔（秒） | number | 否 | 10 | |
| hasTransition | 是否开启过渡动画 | boolean | 否 | false | |
| transition | 过渡动画配置 参考transition说明）| object | 否 | | |
| items | 子组件（参考items说明） | array | 是 |  |

### config.transition:
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| mode | 动画类型 | string | 否 | fadeInAndOut |  |
| duration | 过渡时间（毫秒） | number | 否 | 500 | |

### config.items
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| frontendId | 子组件 id | array | 是 |  |  |
| name | tab名称 |  string |  |  |
| formatter | tab名称格式化字符串 |  string |  |  |
| icon | 图标url |  string | 否 |  |  |
| iconStyle | 图标样式 | object | 否 |  |  |
| activeIcon | 图标url |  string | 否 |  |  |
| activeIconStyle | tab高亮时的图标样式 | object | 否 |  |  |
| postDataList | 子组件传参 | array | 否 |  |  |

### Schema.config.items.postDataList.postDataMap
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| frontendId | 子组件 id | array | 是 |  |  |
| updateData | frontendId对应子组件的传参 | object | 否 |  |  |
