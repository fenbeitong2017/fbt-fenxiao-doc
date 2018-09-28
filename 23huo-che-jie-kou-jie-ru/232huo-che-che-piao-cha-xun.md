2.3.2 火车车票查询

####接口说明
- 1.**最新接口**
- 2.查询火车订单列表接口


请求方式|请求地址
----|---
POST|/open/api/train/getTrainList


字段|名称|类型|必填|描述
-----|-----|----|----|----
timestamp|时间戳 |long |Y|13位时间戳
sign|签名 |string |Y|
access_token|token | string |Y|登录 token
employee_id| 操作人id|string |Y|操作人id,调用接口人 id
employee_type| 用户类型|string|Y|类型，0为分贝用户，1为第三方用户
data |请求数据| jsonobject |Y|
data.date|开始日期|string  |Y|2018-09-20
data.fromcity| 出发车站code|string |N|JJG
data.tocity| 目的车站code|string |Y|WXN
data.sign| 签名|string |N|k88uewu98u382o8dssd32t43
data.source| 订单来源|string |Y|A企业




请求示例：

```


{
	"access_token":"5747fbc10f0e60e0709d8d722",
	"sign":"oihfnlyeofdh98",
	"timestamp":124124325,
	"employee_id":"59b74c1323445f2d54dd07922",
	"employee_type":0,
	"data":      {
                "date": "2018-10-23",
                "fromcity": "JJG",
                "tocity": "WXN",
                "sign": "890389ui392",
                "source":"JUNWEI000001"
            }
}


```




响应数据:

字段|名称|类型|必填|描述
-----|-----|----|----|----
Id| 序号|string |Y|序号
TrainCode|火车列次 |string |Y|车次
TrainType|  火车类型| string|Y|如: 高速动车
StartCity|出发站 |string |Y|如:北京
StartTime| 出发时间|string |Y|如:HH:mm
EndCity| 到达站|string |Y|如:上海
EndTime|到达时间 |string |Y|HH:mm
BeginStation| 始发站| string|Y|始发站
EndStation|终点站 |string |Y|终点站
Distance| 距离 |integer |Y|1463
CostTime| 耗时|string |Y|如:25分
OverNight|隔夜天数 |string |Y|隔夜天数
YZ_YP| 硬座余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
RZ_YP|软座余票| integer|Y|"-" 或为0代表无票(“-1”代表无此席位)
RZ2_YP| 二等软座余票 |integer|Y|“-“ 或为0代表无票(“-1”代表无此席位) 
RZ1_YP| 一等软座余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
YW_YP| 硬卧余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
RW_YP| 软卧余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
GW_YP|  高级软卧余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
SWZ_YP| 商务座余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
WZ_YP| 无座余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
TDZ_YP| 特等座余票 |integer |Y|“-“ 或为0代表无票(“-1”代表无此席位) 
SWZ|  商务座价格 |double |Y|精确到小数点后一位(“-”代表无价格)
GWX| 高级软卧下铺价格 |double |Y|精确到小数点后一位(“-”代表无价格)
GWS| 高级软卧上铺价格 |double |Y|精确到小数点后一位(“-”代表无价格)
RWX|  软卧下铺价格 |double |Y|精确到小数点后一位(“-”代表无价格)
RWS| 软卧上铺价格 |double |Y|精确到小数点后一位(“-”代表无价格)
YWX| 硬卧下铺价格 |double |Y|精确到小数点后一位(“-”代表无价格)
YWZ|  硬卧中铺价格 |double |Y|精确到小数点后一位(“-”代表无价格)
YWS| 硬卧上铺价格 |double |Y|精确到小数点后一位(“-”代表无价格)
RZ1| 一等软座价格 |double |Y|精确到小数点后一位(“-”代表无价格)
RZ2| 二等软座价格 |double |Y|精确到小数点后一位(“-”代表无价格)
RZ| 软座价格 |double |Y|精确到小数点后一位(“-”代表无价格)
YZ| 硬座价格 |double |Y|精确到小数点后一位(“-”代表无价格)
TDZ| 特等座价格 |double |Y|精确到小数点后一位(“-”代表无价格)

































