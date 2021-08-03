# schema
```
{
  "type": "header",
  "frontendId": "header",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Weather",
  "postData": {},
  "config": {
    "title": "灯芯巷社区驾驶舱",
    "isWeather": true,
    "isTime": true,
    "isLightSpot": true,
  }
}
```

# 返回数据
```
{
    "temperature": 28,
    "weatherType": "晴天",
}
```

#### 数据说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| type | 组件类型 | 是 | string | 前端根据schema的type识别组件 |
| frontendId | 组件id | 是 | string | 唯一的key值 |
| dataUrl | 接口地址 | 否 | string | 用于获取天气数据，isWeather为false时不调用 |
| postData | 请求时的特定数据 | 否 | object | 自定义 |
| refreshInterval | 定时刷新时间 | 否 | number | 毫秒，大于999 |
| config | 组件配置 | 否 | object | 参考Schema.config |

#### Schema.config
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--| -- |
| title | 标题 | 是| string | |
| isWeather | 是否展示天气 | 否 | bool | |
| isTime | 是否显示时间| 否 | bool | |
| isLightSpot | 是否显示光点 | 否 | bool | |

## 返回数据说明：
接口返回为字符串，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| temperature | 温度 | 是 | number | |
| weatherType | 天气类型 | 是 | string |  |