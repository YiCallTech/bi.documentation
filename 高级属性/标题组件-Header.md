# schema
```json
{
  "title": "灯芯巷社区驾驶舱",
  "isWeather": true,
  "isTime": true,
  "isToggleContent": true,
  "isLightSpot": true,
  "background": "",
  "titleStyle": {},
  "timeStyle": {}
}
```

# 请求结果
```json
{
    "temperature": 28,
    "weatherType": "晴天",
}
```

#### Schema说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--| -- |
| title | 标题 | 是| string | |
| isWeather | 是否展示天气 | 否 | bool | |
| isTime | 是否显示时间| 否 | bool | |
| isToggleContent | 是否可以隐藏驾驶舱内容 | 否 | bool | |
| isLightSpot | 是否显示光点 | 否 | bool | |
| background | 背景颜色 | 是| string | |
| titleStyle | 标题样式 | 否 | object | react-css |
| timeStyle | 时间样式 | 否 | object | react-css |

#### 返回数据说明:

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| temperature | 温度 | 是 | number | |
| weatherType | 天气类型 | 是 | string |  |

