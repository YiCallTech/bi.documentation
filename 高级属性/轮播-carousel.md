# schema
```
{
  "direction": "row",
  "defaultItem": 1,
  "itemStyle": {},
  "carouselInterval": 3,
  "transition": {
    "mode": "fadeInAndOut",
    "duration": 500
  },
  "items": [
    {
      "frontendId": [
        "tt7gt2i0z8xs"
      ],
      "iconStyle": {},
      "activeIconStyle": {},
      "postDataList": [],
      "name": "1"
    },
    {
      "frontendId": [
        "tt7gw9b7gu80"
      ],
      "iconStyle": {},
      "activeIconStyle": {},
      "name": "2"
    }
  ],
  "tabsType": "type1",
  "tabStyle": {},
  "tabActiveStyle": {},
  "hasTransition": true,
  "carousel": false
}
```

## schema说明:
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| direction | tab排布 row，column | string | 否 | row |  |
| hidden | 是否隐藏按钮 | boolean | 否 | false | |
| defaultItem | 默认当前显示子项内容下标，从1开始 | number | 否 | 1 | |
| btnStyle | 按钮样式 | object | 否 |  | |
| showName | 是否显示子项名称 | boolean | 否 | false | |
| nameStyle | 子项名称样式 | object | 否 |  | |
| carousel | 是否开启轮播功能 | boolean | 否 | false | |
| carouselInterval | 轮播时间间隔（秒） | number | 否 | 10 | |
| hasTransition | 是否开启过渡动画 | boolean | 否 | false | |
| transition | 过渡动画配置 参考transition说明）| object | 否 | | |
| items | 子项（参考items说明） | Array | 是 |  | |


### transition说明:
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| mode | 动画类型 | string | 否 | fadeInAndOut |  |
| duration | 过渡时间（毫秒） | number | 否 | 500 | |

### items说明:
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| frontendId | 子组件 id | array | 是 |  |
