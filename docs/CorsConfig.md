# CorsConfig

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_all** | Option<**bool**> | 一键放行所有来源、方法与请求头。 | [optional]
**allow_credentials** | Option<**bool**> | 是否允许携带凭据（Cookie / `Authorization`）。 | [optional]
**allow_headers** | Option<**Vec<String>**> | 允许的请求头；为空表示回显预检请求声明的请求头。 | [optional]
**allow_methods** | Option<**Vec<String>**> | 允许的方法；为空表示回显预检请求声明的方法。 | [optional]
**allow_origins** | Option<**Vec<String>**> | 允许的来源，例如 `http://localhost:5173`；支持 `*` 与 `null`。 | [optional]
**expose_headers** | Option<**Vec<String>**> | 暴露给浏览器的响应头。 | [optional]
**max_age_seconds** | Option<**i64**> | 预检结果缓存秒数；`None` 时不发送 `Access-Control-Max-Age`。 | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
