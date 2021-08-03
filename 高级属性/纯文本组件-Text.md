# schema
```
{
  "text": "text",
  "style": {"width": "40%"}
}
```

## Schema说明:

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| text | 文字内容 | 否 | string |  |
| style | 文本样式 | 否 | object | react-css |
| action | 点击事件 | 否 | string | 详见 [事件](/事件) |
| actionData | 点击事件所需参数 | 否 | object | 详见 [事件](/事件) |

## 请求结果
```Json
{
  "text": "text接口返回"
}
```
