2.3.9火车票订单详情

####接口说明
- 1.**最新接口**
- 2.火车票订单详情




请求方式|请求地址
----|---
POST|/open/api/train/order/detail


字段|名称|类型|必填|描述
-----|-----|----|----|----
timestamp|时间戳 |long |Y|13位时间戳
sign|签名 |string |Y|
access_token|token | string |Y|登录 token
employee_id| 操作人id|string |Y|操作人id,调用接口人 id
employee_type| 用户类型|string|Y|类型，0为分贝用户，1为第三方用户
data |请求数据| jsonobject |Y|
data.orderno| 订单号|string |Y|Jljsfo98w8eoiewnlsdo
data.supplier| 供应商|string |Y|分贝通
data.source| 订单来源|string |Y|A企业




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
                "supplier": "分贝通",
                "source":"JUNWEI000001"
            }
}


```






```
{
    "request_id": "i8UkcYLP5euvxvBdeGY3",
    "code": 0,
    "type": 0,
    "msg": "success",
    "data": {
        "ContactMobile": "17080151667",
        "passengers": [
            {
                "PassengerType": "韩树起",
                "IdCardNumber": "iu3k83ks3ls3",
                "PassengerName": "韩树起",
                "IdCardType": 2
            }
        ],
        "tickets": [
            {
                "ArriveTime": "13:02",
                "DepartTime": "12:09",
                "TrainNo": "K876",
                "Price": 11,
                "DepartPort": "九江",
                "InsuranceNum": 0,
                "SeatType": "硬座",
                "SeatNo": "13车厢,061号",
                "TicketNo": "5badddec27986379fa183a45",
                "ArrivePort": "武穴",
                "Coach": "13车厢,061号"
            }
        ],
        "OrderNumber": "5badddec27986379fa183a44",
        "source": "JUNWEI000001",
        "intrecordcount": 0,
        "TotalPayPrice": 11,
        "OrderStatus": 3,
        "supplier": "分贝通",
        "Id": 1,
        "PayTime": 1538121196844,
        "ContactName": "韩树起",
        "successcode": "T",
        "intpagecount": 1
    }
}


```

