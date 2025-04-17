---  
nav_order: 4
parent: API Reference  
title: "squote"
--- 
<link rel="stylesheet" href="/assets/css/just-the-docs-custom.css">
現貨行情
註冊接收即時和查詢

<a id="squote.SQuote"></a>

## SQuote Objects

```python
class SQuote()
```

<a id="squote.SQuote.on_error"></a>

#### on\_error

錯誤事件

<a id="squote.SQuote.on_connected"></a>

#### on\_connected

連線成功事件

<a id="squote.SQuote.on_disonnected"></a>

#### on\_disonnected

斷線事件

<a id="squote.SQuote.on_base_data"></a>

#### on\_base\_data

普通個股基本資料事件..傳入物件:BaseData

<a id="squote.SQuote.on_tick_data"></a>

#### on\_tick\_data

普通股競價交易即時行情資訊事件..傳入物件:TickData

<a id="squote.SQuote.on_tick_data_open_close"></a>

#### on\_tick\_data\_open\_close

普通股競價交易開(收)盤價資料事件..傳入物件:TickDataOpenclose

<a id="squote.SQuote.on_index_data"></a>

#### on\_index\_data

指數資訊事件..傳入物件:IndexData

<a id="squote.SQuote.on_otc_base_data"></a>

#### on\_otc\_base\_data

上櫃個股基本資料事件..傳入物件:BaseData

<a id="squote.SQuote.on_otc_tick_data"></a>

#### on\_otc\_tick\_data

上櫃股競價交易即時行情資訊事件..傳入物件:TickData

<a id="squote.SQuote.on_otc_tick_data_open_close"></a>

#### on\_otc\_tick\_data\_open\_close

上櫃股競價交易開(收)盤價資料事件..傳入物件:TickDataOpenclose

<a id="squote.SQuote.on_otc_index_data"></a>

#### on\_otc\_index\_data

櫃買指數資訊事件..傳入物件:IndexData

<a id="squote.SQuote.get_current_server"></a>

#### get\_current\_server

```python
def get_current_server()
```

目前連結主機IP 和 PORT
##### Returns 

| Name | Type | Description |
| ------ | ------ | ------------- |
| host | str | 主機IP |    
| port | str | 主機Port |

<a id="squote.SQuote.get_server_list"></a>

#### get\_server\_list

```python
def get_server_list()
```

透過可連結主機
##### Returns dict[Server]

| Name | Type | Description |
| ------ | ------ | ------------- |
| key | str | servername |    
| value | Server | Server ip:str / port:int |

<a id="squote.SQuote.set_sever_by_name"></a>

#### set\_sever\_by\_name

```python
def set_sever_by_name(servername)
```

透過主機名稱連結主機
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| servername | str | 主機名稱 |

<a id="squote.SQuote.get_subscribe"></a>

#### get\_subscribe

```python
def get_subscribe()
```

查詢已註冊商品

<a id="squote.SQuote.query_base_data"></a>

#### query\_base\_data

```python
def query_base_data(item) -> BaseDataResponse
```

查詢普通個股基本資料
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |      

##### Returns 
BaseDataResponse

<a id="squote.SQuote.query_tick_data"></a>

#### query\_tick\_data

```python
def query_tick_data(item) -> TickDataResponse
```

查詢最後普通股競價交易即時行情資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |      

##### Returns 
TickDataResponse

<a id="squote.SQuote.query_tick_open_close"></a>

#### query\_tick\_open\_close

```python
def query_tick_open_close(item) -> TickDataOpenCloseResponse
```

查詢最後普通股競價交易開(收)盤價資料資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |      

##### Returns 
TickDataOpenCloseResponse

<a id="squote.SQuote.query_otc_base_data"></a>

#### query\_otc\_base\_data

```python
def query_otc_base_data(item) -> BaseDataResponse
```

查詢otc普通個股基本資料
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |      

##### Returns 
BaseDataResponse

<a id="squote.SQuote.query_otc_tick_data"></a>

#### query\_otc\_tick\_data

```python
def query_otc_tick_data(item) -> TickDataResponse
```

查詢otc最後普通股競價交易即時行情資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |      

##### Returns 
TickDataResponse

<a id="squote.SQuote.query_otc_tick_open_close"></a>

#### query\_otc\_tick\_open\_close

```python
def query_otc_tick_open_close(item) -> TickDataOpenCloseResponse
```

查詢otc最後普通股競價交易開(收)盤價資料資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |      

##### Returns 
TickDataOpenCloseResponse

<a id="squote.SQuote.query_index_data"></a>

#### query\_index\_data

