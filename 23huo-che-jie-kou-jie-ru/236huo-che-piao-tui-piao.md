2.3.6火车票退票

####接口说明
- 1.**最新接口**
- 2. 火车票退票




请求方式|请求地址
----|---
POST|/open/api/train/closeTicket


字段|名称|类型|必填|描述
-----|-----|----|----|----
timestamp|时间戳 |long |Y|13位时间戳
sign|签名 |string |Y|
access_token|token | string |Y|登录 token
employee_id| 操作人id|string |Y|操作人id,调用接口人 id
employee_type| 用户类型|string|Y|类型，0为分贝用户，1为第三方用户
data |请求数据| jsonobject |Y|
data.orderno|订单号|string  |Y|5bade0b427986379fa183a75
data.ticketnos|票号|jsonarray  |Y|5bade0b427986379fa183a76
data.supplier|供应商|string  |Y|分贝通
data.source|订单来源|string  |Y|A企业



















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
                "orderno": "5bade0b427986379fa183a75",
                "ticketnos":["5bade0b427986379fa183a76"],
                "supplier": "分贝通",
                "source":"JUNWEI000001"
            }
}


```






```
{
    "request_id": "dy62P0ajDa6oIRfhpbiV",
    "code": 0,
    "type": 0,
    "msg": "success",
    "data": {
        "data": {
            "msg": "退订成功",
            "orderId": "5bade0b427986379fa183a75"
        },
        "supplier": "分贝通",
        "source": "JUNWEI000001",
        "successcode": "T"
    }
}


```

