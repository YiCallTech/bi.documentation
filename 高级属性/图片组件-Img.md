# schema
```
{
    "url": "https://control.hzxc.gov.cn/dxx/static/basic_man.png",
    "name": "basic_man.png",
    "style": {
        "width": 20,
        "height": 20
    }
}

```
# 返回数据
```
{
    "url": "https://control.hzxc.gov.cn/dxx/static/basic_man.png",
}
```

## schema说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| name | 图片名称 | 否 | string |  |
| url | 图片地址 | 否 | string | 支持外链、base64、路径 |
| style | css样式 | 否 | Object | react-css |

## 返回数据说明:
接口返回为对象，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| url | 图片地址 | 否 | string | 支持外链、base64、路径 |