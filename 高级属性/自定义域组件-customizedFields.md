# schema

```
{
  "style": {
    "color": "red"
  },
  "labelStyle": {},
  "valueStyle": {},
  "key": "name",
  "label": "姓名",
  "value": "",
  "template": "<span>{name}1221212</span>"
}
```

# 返回数据

```
{
  "name": "张三",
  "location": "德胜东村47幢",
  "xxxx": "xxxx"
}
```

## schema 说明:
| 名称 | 描述 | 类型 | 必填 | 默认值 | 备注 |
|--|--|--|--|--|--|
| key | 属性键值 | string | 否 |  |  |
| label | 标签名 | string | 否 |  |  |
| value | 默认值 | string | 否 |  |  |
| template | 值模版 | string | 否 |  |  |
| style | 域样式 | object | 否 |  |  |
| labelStyle | 标签样式 | object | 否 |  |  |
| valueStyle | 值样式 | object | 否 |  |  |

## 返回数据说明:

接口返回为对象，值任意
