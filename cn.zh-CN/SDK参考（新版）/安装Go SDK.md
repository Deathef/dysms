# 安装Go SDK {#concept_nvv_r2b_fhb .concept}

可以通过直接安装依赖包的方式安装阿里云Go SDK。

**说明：** 无论通过何种方式安装Go SDK，都必须安装阿里云Go SDK核心库。

## 前提条件 {#section_csz_sfb_fhb .section}

在安装和使用阿里云SDK前，确保您已经注册阿里云账号并生成访问访问密钥（AccessKey）。详情参考[创建AccessKey](~~53045~~)。

## 安装方式 {#section_rjs_x3b_fhb .section}

您可以通过以下两种方式安装Go SDK。

-   [使用依赖包工具安装（推荐）](#)
-   [自行下载安装](#)

## 使用Glide安装GO SDK（推荐） {#section_rp1_5fb_fhb .section}

执行以下命令，安装阿里云Go SDK：

```
glide get github.com/aliyun/alibaba-cloud-sdk-go
```

在安装完成后，您可以使用[OpenAPI Explorer](https://api.aliyun.com/#/?product=Dysmsapi&lang=GO)来生成相关API的Demo并应用在您的项目中。

## 使用Govendor安装 {#section_nkm_vfb_fhb .section}

执行以下命令，安装阿里云Go SDK：

```
go get -u github.com/aliyun/alibaba-cloud-sdk-go/sdk
```

在安装完成后，您可以使用[OpenAPI Explorer](https://api.aliyun.com/#/?product=Dysmsapi&lang=GO)来生成相关API的Demo并应用在您的项目中。

## Go SDK GitHub地址 {#section_fbm_lzg_fhb .section}

[Go SDK核心库](https://github.com/aliyun/alibaba-cloud-sdk-go/)

