# ModifySmsTemplate {#doc_api_Dysmsapi_ModifySmsTemplate .reference}

调用接口ModifySmsTemplate修改未通过审核的短信模板。

申请短信模板后，如果模板未通过审核，可以通过接口**ModifySmsTemplate**修改短信模板，并重新申请，提交审核。

模板内容需要符合[文本短信模板规范](~~108253~~)或[国际/港澳台短信模板规范](~~108254~~)。短信模板审核流程请参考[模板审核流程](~~108257~~)。

**说明：** 一个自然日最多可以申请100个模板。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Dysmsapi&api=ModifySmsTemplate)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|TemplateType|Integer|是|1|短信类型。其中：

 -   0表示验证码。
-   1表示短信通知。
-   2表示推广短信。
-   3国际/港澳台消息。

 |
|TemplateName|String|是|阿里云短信测试模板|模板名称，长度为1~30个字符。

 |
|TemplateContent|String|是|您正在申请手机注册，验证码为：$\{code\}，5分钟内有效！|模板内容，长度为1~500个字符。

 模板内容需要符合[文本短信模板规范](~~108253~~)或[国际/港澳台短信模板规范](~~108254~~)。

 **说明：** 修改模板时，请针对审核意见合理设计模板内容。

 |
|Remark|String|是|当前的短信模板应用于双11大促推广营销|短信模板申请说明。请在申请说明中描述您的业务使用场景，长度为1~100个字符。

 |
|TemplateCode|String|是|SMS\_152550005|短信模板CODE。您可以在控制台**模板管理**页面或API接口**AddSmsTemplate**的返回参数中获取短信模板CODE。

 |
|Action|String|否|ModifySmsTemplate|系统规定参数。取值：**ModifySmsTemplate**。

 |
|AccessKeyId|String|否|LTAIP00vvvvvvvvv|主账号AccessKey的ID。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|请求状态码。

 -   返回OK代表请求成功。
-   其他错误码详见[错误码列表](~~101346~~)。

 |
|Message|String|OK|状态码的描述。

 |
|RequestId|String|F655A8D5-B967-440B-8683-DAD6FF8DE990|请求ID。

 |
|TemplateCode|String|SMS\_152550005|短信模板CODE。您可以使用模板CODE通过API接口**QuerySmsTemplate**或在控制台查看模板申请状态和结果。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://dysmsapi.aliyuncs.com/?Action=ModifySmsTemplate
&TemplateType=1
&TemplateName=阿里云短信测试模板
&TemplateContent=您正在申请手机注册，验证码为：${code}，5分钟内有效！
&Remark=当前的短信模板应用于双11大促推广营销
&TemplateCode=SMS_152550005
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifySmsTemplateResponse>
  <TemplateCode>SMS_152550005</TemplateCode>
  <Message>OK</Message>
  <RequestId>F655A8D5-B967-440B-8683-DAD6FF8DE990</RequestId>
  <Code>OK</Code>
</ModifySmsTemplateResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Message":"OK",
	"RequestId":"F655A8D5-B967-440B-8683-DAD6FF8DE990",
	"TemplateCode":"SMS_152550005",
	"Code":"OK"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Dysmsapi)

