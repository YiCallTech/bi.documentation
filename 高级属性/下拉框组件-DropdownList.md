# Schema

```
{
    "title": "基础数据",
    "titleStyle": {},
    "buttonStyle": { },
    "isHover": false,
    "showIcon": true,
    "iconType": "img",
    "icon": "https://control.hzxc.gov.cn/dxx/static/xia@2x.png",
    "iconStyle": { },
    "menuStyle": { },
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
```

## Schema说明：
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| title | 下拉框按钮显示文本 | String | 否 | |
| titleStyle | 按钮文本样式 | Object | 否 |  |
| dropdownType | 下拉框样式,type1或者type2 | String | 否 | type1 |
| buttonStyle | 下拉框按钮样式 | Object | 否 |  |
| menuStyle | 下拉菜单样式 | Object | 否 |  |
| showIcon | 是否展示图标 | Boolean | 否 | false |
| icon | iconType - img：需要传图片url；antd：antd3.X的icon type |  String | 否 |  |
| activeIcon | iconType - img：需要传图片url；antd：antd3.X的icon type |  String | 否 |  |
| iconType | 图标类型 img，antd | String | 否 | img |
| iconStyle | 图标样式 | Object | 否 | |
| isHover | 下拉框是否移入触发（true: 移入触发; false: 点击触发;） | bool | 否 | false |
| dropdownHeight | 下拉框高度 | number | 否 |  |
| dropdownWidth | 下拉框宽度 | number | 否 | |
| isTitleChange | 下拉框标题是否随着菜单选择改变 | Boolean | 否 | false |
| hiddenFrontendId | 需要初始时隐藏的组件frontendId | Array | 是 | |
| items | 子组件（参考items说明） | Array | 是 | |
| defaultItem | 默认当前显示菜单下标 | number | 否 | 1 |

#### menuValue
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| menuKey | 下拉菜单项的key |  String |  |


#### items说明
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| name | 下拉菜单名称 |  String |  |
| action | 点击事件类型 详见 [事件](/交互事件.md)  | String | 否 |  |
| actionData | 点击事件类型参数 详见 [事件](/交互事件.md) | Object | 否 |  |
| frontendId | 更新组件 id |  String |  |
| postDataList | 更新组件传参 详见items.postDataList | Array | 否 |  |
| value | 下拉框菜单的value | string | 否 |  |
| subItems | 下拉框子菜单 详见items.subMenu | Object | 否 |  |

###### items.postDataList
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| frontendId | 子组件 id | Array | 是 |  |
| updateData | frontendId对应子组件的传参 | object | 否 |  |

###### items.subMenu
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| title | 下拉菜单名称 |  String |  |
| value | 下拉框菜单的value | string | 否 |  |
| children | 下一层下拉框子菜单 | string | 否 |  |