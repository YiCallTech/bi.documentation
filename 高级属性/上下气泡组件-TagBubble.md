# schema
```
{
    "style": {},
    "itemStyle": {},
    "nameStyle": {},
    "countStyle": {},
    "unitStyle": {},
    "unit",
    "maxTagWidth": 140,
    "minTagWidth": 70,
    "displacement": 100,
    "animationTime": 2
}
```
# 返回数据
```
[{
    "name": "标题名称",
    "count": 123,
}]
```

## Schema说明:
| 名称 | 描述 | 必填 | 类型 | 默认值 |
|--|--|--|--|--|
| style | 组件的样式 | 否 | object |  |
| itemStyle | 气泡的样式 | 否 | object |  |
| nameStyle | 气泡名称的样式 | 否 | object |  |
| countStyle | 气泡数值的样式 | 否 | object |  |
| unitStyle | 气泡单位的样式 | 否 | object |  |
| unit | 单位 | 否 | string |  |
| maxTagWidth | 最大气泡的宽度 | 否 | number | 140 |
| minTagWidth | 最小气泡的宽度 | 否 | number | 70 |
| displacement | 气泡运动时的百分比位移 | 否 | number | 100 |
| animationTime | 气泡单次运动周期的时长(秒) | 否 | number | 2 |

## 返回数据说明：
接口返回为数组对象，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 默认值 |
|--|--|--|--|--|
| name | 气泡展示的标题名称 | 否 | string |  |
| count | 气泡展示的数值 | 否 | number |  |