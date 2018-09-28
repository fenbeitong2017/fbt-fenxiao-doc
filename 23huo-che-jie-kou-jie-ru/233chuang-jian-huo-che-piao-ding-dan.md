2.3.3创建火车票订单

####接口说明
- 1.**最新接口**
- 2.创建火车票订单




请求方式|请求地址
----|---
POST|/open/api/train/createOrder


字段|名称|类型|必填|描述
-----|-----|----|----|----
timestamp|时间戳 |long |Y|13位时间戳
sign|签名 |string |Y|
access_token|token | string |Y|登录 token
employee_id| 操作人id|string |Y|操作人id,调用接口人 id
employee_type| 用户类型|string|Y|类型，0为分贝用户，1为第三方用户
data |请求数据| jsonobject |Y|
data.date|开始日期|string  |Y|2018-09-20





请求示例：

```


{
	"access_token":"5747fbc10f0e60e0709d8d722",
	"sign":"oihfnlyeofdh98",
	"timestamp":124124325,
	"employee_id":"59b74c1323445f2d54dd07922",
	"employee_type":0,
	"data":        {
                "contactname": "韩树起",
                "contactmobile": "17080151667",
                "ticketcount": 1,
                "totalprice": 11.00,
                "traincode": "K876",
                "fromstation": "九江",
                "tostation": "武穴",
                "sdate": "2018-10-24",
                "insurancenum": 0,
                "seatname": "硬座",
                "seatcode": "3",
                "passenger": [
                  {
                    "TicketType": 1,
                    "passengerName": "韩树起",
                    "passengerIdCardType": 2,
                    "passengerIdCardNum": "iu3k83ks3ls3",
                    "Insurancecount": 0
                    
                  }
                ],
                "supplier": "分贝通",
                "source":"JUNWEI000001"
            }
}


```






```
{
    "request_id": "ID6ja6rJvrowfQBXbBfR",
    "code": 0,
    "type": 0,
    "msg": "success",
    "data": {
        "data": {
            "orderTime": "16:08",
            "orderId": "5badddec27986379fa183a44"
        },
        "supplier": "分贝通",
        "source": "JUNWEI000001",
        "successcode": "T"
    }
}


```