```python
def query_index_data(item) -> IndexDataResponse
```

查詢最後指數資料資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 指數代號 |      

##### Returns 
IndexDataResponse

<a id="squote.SQuote.query_otc_index_data"></a>

#### query\_otc\_index\_data

```python
def query_otc_index_data(item) -> IndexDataResponse
```

查詢最後櫃買指數資料資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 指數代號 |      

##### Returns 
IndexDataResponse

<a id="squote.SQuote.sub_stock"></a>

#### sub\_stock

```python
def sub_stock(item: str) -> Tuple[bool, str]
```

註冊股票行情
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |     

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.unsub_stock"></a>

#### unsub\_stock

```python
def unsub_stock(item: str) -> Tuple[bool, str]
```

反註冊
##### Parameters  

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |     

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.sub_otc"></a>

#### sub\_otc

```python
def sub_otc(item: str) -> Tuple[bool, str]
```

註冊otc行情
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |     

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.unsub_otc"></a>

#### unsub\_otc

```python
def unsub_otc(item: str) -> Tuple[bool, str]
```

反註冊
##### Parameters  

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 股票代碼 |     

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.sub_index"></a>

#### sub\_index

```python
def sub_index(item: str) -> Tuple[bool, str]
```

註冊指數資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 指數代碼 |     

| 指數名稱 | 指數代碼 |     
| ------ | ------ |
| 臺股指數 | IX0001 |
| 臺灣50指數 | TW50 |
| 臺灣中型100指數 | TWMC |
| 臺灣資訊科技指數 | TWIT |
| 臺灣發達指數 | TWEI |
| 臺灣高股息指數 | TWDP |
| 臺灣就業99指數 | EMP99 |
| 臺灣公司治理100指數 | CG100 |
| 寶島股價指數 | FRMSA |
| 臺灣高薪100指數 | HC100 |
| 電子類兩倍槓桿指數 | EDRL2 |
| 電子類反向指數 | EDRIN |
| 臺指日報酬兩倍指數 | TTDRL2 |
| 臺指反向一倍指數 | TTDRIN |
| 小型股300指數 | SC300 |
| 金融類日報酬兩倍指數 | FDRL2 |
| 金融類日報酬反向一倍指數 | FDRIN |
| 漲升股利150指數 | DVA150 |
| 漲升股利100指數 | DVA100 |
| 藍籌30指數 | BC30 |
| 工業菁英30指數 | INE30 |
| 電子菁英30指數 | ITE30 |
| 低波動精選30指數 | LV30 |
| 低貝塔100指數 | LB100 |
| 藍籌30反向一倍指數 | BC30-1 |
| 中小型精選50指數 | SMC50 |
| 中小型A級動能50指數 | SAM50 |
| 臺灣永續指數 | F4GTTE |
| 股利150報酬指數 | IR0091 |
| 電子菁英30報酬指數 | IR0095 |
| 存股雙十等權重報酬指數 | IR0112 |
| 特選大蘋果報酬指數 | IR0113 |
| 中小型300報酬指數 | IR0114 |
| 特股高息20報酬指數 | IR0115 |
| 臺灣500報酬指數 | IR0116 |
| 特選外資豐擁50報酬指數 | IR0117 |
| 臺灣生技指數 | IX0103 |
| 特選高息低波指數 | IX0104 |
| 工業菁英30反向一倍指數 | IX0106 |
| 特選內需高收益指數 | IX0107 |
| 臺灣中小型公司治理指數 | IX0108 |
| 臺灣IPO指數 | IX0109 |
| 價值投資指數 | IX0110 |
| 中小型300指數 | IX0114 |

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.unsub_index"></a>

#### unsub\_index

```python
def unsub_index(item: str) -> Tuple[bool, str]
```

反註冊指數資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 指數代碼 |     

