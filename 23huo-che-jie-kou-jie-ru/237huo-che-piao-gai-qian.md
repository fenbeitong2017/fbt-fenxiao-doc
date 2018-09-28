2.3.7火车票改签

####接口说明
- 1.**最新接口**
- 2.火车票改签




请求方式|请求地址
----|---
POST|/open/api/train/updateTicket


字段|名称|类型|必填|描述
-----|-----|----|----|----
timestamp|时间戳 |long |Y|13位时间戳
sign|签名 |string |Y|
access_token|token | string |Y|登录 token
employee_id| 操作人id|string |Y|操作人id,调用接口人 id
employee_type| 用户类型|string|Y|类型，0为分贝用户，1为第三方用户
data |请求数据| jsonobject |Y|
data.bdate|开始日期|string  |Y|2018-09-20





请求示例：

```


{
	"access_token":"5747fbc10f0e60e0709d8d722",
	"sign":"oihfnlyeofdh98",
	"timestamp":124124325,
	"employee_id":"59b74c1323445f2d54dd07922",
	"employee_type":0,
	"data":  
	        {
       "orderno": "5badddec27986379fa183a44",
        "ticketnos":"5badddec27986379fa183a45",
         "totalprice": 11.00,
        "traincode":"K876",
         "fromstation": "九江",
         "tostation": "武穴",
        "sdate":"2018-10-25",
         "seatname": "硬座",
         "seatcode": "1",
         "supplier": "分贝通",
        "source":"JUNWEI000001"
            }
}


```






```
{
    "request_id": "3Bx3DLuZ43WB7oRjjq7a",
    "code": 0,
    "type": 0,
    "msg": "success",
    "data": {
        "data": "success",
        "supplier": "分贝通",
        "source": "JUNWEI000001",
        "successcode": "T"
    }
}


```

