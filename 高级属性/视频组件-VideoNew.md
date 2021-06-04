# schema
```
{
	"url": "http://xx.mp4",
	"style": {},
	"autoplay": false,
	"preload": "meta",
	"controls": true,
	"loop": false,
	"muted": false,
	"poster": "http://xx.png",
	"disablePictureInPicture": true,
	"controlsList": "nodownload"
}
```

# 返回数据
```
{
"url": "http://www.w3school.com.cn/example/html5/mov_bbb.mp4"
}
```

#### schema说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| url | 视频地址 | 否 | string |  |
| style | css样式 | 否 | Object | react-css |
| autoplay | 视频在就绪后马上播放 | 否 | bool |  |
| preload | 视频在页面加载时是否进行加载并预备播放 | 否 | string | 默认：'meta' |
| controls | 是否显示视频控件 | 否 | bool | 默认：true |
| loop | 是否重复播放 | 否 | bool |  |
| muted | 是否被静音 | 否 | bool |  |
| poster | 视频封面地址 | 否 | string |  |
| disablePictureInPicture | 是否隐藏画中画 | 否 | bool |  |
| controlsList | 视频控件集 | 否 | string | 可多选, nodownload=隐藏视频下载按钮 nofullscreen=隐藏全屏模式控件 noremoteplayback=隐藏远程播放控件 |

## 返回数据说明:
接口返回为对象，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| url | 视频地址 | 否 | string |  |