# TemplateSmsReport {#concept_423101 .concept}

通过HTTP批量推送方式可以拉取短信模板审核状态消息（TemplateSmsReport）。

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
        "template_type":"验证码",
        "reason":"test",
        "template_name":"短信测试模版1957",
        "orderId":"14130019",
        "template_content":"签名测试签名测试签名测试签名测试",
        "template_status":"AuditPass",
        "remark":"test",
        "template_code":"SMS_123123242",
        "create_date":"2019-05-30 19:58:25"
    }
    ```

-   字段说明

    |名称|类型|是否必选|示例|描述|
    |--|--|----|--|--|
    |template\_status|string|必选|approved|模板审核状态：     -   approving：审核中
    -   approved：审核通过
    -   rejected：审核未通过
 |
    |reason|string|可选| 非验证码、注册码、校验码、动态码类型短信

 请选择短信通知类型/营销推广类型

 |审核未通过原因|
    |template\_code|string|必选|SMS\_152550005|短信模板CODE|
    |template\_name|string|必选|阿里云测试|模板名称|
    |remark|string|可选|当前的短信模板应用于双11大促推广营销|申请说明|
    |creat\_date|string|必选|2019-01-08 16:44:13|短信模板创建日期和时间|
    |order\_id|string|必选|205101|短信模板审核工单号|
    |template\_type|string|必选|验证码|模板类型|
    |template\_content|string|必选| 您正在申请手机注册，验证码为：$\{code\}。

 5分钟内有效！

 |模板内容|


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

