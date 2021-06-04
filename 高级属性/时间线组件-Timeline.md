# Schema
```
"structure":{
	"structure": [
		{
			"key": "a",
			"name": "子项1"
		},
		{
			"key": "b",
			"name": "子项2"
		},
		{
			"key": "c",
			"name": "子项3"
		}
	]
}
```
# 返回数据
```
"a"
```

## Schema说明:
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| direction | 排布方向（可选值：row、column） | string | 否 | row |
| structure | 结构（详见structure） | array | 否 |  |
| style | 时间线样式 | object | 否 |  |
| itemStyle | 子项样式 | object | 否 |  |
| activeItemStyle | 高亮子项样式 | object | 否 |  |
| nameStyle | 子项名称样式 | object | 否 |  |
| activeNameStyle | 高亮子项名称样式 | object | 否 |  |
| iconStyle | 子项图标样式 | object | 否 |  |
| activeIconStyle | 高亮子项图标样式 | object | 否 |  |
| lineStyle | 子项线样式 | object | 否 |  |
| activeLineStyle | 高亮子项线样式 | object | 否 |  |

#### structure
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
| key | 唯一key值，用于当前进行项的判断 | string | true |  |
| name | 子项名称 | string | true |  |

## 返回数据说明：
接口返回为字符串，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 默认值 |
|--|--|--|--|--|
| [structure.key] | Schema中配置的structure唯一key值 | 是 | string |  |
