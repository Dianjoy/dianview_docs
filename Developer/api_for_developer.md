# APi for Developer

###dianview 视频广告提供APi接口便开发者获取数据，结果会返回对应数据的列表。

##概述

###开发者依据文档提供的参数，构造请求链接，获取相应的数据。

##请求格式

<b><font color="red">www.dianview.com/stats/transfer-api/index?ad_category=video&start_time=2016-12-01&end_time=2016-12-25&group_by_date=1&apikey=*******</font></b>

##参数列表

| 字段名称 | 是否必须 | 类型 | 描述 | 
|--------|----------|--------|----------|
| ad_category | 是 | string | 广告类别,值为video(视频)或者interstitial(插屏)[注:无此参数默认为video] |
| apikey | 是  | string | 用户惟一key  |
| start_time | 否  | string | 起始时间，例如2016-12-22  |
| end_time | 否  | string | 结束时间，例如2016-12-25  |
| group_by_date | 否  | string | 是否按天分组，值为0或者1  |


##数据返回

###数据格式

####数据返回格式:json

##返回数据内容

###示例

<p>

####示例1

<b>用户唯一key为XXXXXXX,广告类别为video,查找其2016-12-01日到2016-12-25日的详情,需要按天分</b>
<pre>
GET   www.dianview.com/stats/transfer-api/index?start_time=2016-12-01&end_time=2016-12-25&group_by_date=1&ad_category=video&apikey=********
</pre>

####示例2

<b>用户唯一key为XXXXXXX,广告类别为interstitial,查找其2016-12-01日到2016-12-25日的总数据</b>
<pre>
GET   www.dianview.com/stats/transfer-api/index?start_time=2016-12-01&end_time=2016-12-25&group_by_date=0&ad_category=interstitial&apikey=********
</pre>

####示例3

<b>用户唯一key为XXXXXXX,广告类别为video,查其历史总数据</b>
<pre>
GET   www.dianview.com/stats/transfer-api/index?ad_category=video&apikey=********
</pre>

##返回参数列表

###视频参数列表

| 字段名称 | 是否必须 | 类型 | 描述 | 
|--------|----------|--------|----------|
| app_id | 是  | string | 应用id  |
| earning | 是  | string | 收入 |
| ad_click | 是 | int | 点击数 |
| req_num | 是  | int | 返回数  |
| video_start | 是  | int | 播放开始数  |
| video_finish | 是  | int | 播放完成数  |
| ad_show | 是  | int | 广告展示数  |
| day | 否  | string | 日期 |

###插屏参数列表

| 字段名称 | 是否必须 | 类型 | 描述 | 
|--------|----------|--------|----------|
| req_num | 是 | int | 返回数 |
| app_id | 是 | string | 应用id |
| earning | 是  | string | 收入  |
| ad_click | 是 | int | 点击数 |
| ad_install | 是  | int | 安装数 |
| ad_imp | 是  | int | 展示数  |
| down_ok | 是  | int | 下载数  |
| ad_notify | 是 | int | 回调数 |
| day | 否  | string | 日期 |

###提示

用户唯一key可以找相关人员获取。