```

{
"request_id": "KRuaqq6ckrvVHF40sP8g",
"code": 0,
"type": 0,
"msg": "success",
"data": {
"data": [
{
"RZ_YP": "-1",
"EndTime": "13:02",
"OverNight": "0",
"WZ_YP": "-1",
"RZ": "-",
"CostTime": "53",
"RZ1_YP": "-1",
"SWZ_YP": "-1",
"YW_YP": 21,
"GW_YP": "-1",
"TrainType": "K",
"ID": 1,
"Distance": "0",
"BeginStation": "九江",
"YZ": 11,
"EndCity": "武穴",
"GWS": "-",
"WZ": "-",
"TrainCode": "K876",
"YZ_YP": 21,
"StartTime": "12:09",
"RZ1": "-",
"GWX": "-",
"RZ2": "-",
"TDZ": "-",
"RWS": 86.5,
"StartCity": "九江",
"RWX": 131.5,
"TDZ_YP": "-1",
"EndStation": "武穴",
"YWS": 57,
"RZ2_YP": "-1",
"SWZ": "-",
"YWX": 102,
"YWZ": 0,
"RW_YP": 21
},
{
"RZ_YP": "-1",
"EndTime": "13:55",
"OverNight": "0",
"WZ_YP": 21,
"RZ": "-",
"CostTime": "1:12",
"RZ1_YP": "-1",
"SWZ_YP": "-1",
"YW_YP": 0,
"GW_YP": "-1",
"TrainType": "K",
"ID": 1,
"Distance": "0",
"BeginStation": "九江",
"YZ": 11,
"EndCity": "武穴",
"GWS": "-",
"WZ": 11,
"TrainCode": "K244",
"YZ_YP": 0,
"StartTime": "12:43",
"RZ1": "-",
"GWX": "-",
"RZ2": "-",
"TDZ": "-",
"RWS": 86.5,
"StartCity": "九江",
"RWX": 131.5,
"TDZ_YP": "-1",
"EndStation": "武穴",
"YWS": 57,
"RZ2_YP": "-1",
"SWZ": "-",
"YWX": 102,
"YWZ": 0,
"RW_YP": 0
},
{
"RZ_YP": "-1",
"EndTime": "14:35",
"OverNight": "0",
"WZ_YP": "-1",
"RZ": "-",
"CostTime": "1:10",
"RZ1_YP": "-1",
"SWZ_YP": "-1",
"YW_YP": "-1",
"GW_YP": "-1",
"TrainType": "P",
"ID": 1,
"Distance": "0",
"BeginStation": "九江",
"YZ": 3,
"EndCity": "武穴",
"GWS": "-",
"WZ": "-",
"TrainCode": "6026",
"YZ_YP": 21,
"StartTime": "13:25",
"RZ1": "-",
"GWX": "-",
"RZ2": "-",
"TDZ": "-",
"RWS": "-",
"StartCity": "九江",
"RWX": "-",
"TDZ_YP": "-1",
"EndStation": "武穴",
"YWS": "-",
"RZ2_YP": "-1",
"SWZ": "-",
"YWX": "-",
"YWZ": "-",
"RW_YP": "-1"
},
{
"RZ_YP": "-1",
"EndTime": "18:26",
"OverNight": "0",
"WZ_YP": "-1",
"RZ": "-",
"CostTime": "49",
"RZ1_YP": "-1",
"SWZ_YP": "-1",
"YW_YP": 21,
"GW_YP": "-1",
"TrainType": "K",
"ID": 1,
"Distance": "0",
"BeginStation": "九江",
"YZ": 11,
"EndCity": "武穴",
"GWS": "-",
"WZ": "-",
"TrainCode": "K754",
"YZ_YP": 10,
"StartTime": "17:37",
"RZ1": "-",
"GWX": "-",
"RZ2": "-",
"TDZ": "-",
"RWS": 86.5,
"StartCity": "九江",
"RWX": 131.5,
"TDZ_YP": "-1",
"EndStation": "武穴",
"YWS": 57,
"RZ2_YP": "-1",
"SWZ": "-",
"YWX": 102,
"YWZ": 0,
"RW_YP": 4
},
{
"RZ_YP": "-1",
"EndTime": "19:12",
"OverNight": "0",
"WZ_YP": "-1",
"RZ": "-",
"CostTime": "59",
"RZ1_YP": "-1",
"SWZ_YP": "-1",
"YW_YP": 21,
"GW_YP": "-1",
"TrainType": "K",
"ID": 1,
"Distance": "0",
"BeginStation": "九江",
"YZ": 11,
"EndCity": "武穴",
"GWS": "-",
"WZ": "-",
"TrainCode": "K1454",
"YZ_YP": 21,
"StartTime": "18:13",
"RZ1": "-",
"GWX": "-",
"RZ2": "-",
"TDZ": "-",
"RWS": 86.5,
"StartCity": "九江",
"RWX": 131.5,
"TDZ_YP": "-1",
"EndStation": "武穴",
"YWS": 57,
"RZ2_YP": "-1",
"SWZ": "-",
"YWX": 102,
"YWZ": 0,
"RW_YP": 0
},
{
"RZ_YP": "-1",
"EndTime": "21:49",
"OverNight": "0",
"WZ_YP": "-1",
"RZ": "-",
"CostTime": "1:15",
"RZ1_YP": "-1",
"SWZ_YP": "-1",
"YW_YP": 14,
"GW_YP": "-1",
"TrainType": "K",
"ID": 1,
"Distance": "0",
"BeginStation": "九江",
"YZ": 11,
"EndCity": "武穴",
"GWS": "-",
"WZ": "-",
"TrainCode": "K570",
"YZ_YP": 21,
"StartTime": "20:34",
"RZ1": "-",
"GWX": "-",
"RZ2": "-",
"TDZ": "-",
"RWS": 86.5,
"StartCity": "九江",
"RWX": 131.5,
"TDZ_YP": "-1",
"EndStation": "武穴",
"YWS": 57,
"RZ2_YP": "-1",
"SWZ": "-",
"YWX": 102,
"YWZ": 0,
"RW_YP": 0
},
{
"RZ_YP": "-1",
"EndTime": "22:21",
"OverNight": "0",
"WZ_YP": "-1",
"RZ": "-",
"CostTime": "1:0",
"RZ1_YP": "-1",
"SWZ_YP": "-1",
"YW_YP": 0,
"GW_YP": "-1",
"TrainType": "K",
"ID": 1,
"Distance": "0",
"BeginStation": "九江",
"YZ": 11,
"EndCity": "武穴",
"GWS": "-",
"WZ": "-",
"TrainCode": "K446",
"YZ_YP": 21,
"StartTime": "21:21",
"RZ1": "-",
"GWX": "-",
"RZ2": "-",
"TDZ": "-",
"RWS": 86.5,
"StartCity": "九江",
"RWX": 131.5,
"TDZ_YP": "-1",
"EndStation": "武穴",
"YWS": 57,
"RZ2_YP": "-1",
"SWZ": "-",
"YWX": 102,
"YWZ": 0,
"RW_YP": 0
}
],
"supplier": "分贝通",
"source": "JUNWEI000001",
"successcode": "T"
}
}

```




