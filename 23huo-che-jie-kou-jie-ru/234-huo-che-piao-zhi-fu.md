2.3.4 火车票支付

####接口说明
- 1.**最新接口**
- 2.火车票支付




请求方式|请求地址
----|---
POST|/open/api/train/createTicket


字段|名称|类型|必填|描述
-----|-----|----|----|----
timestamp|时间戳 |long |Y|13位时间戳
sign|签名 |string |Y|
access_token|token | string |Y|登录 token
employee_id| 操作人id|string |Y|操作人id,调用接口人 id
employee_type| 用户类型|string|Y|类型，0为分贝用户，1为第三方用户
data |请求数据| jsonobject |Y|
data.orderno|开始日期|string  |Y|7dj73j9f384ud983hfd98
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
	"data":      {
                "orderno": "5badddec27986379fa183a44",
                "supplier": "分贝通",
                "source":"JUNWEI000001"
            }
}


```



响应数据:

字段|名称|类型|必填|描述
-----|-----|----|----|----
orderStatusValue| 订单状态value|string |Y|5badddec27986379fa183a44
orderStatusKey| 订单状态key|integer |Y|3201
orderId|订单ID|string |Y|5badddec27986379fa183a44
supplier| 供应商| string|Y|分贝通
source|订单来源 |string |Y|JUNWEI000001
successcode| 成功标识 |string |Y| T-成功;F-失败



```
{
    "request_id": "BETSQTDpXt3yknU5mtfF",
    "code": 0,
    "type": 0,
    "msg": "success",
    "data": {
        "data": {
            "orderId": "5badddec27986379fa183a44",
            "orderStatusValue": "出票中",
            "orderStatusKey": 3201
        },
        "supplier": "分贝通",
        "source": "JUNWEI000001",
        "successcode": "T"
    }
}


```




