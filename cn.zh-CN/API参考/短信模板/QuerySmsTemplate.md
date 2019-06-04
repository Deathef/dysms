# QuerySmsTemplate {#doc_api_Dysmsapi_QuerySmsTemplate .reference}

调用接口QuerySmsTemplate查询短信模板的审核状态。

申请短信模板后，可以通过接口QuerySmsTemplate查询短信模板的审核状态。如果审核未通过，会返回审核失败的原因，请针对具体原因重新修改短信模板。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Dysmsapi&api=QuerySmsTemplate)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|TemplateCode|String|是|SMS\_152550005|短信模板CODE。您可以在控制台**模板管理**页面或API接口**AddSmsTemplate**的返回参数中获取短信模板CODE。

 |
|AccessKeyId|String|否|LTAIP00vvvvvvvvv|主账号AccessKey的ID。

 |
|Action|String|否|QuerySmsTemplate|系统规定参数。取值：**QuerySmsTemplate**。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|请求状态码。

 -   返回OK代表请求成功。
-   其他错误码详见[错误码列表](~~101346~~)。

 |
|CreateDate|String|2019-06-04 11:42:17|短信模板的创建日期和时间。

 |
|Message|String|OK|状态码的描述。

 |
|Reason|String|非验证码类型短信，请选择短信通知类型为推广短信。|审核备注。

 -   如果审核状态为**审核通过**或**审核中**，参数Reason显示为“无审核备注”。
-   如果审核状态为**审核未通过**，参数Reason显示审核的具体原因。

 |
|RequestId|String|0A974B78-02BF-4C79-ADF3-90CFBA1B55B1|请求ID。

 |
|TemplateCode|String|SMS\_167035184|短信模板CODE。

 |
|TemplateContent|String|亲爱的会员！阿里云短信服务祝您新年快乐！|模板内容。

 |
|TemplateName|String|阿里云短信测试模板|模板名称。

 |
|TemplateStatus|Integer|1|模板审核状态。其中：

 -   0：审核中。
-   1：审核通过。
-   2：审核失败，请在返回参数Reason中查看审核失败原因。

 |
|TemplateType|Integer|1|短信类型。其中：

 -   0：验证码。
-   1：短信通知。
-   2：推广短信。
-   3：国际/港澳台消息。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=QuerySmsTemplate
&TemplateCode=SMS_152550005
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<QuerySmsTemplateResponse>
  <TemplateCode>SMS_167035184</TemplateCode>
  <Message>OK</Message>
  <RequestId>0A974B78-02BF-4C79-ADF3-90CFBA1B55B1</RequestId>
  <TemplateContent>亲爱的会员！阿里云短信服务祝您新年快乐！</TemplateContent>
  <TemplateName>阿里云短信测试模板</TemplateName>
  <TemplateType>1</TemplateType>
  <Code>OK</Code>
  <CreateDate>2019-06-04 11:42:17</CreateDate>
  <Reason>非验证码类型短信，请选择短信通知类型为推广短信。</Reason>
  <TemplateStatus>1</TemplateStatus>
</QuerySmsTemplateResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"TemplateType":1,
	"TemplateContent":"亲爱的会员！阿里云短信服务祝您新年快乐！",
	"TemplateName":"阿里云短信测试模板",
	"Message":"OK",
	"RequestId":"0A974B78-02BF-4C79-ADF3-90CFBA1B55B1",
	"TemplateCode":"SMS_167035184",
	"CreateDate":"2019-06-04 11:42:17",
	"Code":"OK",
	"TemplateStatus":1,
	"Reason":"非验证码类型短信，请选择短信通知类型为推广短信。"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Dysmsapi)

