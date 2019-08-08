# API概览 {#concept_t4w_pcs_ggb .concept}

本文档为您展示短信服务所有可调用的API接口，详细接口信息请参见对应接口文档。

更多 API 资源，请访问 [OpenAPI Explorer](https://api.aliyun.com/)。

## 短信发送接口 {#section_ix1_xcs_ggb .section}

|API|描述|
|:--|:-|
|[SendSms](cn.zh-CN/API参考/发送短信/SendSms.md)|发送短信。|
|[SendBatchSms](cn.zh-CN/API参考/发送短信/SendBatchSms.md)|批量发送短信。|

## 短信查询接口 {#section_ktk_xcs_ggb .section}

|API|描述|
|:--|:-|
|[QuerySendDetails](cn.zh-CN/API参考/查询发送记录/QuerySendDetails.md)|查询短信发送的状态。|

## 签名申请接口 {#section_qaw_3mh_6jl .section}

|API|描述|
|---|--|
|[AddSmsSign](cn.zh-CN/API参考/短信签名/AddSmsSign.md#)|调用短信AddSmsSign申请短信签名。|
|[DeleteSmsSign](cn.zh-CN/API参考/短信签名/DeleteSmsSign.md#)|调用接口DeleteSmsSign删除短信签名。|
|[QuerySmsSign](cn.zh-CN/API参考/短信签名/QuerySmsSign.md#)|调用接口QuerySmsSign查询短信签名申请状态。|
|[ModifySmsSign](cn.zh-CN/API参考/短信签名/ModifySmsSign.md#)|调用接口ModifySmsSign修改未审核通过的短信签名，并重新提交审核。|

## 模板申请接口 {#section_sa6_4zm_r8o .section}

|API|描述|
|---|--|
|[ModifySmsTemplate](cn.zh-CN/API参考/短信模板/ModifySmsTemplate.md#)|调用接口ModifySmsTemplate修改未通过审核的短信模板。|
|[QuerySmsTemplate](cn.zh-CN/API参考/短信模板/QuerySmsTemplate.md#)|调用接口QuerySmsTemplate查询短信模板的审核状态。|
|[AddSmsTemplate](cn.zh-CN/API参考/短信模板/AddSmsTemplate.md#)|调用接口AddSmsTemplate申请短信模板。|
|[DeleteSmsTemplate](cn.zh-CN/API参考/短信模板/DeleteSmsTemplate.md#)|调用接口DeleteSmsTemplate删除短信模板。|

## 回执消息 {#section_z1s_xcs_ggb .section}

|API|描述|
|:--|:-|
|[SmsReport](cn.zh-CN/API参考/回执消息/MNS消息队列消费模式/SmsReport.md)|订阅SmsReport短信状态报告，获取短信发送状态。|
|[SmsUp](cn.zh-CN/API参考/回执消息/MNS消息队列消费模式/SmsUp.md)|订阅SmsUp上行短信消息，获取终端用户回复短信的内容。|
|[SignSmsReport](cn.zh-CN/API参考/回执消息/模板和签名申请状态回执/SignSmsReport.md#)|订阅签名审核状态消息（SignSmsReport），获取指定签名的审核状态。|
|[TemplateSmsReport](cn.zh-CN/API参考/回执消息/模板和签名申请状态回执/TemplateSmsReport.md#)|订阅模板审核状态消息（TemplateSmsReport），获取指定模板的审核状态。|

