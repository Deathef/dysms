# DeleteSmsTemplate {#doc_api_Dysmsapi_DeleteSmsTemplate .reference}

调用接口DeleteSmsTemplate删除短信模板。

**注意**：

-   不支持删除正在审核中的模板。
-   删除短信模板后不可恢复，请谨慎操作。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Dysmsapi&api=DeleteSmsTemplate)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|TemplateCode|String|是|SMS\_152550005|短信模板CODE。您可以在控制台**模板管理**页面或API接口**AddSmsTemplate**的返回参数中获取短信模板CODE。

 |
|AccessKeyId|String|否|LTAIP00vvvvvvvvv|主账号AccessKey的ID。

 |
|Action|String|否|DeleteSmsTemplate|系统规定参数。取值：**DeleteSmsTemplate**。

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
|RequestId|String|CCA2BCFF-2BA7-427C-90EE-AC6994748607|请求ID。

 |
|TemplateCode|String|SMS\_20375006|短信模板CODE。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://dysmsapi.aliyuncs.com/?Action=DeleteSmsTemplate
&TemplateCode=SMS_152550005
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteSmsTemplateResponse>
  <TemplateCode>SMS_20375006</TemplateCode>
  <Message>OK</Message>
  <RequestId>CCA2BCFF-2BA7-427C-90EE-AC6994748607</RequestId>
  <Code>OK</Code>
</DeleteSmsTemplateResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Message":"OK",
	"RequestId":"CCA2BCFF-2BA7-427C-90EE-AC6994748607",
	"TemplateCode":"SMS_20375006",
	"Code":"OK"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Dysmsapi)

