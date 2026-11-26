# ServiceDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cors** | Option<[**models::CorsConfig**](CorsConfig.md)> | 跨域配置；未配置时不返回该字段。 | [optional]
**endpoints** | **Vec<String>** | apiInfo 中声明的路径，排序后返回。 |
**last_probe** | Option<**String**> | 最近一次探测时间。 | [optional]
**name** | **String** | 服务名。 |
**notify_url** | Option<**String**> | 端口变更通知地址。 | [optional]
**owner** | [**models::OwnerSummary**](OwnerSummary.md) | owner 摘要。 |
**port** | **i32** | provider 端口。 |
**probe** | [**models::ProbeConfig**](ProbeConfig.md) | 探活配置。 |
**project_root** | Option<**String**> | provider 项目根目录。 | [optional]
**protocol** | [**models::Protocol**](Protocol.md) | 协议。 |
**revision** | **i64** | 单服务 revision。 |
**status** | [**models::ServiceStatus**](ServiceStatus.md) | 当前状态。 |
**updated_at** | **String** | 最近更新时间。 |
**version** | **String** | provider 版本。 |

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
