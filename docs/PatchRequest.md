# PatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_info** | Option<**serde_json::Value**> | 新的 apiInfo。 | [optional]
**cors** | Option<[**models::CorsConfig**](CorsConfig.md)> | 新的跨域配置；缺省表示不修改。 | [optional]
**probe** | Option<[**models::ProbeConfig**](ProbeConfig.md)> | 新的探活配置。 | [optional]
**project_root** | Option<**String**> | 新的项目根目录。 | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
