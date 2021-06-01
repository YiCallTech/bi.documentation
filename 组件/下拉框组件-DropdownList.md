# Schema

```json
{
  "width": 100,
  "height": 60,
  "left": 15,
  "top": 50,
  "zIndex": 1,
  "refreshIntervel": 5000,
  "config": {
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
}
```

# Schema说明

## Schema
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| type | 组件类型 |  String | 是 | 固定：dropdownlist |
| frontendId |  组件id，后端自动生成 | String | 是 |  |
| width | 组件宽度 | String/Number | 否 | 100 |
| height | 组件高度 | String/Number | 否 | 100 |
| left | 组件离父极左边距离 | String/Number | 否 | 0 |
| top | 组件离父极顶部距离 | String/Number | 否 | 0 |
| zIndex | 组件层级 | Number | 否 | 99 |
| config | 组件配置 | Object | 否 | 参考Schema.config |

| dataUrl | 接口地址 | string | 否 | |
| postData | 请求时的特定数据 | Object | 否 | 自定义 |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| title | 下拉框按钮显示文本 | String | 否 | |
| dropdownType | 下拉框样式,type1或者type2 | String | 否 | type1 |
| titleStyle | 按钮文本样式 | Object | 否 |  |
| buttonStyle | 下拉框按钮样式 | Object | 否 |  |
| menuStyle | 下拉菜单样式 | Object | 否 |  |
| showIcon | 是否展示图标 | Boolean | 否 | false |
| iconType | 图标类型 img，antd | String | 否 | img |
| iconStyle | 图标样式 | Object | 否 | |
| icon | iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| activeIcon | iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| defaultTab | 默认当前显示菜单下标 | number | 否 | 1 |
| isHover | 下拉框是否移入触发（true: 移入触发; false: 点击触发;） | bool | 否 | false |
| dropdownHeight | 下拉框高度 | number | 否 |  |
| dropdownWidth | 下拉框宽度 | number | 否 | |
| isTitleChange | 下拉框标题是否随着菜单选择改变 | Boolean | 否 | false |
| hiddenFrontendId | 需要初始时隐藏的组件frontendId | Array | 是 | |
| items | 子组件（参考items说明） | Array | 是 | |

### Schema.config.items
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| name | 下拉菜单名称 |  String |  |
| action | 点击事件类型 详见 [事件](/事件)  | String | 否 |  |
| actionData | 点击事件类型参数 详见 [事件](/事件) | Object | 否 |  |
| value | 下拉框菜单的value | string | 否 |  |
| subButtonStyle | 下拉框子菜单样式 | Object | 否 |  |
| menuValue | 下拉框子菜单的value | Object | 否 |  |
| subMenu | 下拉框子菜单 | Object | 否 |  |
| postDataList | 子组件传参 | Array | 否 |  |

### Schema.config.items.postDataList
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| frontendId | 子组件 id | Array | 是 |  |
| updateData | frontendId对应子组件的传参 | object | 否 |  |

### Schema.config.items.subMenu
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| title | 下拉菜单名称 |  String |  |
| value | 下拉框菜单的value | string | 否 |  |
| children | 下一层下拉框子菜单 | string | 否 |  |

### Schema.config.items.menuValue
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| menuKey | 下拉菜单项的key |  String |  |

### Schema.config.items.subMenu
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| title | 下拉菜单名称 |  String |  |
| value | 下拉框菜单的value | string | 否 |  |
