# schema
```
{
    "temperature": 28,
    "weatherType": "晴天",
    "showIcon": true,
    "style": {
      "width": "40%",
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

## schema说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| temperature | 默认温度 | 否 | number |  |
| weatherType | 默认天气类型 | 否 | string |  |
| showIcon | 默认天气类型 | 否 | boolean |  |
| style | 组件样式 | 否 | object | react-css |

## 返回数据说明:
接口返回为对象，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| temperature | 温度 | 是 | number | |
| weatherType | 天气类型 | 是 | string |  |
