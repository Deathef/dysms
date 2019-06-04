# DeleteSmsSign {#doc_api_Dysmsapi_DeleteSmsSign .reference}

调用接口DeleteSmsSign删除短信签名。

**注意**：

-   不支持删除正在审核中的签名。
-   短信签名删除后不可恢复，请谨慎操作。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Dysmsapi&api=DeleteSmsSign)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|SignName|String|是|阿里云|短信签名。

 **说明：** 必须是本账号已申请的短信签名。

 |
|AccessKeyId|String|否|LTAIP00vvvvvvvvv|主账号AccessKey的ID。

 |
|Action|String|否|DeleteSmsSign|系统规定参数。取值：**DeleteSmsSign**。

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
|SignName|String|阿里云|签名名称。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DeleteSmsSign
&SignName=阿里云
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteSmsSignResponse>
  <Message>OK</Message>
  <RequestId>F655A8D5-B967-440B-8683-DAD6FF8DE990</RequestId>
  <SignName>阿里云</SignName>
  <Code>OK</Code>
</DeleteSmsSignResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"SignName":"阿里云",
	"Message":"OK",
	"RequestId":"F655A8D5-B967-440B-8683-DAD6FF8DE990",
	"Code":"OK"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Dysmsapi)