| 指數名稱 | 指數代碼 |     
| ------ | ------ |
| 臺股指數 | IX0001 |
| 臺灣50指數 | TW50 |
| 臺灣中型100指數 | TWMC |
| 臺灣資訊科技指數 | TWIT |
| 臺灣發達指數 | TWEI |
| 臺灣高股息指數 | TWDP |
| 臺灣就業99指數 | EMP99 |
| 臺灣公司治理100指數 | CG100 |
| 寶島股價指數 | FRMSA |
| 臺灣高薪100指數 | HC100 |
| 電子類兩倍槓桿指數 | EDRL2 |
| 電子類反向指數 | EDRIN |
| 臺指日報酬兩倍指數 | TTDRL2 |
| 臺指反向一倍指數 | TTDRIN |
| 小型股300指數 | SC300 |
| 金融類日報酬兩倍指數 | FDRL2 |
| 金融類日報酬反向一倍指數 | FDRIN |
| 漲升股利150指數 | DVA150 |
| 漲升股利100指數 | DVA100 |
| 藍籌30指數 | BC30 |
| 工業菁英30指數 | INE30 |
| 電子菁英30指數 | ITE30 |
| 低波動精選30指數 | LV30 |
| 低貝塔100指數 | LB100 |
| 藍籌30反向一倍指數 | BC30-1 |
| 中小型精選50指數 | SMC50 |
| 中小型A級動能50指數 | SAM50 |
| 臺灣永續指數 | F4GTTE |
| 股利150報酬指數 | IR0091 |
| 電子菁英30報酬指數 | IR0095 |
| 存股雙十等權重報酬指數 | IR0112 |
| 特選大蘋果報酬指數 | IR0113 |
| 中小型300報酬指數 | IR0114 |
| 特股高息20報酬指數 | IR0115 |
| 臺灣500報酬指數 | IR0116 |
| 特選外資豐擁50報酬指數 | IR0117 |
| 臺灣生技指數 | IX0103 |
| 特選高息低波指數 | IX0104 |
| 工業菁英30反向一倍指數 | IX0106 |
| 特選內需高收益指數 | IX0107 |
| 臺灣中小型公司治理指數 | IX0108 |
| 臺灣IPO指數 | IX0109 |
| 價值投資指數 | IX0110 |
| 中小型300指數 | IX0114 |

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.sub_otc_index"></a>

#### sub\_otc\_index

```python
def sub_otc_index(item: str) -> Tuple[bool, str]
```

註冊櫃買指數資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 指數代碼 |     

| 指數名稱 | 指數代碼 |     
| ------ | ------ |
| 櫃買指數 | IX0043 |
| 富櫃五十指數 | GTSM50 |
| 指標公債指數 | TWTBI |
| 線上遊戲業指數 | GAME |
| 高殖利率指數 | GTHD |
| 勞工就業88指數 | EMP88 |
| 櫃買薪酬指數 | GTCI |
| 櫃買公司治理指數 | TPCGI |
| 富櫃200報酬指數 | IR0118 |
| 臺灣生技指數 | IX0103 |
| 臺灣中小型公司治理指數 | IX0108 |
| 臺灣IPO指數 | IX0109 |
| 富櫃200指數 | IX0118 |

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.unsub_otc_index"></a>

#### unsub\_otc\_index

```python
def unsub_otc_index(item: str) -> Tuple[bool, str]
```

反註冊櫃買指數資訊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| item | str | 指數代碼 |     

| 指數名稱 | 指數代碼 |     
| ------ | ------ |
| 櫃買指數 | IX0043 |
| 富櫃五十指數 | GTSM50 |
| 指標公債指數 | TWTBI |
| 線上遊戲業指數 | GAME |
| 高殖利率指數 | GTHD |
| 勞工就業88指數 | EMP88 |
| 櫃買薪酬指數 | GTCI |
| 櫃買公司治理指數 | TPCGI |
| 富櫃200報酬指數 | IR0118 |
| 臺灣生技指數 | IX0103 |
| 臺灣中小型公司治理指數 | IX0108 |
| 臺灣IPO指數 | IX0109 |
| 富櫃200指數 | IX0118 |

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="squote.SQuote.close"></a>

#### close

```python
def close()
```

關閉物件

<a id="squote.Format"></a>

## Format Objects

```python
class Format()
```

<a id="squote.Format.Data01"></a>

#### Data01

集中市場普通股個股基本資料

<a id="squote.Format.Data03"></a>

#### Data03

集中市場普通股競價交易指數統計資料

<a id="squote.Format.Data06"></a>

#### Data06

集中市場普通股競價交易即時行情資訊

<a id="squote.Format.Data10"></a>

#### Data10

新編臺灣指數資料

<a id="squote.Format.Data12"></a>

#### Data12

集中市場普通股競價交易開(收)盤價資料

<a id="squote.Format.OTC_Data01"></a>

#### OTC\_Data01

上櫃股票個股基本資料

<a id="squote.Format.OTC_Data03"></a>

#### OTC\_Data03

上櫃股票等價交易指數統計資料

<a id="squote.Format.OTC_Data06"></a>

#### OTC\_Data06

上櫃股票等價交易即時行情資訊

<a id="squote.Format.OTC_Data11"></a>

#### OTC\_Data11

上櫃股票等價交易個股開收盤價資料

<a id="squote.Format.OTC_Data12"></a>

#### OTC\_Data12

