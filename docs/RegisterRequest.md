# RegisterRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_info** | Option<**serde_json::Value**> | provider 的 OpenAPI 文档，可后补。 | [optional]
**notify_url** | Option<**String**> | 端口变更时的定向通知地址。 | [optional]
**port** | **i32** | provider 监听端口。 |
**probe** | Option<[**models::ProbeConfig**](ProbeConfig.md)> | 探活配置；`probe.path` 必填。 | [optional]
**project_root** | Option<**String**> | provider 项目根目录。 | [optional]
**protocol** | Option<[**models::Protocol**](Protocol.md)> | 协议，缺省为 `http`。 | [optional]
**version** | **String** | provider 版本。 |

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
