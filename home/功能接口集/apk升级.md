- 获取apk的版本信息：

[GET]
```
/device/<str:device_sn>/update/apk/<str:apk_version>
```
[Note] device_sn为设备的序列号， apk_version为当前的版本

[RESPONSE]
```
{
"code": 20001, 
"message": "", 
"data": {
"version": "V3.0 Rev1.0", // 新的版本号
"update_at": "2018-10-11",
"etag": "sdahjkskldjaksljhdknxkl", //一堆文件校验码，可以忽略
"size": "300M", //文件大小
"url": "https://s.s.com/d.s.d"  //下载链接
}
}
```
[ERROR CODE]
```
DEVICE_NOT_REGISTERED = ErrorTuple(('40011', '设备未注册'))
RECORD_PARAMS_ERROR = ErrorTuple(('40001', '记录的参数错误'))
```