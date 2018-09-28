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






```

TDZ:特等座,YZ:硬座,RZ:软座,RZ2:二等软座,RZ1:一等软座,YWS:硬卧上铺,YWZ:硬卧中铺,YWX:硬卧下铺,RWS:软卧上铺,RWX:软卧下铺,GWS:高级软卧上铺,GWX:高级软卧上铺,SWZ:商务座

身份证:1 护照:2,军官证:3,士兵证:4,台胞证:5,其他:6

```





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



响应数据:

字段|名称|类型|必填|描述
-----|-----|----|----|----
Id| 序号|string |Y|序号
OrderNumber|订单号 |string |Y|
ContactName| 联系人姓名| string|Y|韩冰
ContactMobile|联系人手机 |string |Y|17080151667
OrderStatus| 订单状态|integer |Y|参照状态码表
TotalPayPrice| 订单总价 |double |Y|3.0
PayTime| 支付时间|string |Y|11：30
passengers| 乘客对象集合 |jsonarray |Y|乘客信息集合
passengers.PassengerName| 乘客姓名|integer |Y|韩冰
passengers.PassengerType|乘客类型 |integer |Y|成人票 = 1,儿童票 = 2
passengers.IdCardType| 乘客证件类型| string|Y|参照证件类型表
passengers.IdCardNumber|乘客证件号 |string |Y|1234567
tickets| 票信息集合|jsonarray |Y|票信息集合
tickets.DepartPort|出发车站 |string |Y|九江
tickets.DepartTime| 出发时间|string |Y|13:02
tickets.ArrivePort|到达车站 |string |Y|武穴
tickets.ArriveTime| 到达时间 |string |Y|13:40
tickets.TrainNo|火车列次| string|Y|K876
tickets.SeatType|座位类型 |integer |Y|参照类型表
tickets.SeatNo| 座位号|string |Y|13车厢,061号
tickets.Coach|车厢 |string |Y|13车厢,061号
tickets.Price| 价格 |double |Y|3.0
tickets.InsuranceNum|保险份数 |integer |Y|1
tickets.InsuranceNumber| 保单号 |string |Y|89ifiu9873isd9832
tickets.InsurancePrice|保险价格| string|Y|10






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
                "PassengerType": 1,
                "IdCardNumber": "iu3k83ks3ls3",
                "PassengerName": "韩冰",
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
        "ContactName": "韩冰",
        "successcode": "T",
        "intpagecount": 1
    }
}


```

