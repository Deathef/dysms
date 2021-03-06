# SendSms {#doc_api_Dysmsapi_SendSms .reference}

调用SendSms发送短信。

**SendSms**接口是短信发送接口，支持在一次请求中向多个不同的手机号码发送同样内容的短信。

如果您需要在一次请求中分别向多个不同的手机号码发送不同签名和模版内容的短信，请使用**SendBatchSms**接口。

调用该接口发送短信时，请注意：

-   发送短信会根据发送量计费，价格请参考[计费说明](https://www.aliyun.com/price/product#/sms/detail)。
-   在一次请求中，最多可以向1000个手机号码发送同样内容的短信。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Dysmsapi&api=SendSms&type=RPC&version=2017-05-25)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|PhoneNumbers|String|是|15900000000|接收短信的手机号码。

 格式：

 -   国内短信：11位手机号码，例如15951955195。
-   国际/港澳台消息：国际区号+号码，例如85200000000。

 支持对多个手机号码发送短信，手机号码之间以英文逗号（,）分隔。上限为1000个手机号码。批量调用相对于单条调用及时性稍有延迟。

 **说明：** 验证码类型短信，建议使用单独发送的方式。

 |
|SignName|String|是|阿里云|短信签名名称。请在控制台**签名管理**页面**签名名称**一列查看。

 **说明：** 必须是已添加、并通过审核的短信签名。

 |
|TemplateCode|String|是|SMS\_153055065|短信模板ID。请在控制台**模板管理**页面**模板CODE**一列查看。

 **说明：** 必须是已添加、并通过审核的短信签名；且发送国际/港澳台消息时，请使用国际/港澳台短信模版。

 |
|AccessKeyId|String|否|LTAIP00vvvvvvvvv|主账号AccessKey的ID。

 |
|Action|String|否|SendSms|系统规定参数。取值：**SendSms**。

 |
|OutId|String|否|abcdefgh|外部流水扩展字段。

 |
|SmsUpExtendCode|String|否|90999|上行短信扩展码，无特殊需要此字段的用户请忽略此字段。

 |
|TemplateParam|String|否|\{"code":"1111"\}|短信模板变量对应的实际值，JSON格式。

 **说明：** 如果JSON中需要带换行符，请参照标准的JSON协议处理。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|BizId|String|900619746936498440^0|发送回执ID，可根据该ID在接口QuerySendDetails中查询具体的发送状态。

 |
|Code|String|OK|请求状态码。

 -   返回OK代表请求成功。
-   其他错误码详见[错误码列表](~~101346~~)。

 |
|Message|String|OK|状态码的描述。

 |
|RequestId|String|F655A8D5-B967-440B-8683-DAD6FF8DE990|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?PhoneNumbers=15900000000
&SignName=阿里云
&TemplateCode=SMS_153055065
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<SendSmsResponse>
      <Message>OK</Message>
      <RequestId>44DF7A95-603F-4651-9298-BE1850BEB53F</RequestId>
      <BizId>336006646937050335^0</BizId>
      <Code>OK</Code>
</SendSmsResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Message":"OK",
	"RequestId":"2184201F-BFB3-446B-B1F2-C746B7BF0657",
	"BizId":"197703245997295588^0",
	"Code":"OK"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Dysmsapi)查看更多错误码。

