# DeleteLivePullStreamInfoConfig {#concept_57735_zh .concept}

删除拉流信息。

## 请求参数 {#section_k4f_qm1_dfb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|Action|String|是|DeleteLivePullStreamInfoConfig|系统规定参数。取值：DeleteLivePullStreamInfoConfig|
|AppName|String|是|testApp|直播流所属应用名称。|
|DomainName|String|是|www.yourdomain.com|您的拉流域名。|
|StreamName|String|是|testStream|直播流名。|

## 返回参数 {#section_p4f_qm1_dfb .section}

|名称|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|40A4F36D-A7CC-473A-88E7-154F92242566|该条任务请求ID|

## 示例 {#section_zcx_4j1_dfb .section}

请求示例

```
 https://live.aliyuncs.com?Action=DeleteLivePullStreamInfo&DomainName=test101.pulllive.com&AppName=xxx&StreamName=xxx&SourceUrl=xxxx&Always=yes&<公共请求参数>
```

正常返回示例

JSON格式

```
{
    "RequestId":"16A96B9A-F203-4EC5-8E43-CB92E68F4CD8"
}
```

异常返回示例

JSON格式

```
{
    "Code":"InternalError",
    "HostId":"live.aliyuncs.com",
    "Message":"The request processing has failed due to some unknown error.",
    "RequestId":"6EBD1AC4-C34D-4AE1-963E-B688A228BE31"
}
```

## 错误码 {#section_v4f_qm1_dfb .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/live)

