# SignSmsReport {#concept_423096 .concept}

通过HTTP批量推送方式可以拉取签名审核状态消息（SignSmsReport）。

## 协议说明 {#section_qz1_ylk_3gb .section}

|参数|说明|
|:-|:-|
|协议|HTTP + JSON|
|编码|UTF-8|

## 请求说明 {#section_ert_j4k_3gb .section}

请求内容为JSON格式，单次请求仅包含一条审核状态报告。

-   请求样例

    ``` {#codeblock_qkf_pw2_s2j}
    {
        "sign_source":"公众号",
        "reason":"test",
        "sign_name":"短信签名模版1957",
        "orderId":"14130019",
        "sign_status":"AuditPass",
        "remark":"test",
        "sign_scene":"SMS_123123242",
        "create_date":"2019-05-30 19:58:25"
    }
    ```

-   字段说明

    |名称|类型|是否必选|示例|描述|
    |--|--|----|--|--|
    |sign\_status|string|必选|approved|签名审核状态，包括：     -   approving：审核中
    -   approved：审核通过
    -   rejected：审核未通过
 |
    |reason|string|可选|文件不能证明信息真实性，请重新上传|审核未通过原因|
    |sign\_source|string|必选|企事业单位的全称或简称|签名来源|
    |sign\_name|string|必选|阿里云|签名名称|
    |remark|string|可选|当前的短信签名应用于双11大促推广营销|申请说明|
    |creat\_date|string|必选|2019-01-08 16:44:13|短信签名创建日期和时间|
    |order\_id|string|必选|205100|短信签名审核工单号|
    |sign\_scene|string|必选|通用|适用场景|


## 响应说明 {#section_m1d_r4k_3gb .section}

-   响应样例

    ``` {#codeblock_to1_t6d_9bc}
    {
      "code" : 0,
      "msg" : "接收成功"
    }
    ```

-   字段说明

    |名称|类型|是否必选|说明|示例值|
    |:-|:-|:---|:-|:--|
    |code|Number|必选|应答编码|0|
    |msg|String|可选|描述信息|接收成功|


## 重新推送 {#section_ush_ptk_3gb .section}

第一次推送失败后，间隔1分钟、5分钟、10分钟、30分钟、60分钟、60分钟、60分钟、60分钟、60分钟后会进行重推，直至推送成功为止。如果推送10次后仍失败，不再重试。