新編櫃買指數資料

---  
nav_order: 4
parent: API Reference  
title: "squote"
--- 
<link rel="stylesheet" href="/assets/css/just-the-docs-custom.css">
外期行情物件

<a id="sdata.BaseData"></a>

## BaseData Objects

```python
@dataclass
class BaseData()
```

個股基本資料回覆

<a id="sdata.BaseData.stock_code"></a>

#### stock\_code

股票代號 str

<a id="sdata.BaseData.product_name"></a>

#### product\_name

商品名稱 str

<a id="sdata.BaseData.industry"></a>

#### industry

產業別 str

<a id="sdata.BaseData.security_type"></a>

#### security\_type

證券別 str

<a id="sdata.BaseData.stock_abnormal_code"></a>

#### stock\_abnormal\_code

股票異常代碼 str

<a id="sdata.BaseData.reference_price"></a>

#### reference\_price

參考價 float

<a id="sdata.BaseData.upper_limit_price"></a>

#### upper\_limit\_price

漲停價 float

<a id="sdata.BaseData.lower_limit_price"></a>

#### lower\_limit\_price

跌停價 float

<a id="sdata.BaseData.non_10_denomination"></a>

#### non\_10\_denomination

非10元面額 bool

<a id="sdata.BaseData.abnormal_recommendation_note"></a>

#### abnormal\_recommendation\_note

異常推介個股註記 str

<a id="sdata.BaseData.special_abnormal_security_note"></a>

#### special\_abnormal\_security\_note

特殊異常證券註記 str

<a id="sdata.BaseData.day_trading_note"></a>

#### day\_trading\_note

可現股當沖註記 str

<a id="sdata.BaseData.exempt_short_selling_note"></a>

#### exempt\_short\_selling\_note

豁免平盤下融券賣出註記 str

<a id="sdata.BaseData.exempt_borrowing_short_selling_note"></a>

#### exempt\_borrowing\_short\_selling\_note

豁免平盤下借券賣出註記 str

<a id="sdata.BaseData.matching_cycle_seconds"></a>

#### matching\_cycle\_seconds

搓合循環秒數 int

<a id="sdata.BaseData.foreign_stock_identifier"></a>

#### foreign\_stock\_identifier

外國股票識別碼 str

<a id="sdata.BaseData.trading_unit"></a>

#### trading\_unit

交易單位 int

<a id="sdata.BaseData.trading_currency_code"></a>

#### trading\_currency\_code

交易幣別代號 str

<a id="sdata.TickData"></a>

## TickData Objects

```python
@dataclass
class TickData()
```

個股競價交易即時行情資訊

<a id="sdata.TickData.stock_code"></a>

#### stock\_code

股票代號 str

<a id="sdata.TickData.match_time"></a>

#### match\_time

撮合時間 str

<a id="sdata.TickData.limit_up_down_note"></a>

#### limit\_up\_down\_note

漲跌停註記 str

<a id="sdata.TickData.status_note"></a>

#### status\_note

狀態註記 str

<a id="sdata.TickData.cumulative_volume"></a>

#### cumulative\_volume

累計成交數量 int

<a id="sdata.TickData.trade_price"></a>

#### trade\_price

成交價 float

<a id="sdata.TickData.trade_volume"></a>

#### trade\_volume

成交量 int

<a id="sdata.TickData.best_bid_price_1"></a>

#### best\_bid\_price\_1

最佳一檔買進價 float

<a id="sdata.TickData.best_bid_volume_1"></a>

#### best\_bid\_volume\_1

最佳一檔買進量 int

<a id="sdata.TickData.best_bid_price_2"></a>

#### best\_bid\_price\_2

最佳二檔買進價 float

<a id="sdata.TickData.best_bid_volume_2"></a>

#### best\_bid\_volume\_2

最佳二檔買進量 int

<a id="sdata.TickData.best_bid_price_3"></a>

#### best\_bid\_price\_3

最佳三檔買進價 float

<a id="sdata.TickData.best_bid_volume_3"></a>

#### best\_bid\_volume\_3

最佳三檔買進量 int

<a id="sdata.TickData.best_bid_price_4"></a>

#### best\_bid\_price\_4

最佳四檔買進價 float

<a id="sdata.TickData.best_bid_volume_4"></a>

#### best\_bid\_volume\_4

最佳四檔買進量 int

<a id="sdata.TickData.best_bid_price_5"></a>

#### best\_bid\_price\_5

最佳五檔買進價 float

<a id="sdata.TickData.best_bid_volume_5"></a>

#### best\_bid\_volume\_5

最佳五檔買進量 int

