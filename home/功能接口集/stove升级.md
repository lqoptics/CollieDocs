STOVE升级

[POST]
```
/stove/update/<sdk_version>
```

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