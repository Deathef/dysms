# QuerySmsSign {#doc_api_Dysmsapi_QuerySmsSign .reference}

调用接口QuerySmsSign查询短信签名申请状态。

申请短信签名后，您可以在控制台或通过接口**QuerySmsSign**查看短信签名的申请状态。如果未通过审核，接口会返回未通过审核的原因，请针对具体原因修改签名并重新提交审核。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Dysmsapi&api=QuerySmsSign)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|SignName|String|是|阿里云|签名名称。

 |
|AccessKeyId|String|否|LTAIP00vvvvvvvvv|主账号AccessKey的ID。

 |
|Action|String|否|QuerySmsSign|系统规定参数。取值：**QuerySmsSign**。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|请求状态码。

 -   返回OK代表请求成功。
-   其他错误码详见[错误码列表](~~101346~~)。

 |
|CreateDate|String| 2019-01-08 16:44:13|短信签名的创建日期和时间。

 |
|Message|String|OK|状态码描述。

 |
|Reason|String|文件不能证明信息真实性，请重新上传|审核备注。

 -   如果审核状态为**审核通过**或**审核中**，参数Reason显示为“无审核备注”。
-   如果审核状态为**审核未通过**，参数Reason显示审核的具体原因。

 |
|RequestId|String|CC89A90C-978F-46AC-B80D-54738371E7CA|请求ID。

 |
|SignName|String|阿里云|短信签名。

 |
|SignStatus|Integer|1|签名审核状态。其中：

 -   0：审核中。
-   1：审核通过。
-   2：审核失败，请在返回参数Reason中查看审核失败原因。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://dysmsapi.aliyuncs.com//?Action=QuerySmsSign
&SignName=阿里云
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<QuerySmsSignResponse>
  <Message>OK</Message>
  <RequestId>CC89A90C-978F-46AC-B80D-54738371E7CA</RequestId>
  <SignStatus>1</SignStatus>
  <CreateDate>2019-01-08 16:44:13</CreateDate>
  <Code>OK</Code>
  <SignName>阿里云</SignName>
  <Reason>文件不能证明信息真实性，请重新上传</Reason>
</QuerySmsSignResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"SignName":"阿里云",
	"Message":"OK",
	"RequestId":"CC89A90C-978F-46AC-B80D-54738371E7CA",
	"Code":"OK",
	"CreateDate":" 2019-01-08 16:44:13",
	"Reason":"文件不能证明信息真实性，请重新上传",
	"SignStatus":1
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Dysmsapi)