<a id="sdata.TickData.best_ask_price_1"></a>

#### best\_ask\_price\_1

最佳一檔賣出價 float

<a id="sdata.TickData.best_ask_volume_1"></a>

#### best\_ask\_volume\_1

最佳一檔賣出量 int

<a id="sdata.TickData.best_ask_price_2"></a>

#### best\_ask\_price\_2

最佳二檔賣出價 float

<a id="sdata.TickData.best_ask_volume_2"></a>

#### best\_ask\_volume\_2

最佳二檔賣出量 int

<a id="sdata.TickData.best_ask_price_3"></a>

#### best\_ask\_price\_3

最佳三檔賣出價 float

<a id="sdata.TickData.best_ask_volume_3"></a>

#### best\_ask\_volume\_3

最佳三檔賣出量 int

<a id="sdata.TickData.best_ask_price_4"></a>

#### best\_ask\_price\_4

最佳四檔賣出價 float

<a id="sdata.TickData.best_ask_volume_4"></a>

#### best\_ask\_volume\_4

最佳四檔賣出量 int

<a id="sdata.TickData.best_ask_price_5"></a>

#### best\_ask\_price\_5

最佳五檔賣出價 float

<a id="sdata.TickData.best_ask_volume_5"></a>

#### best\_ask\_volume\_5

最佳五檔賣出量 int

<a id="sdata.TickDataOpenClose"></a>

## TickDataOpenClose Objects

```python
@dataclass
class TickDataOpenClose()
```

個股競價交易開(收)盤價資料

<a id="sdata.TickDataOpenClose.stock_code"></a>

#### stock\_code

股票代號 str

<a id="sdata.TickDataOpenClose.open_price"></a>

#### open\_price

開盤價格 float

<a id="sdata.TickDataOpenClose.high_price"></a>

#### high\_price

最高成交價格 float

<a id="sdata.TickDataOpenClose.low_price"></a>

#### low\_price

最低成交價格 float

<a id="sdata.TickDataOpenClose.last_trade_price"></a>

#### last\_trade\_price

最近成交價 float

<a id="sdata.TickDataOpenClose.cumulative_volume"></a>

#### cumulative\_volume

累計成交量 int

<a id="sdata.TickDataOpenClose.time"></a>

#### time

時間 str

<a id="sdata.IndexData"></a>

## IndexData Objects

```python
@dataclass
class IndexData()
```

指數資料

<a id="sdata.IndexData.index_code"></a>

#### index\_code

指數代號 str

<a id="sdata.IndexData.index_time"></a>

#### index\_time

指數時間 str

<a id="sdata.IndexData.latest_index"></a>

#### latest\_index

最新指數 float

<a id="sdata.BaseDataResponse"></a>

## BaseDataResponse Objects

```python
@dataclass
class BaseDataResponse()
```

查詢個股基本資料回覆物件

<a id="sdata.BaseDataResponse.ok"></a>

#### ok

是否成功 bool

<a id="sdata.BaseDataResponse.error"></a>

#### error

錯誤訊息 str

<a id="sdata.BaseDataResponse.data"></a>

#### data

回覆物件 BaseData

<a id="sdata.TickDataResponse"></a>

## TickDataResponse Objects

```python
@dataclass
class TickDataResponse()
```

查詢個股競價交易即時行情資訊回覆物件

<a id="sdata.TickDataResponse.ok"></a>

#### ok

是否成功 bool

<a id="sdata.TickDataResponse.error"></a>

#### error

錯誤訊息 str

<a id="sdata.TickDataResponse.data"></a>

#### data

回覆物件 TickData

<a id="sdata.TickDataOpenCloseResponse"></a>

## TickDataOpenCloseResponse Objects

```python
@dataclass
class TickDataOpenCloseResponse()
```

查詢個股競價交易開(收)盤價資料回覆物件

<a id="sdata.TickDataOpenCloseResponse.ok"></a>

#### ok

是否成功 bool

<a id="sdata.TickDataOpenCloseResponse.error"></a>

#### error

錯誤訊息 str

<a id="sdata.TickDataOpenCloseResponse.data"></a>

#### data

回覆物件 TickDataOpenClose

<a id="sdata.IndexDataResponse"></a>

## IndexDataResponse Objects

```python
@dataclass
class IndexDataResponse()
```

查詢指數回覆物件

<a id="sdata.IndexDataResponse.ok"></a>

#### ok

是否成功 bool

<a id="sdata.IndexDataResponse.error"></a>

#### error

錯誤訊息 str

<a id="sdata.IndexDataResponse.data"></a>

#### data

回覆物件 IndexData

