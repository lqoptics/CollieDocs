sdk激活与升级

SDK激活

[POST]
```
/sdk/<product_sn>/active/
```

[PAYLOAD]
```
    nocstr = fields.String(required=True)
    sign = fields.String(required=True)
```

[RESPONSE]
```
{
"code": 20001, 
"message": "", 
"data": {
    "status": 1, //0：尚未激活, 1: 激活成功, 2: 被注销了
    "due":"2719-10-1 10:10:10", // 到期时间
    "token": "tsf2xfae4cfsd211s345fds11e",
    "sign": "6f8bfae4cfb63ac59129d2b2345f73fe"
}
}
```

SDK升级

[POST]
```
/sdk/<product_sn>/update/<sdk_version>/
```

[PAYLOAD]
```
    nocstr = fields.String(required=True)
    sign = fields.String(required=True)
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