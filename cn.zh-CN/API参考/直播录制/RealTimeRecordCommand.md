# RealTimeRecordCommand {#concept_85907_zh .concept}

您可以通过手动录制接口按需完成手动录制。例如，动态地启动、停止录制 。

## 请求参数 {#section_k4f_qm1_dfb .section}

|参数|类型|是否必选|描述|
|:-|:-|:---|:-|
|Action|String|是|系统规定参数。取值：RealTimeRecordCommand|
|Command|String|是|操作行为。支持start、stop两种类型。|
|DomainName|String|是|您的加速域名。|
|AppName|String|是|App名。|
|StreamName|String|是|直播流名。|

## 返回参数 {#section_p4f_qm1_dfb .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|该条任务请求ID|

## 示例 {#section_zcx_4j1_dfb .section}

请求示例

```
 https://live.aliyuncs.com?Action=RealTimeRecordCommand&DomainName=test101.cdnpe.com&AppName=abc&StreamName=s1&Command=start<公共请求参数>
```

返回示例

JSON格式

```
{
    "RequestId": "16A96B9A-F203-4EC5-8E43-CB92E68F4CD8"
}
```

## 特殊错误码 {#section_v4f_qm1_dfb .section}

|错误代码|错误信息|Http 状态码|语义|
|:---|:---|:-------|:-|
|InvalidDomain.NotFound|The domain provided does not exist in our records.|404|当前账户下未查到域名|
|MissingDomainName|DomainName is mandatory for this action.|400|缺少DomainName值|
|MissingAppName|AppName is mandatory for this action.|400|缺少AppName值|
|MissingStreamName|StreamName is mandatory for this action.|400|缺少StreamName值|
|MissingCommand|Command is mandatory for this Command.|400|缺少Command值|
|InvalidStream.NotFound|Stream does not exist.|404|流不存在|
|InvalidConfig.NotFound|Config does not exist.|404|配置不存在|
|TaskAlreadyStarted|Task has already started.|409|录制任务已经启动|
|InternalError|The request processing has failed due to some unknown error, exception or failure.|500|内部错误|

您可以查询本产品通用错误码。参见 [通用错误码](https://error-center.aliyun.com/status/product/live?spm=5176.10421674.home.18.186bTEI0TEI0DK)。

