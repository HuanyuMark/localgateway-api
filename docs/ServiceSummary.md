# ServiceSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_info** | Option<**serde_json::Value**> | 仅当 `fields=apiInfo` 时返回。 | [optional]
**last_probe** | Option<**String**> | 最近一次探测时间。 | [optional]
**name** | **String** | 服务名。 |
**probe** | **String** | 探活路径。 |
**project_root** | Option<**String**> | 仅当 `fields=projectRoot` 时返回。 | [optional]
**protocol** | [**models::Protocol**](Protocol.md) | 协议。 |
**revision** | **i64** | 单服务 revision。 |
**status** | [**models::ServiceStatus**](ServiceStatus.md) | 状态。 |
**version** | **String** | provider 版本。 |

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
