# \ServicesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_service_cors**](ServicesApi.md#delete_service_cors) | **DELETE** /gw/services/{serviceName}/cors | `DELETE /gw/services/{serviceName}/cors`
[**get_service**](ServicesApi.md#get_service) | **GET** /gw/services/{serviceName} | `GET /gw/services/{serviceName}`
[**get_service_api_info**](ServicesApi.md#get_service_api_info) | **GET** /gw/services/{serviceName}/api-info | `GET /gw/services/{serviceName}/api-info`
[**list_services**](ServicesApi.md#list_services) | **GET** /gw/services | `GET /gw/services`
[**patch_service**](ServicesApi.md#patch_service) | **PATCH** /gw/services/{serviceName} | `PATCH /gw/services/{serviceName}`
[**put_service_cors**](ServicesApi.md#put_service_cors) | **PUT** /gw/services/{serviceName}/cors | `PUT /gw/services/{serviceName}/cors`
[**register_service**](ServicesApi.md#register_service) | **PUT** /gw/services/{serviceName} | `PUT /gw/services/{serviceName}`
[**unregister_service**](ServicesApi.md#unregister_service) | **DELETE** /gw/services/{serviceName} | `DELETE /gw/services/{serviceName}`



## delete_service_cors

> delete_service_cors(service_name)
`DELETE /gw/services/{serviceName}/cors`

清空跨域配置，恢复为完全透传 provider 的 CORS 头。幂等：未配置时同样返回 204。

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_name** | **String** | 服务名 | [required] |

### Return type

 (empty response body)

### Authorization

[bearer_auth](../README.md#bearer_auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_service

> models::ServiceDetail get_service(service_name)
`GET /gw/services/{serviceName}`

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_name** | **String** | 服务名 | [required] |

### Return type

[**models::ServiceDetail**](ServiceDetail.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_service_api_info

> serde_json::Value get_service_api_info(service_name)
`GET /gw/services/{serviceName}/api-info`

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_name** | **String** | 服务名 | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/vnd.oai.openapi+json, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_services

> models::ServiceListResponse list_services(name_contains, page, limit, fields)
`GET /gw/services`

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**name_contains** | Option<**String**> | 服务名子串，大小写不敏感 |  |
**page** | Option<**i32**> | 页码，从 1 开始 |  |
**limit** | Option<**i32**> | 每页数量，默认 20，上限 200 |  |
**fields** | Option<**String**> | 扩展字段：apiInfo,projectRoot |  |

### Return type

[**models::ServiceListResponse**](ServiceListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## patch_service

> models::RegistrationResponse patch_service(service_name, patch_request)
`PATCH /gw/services/{serviceName}`

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_name** | **String** | 服务名 | [required] |
**patch_request** | [**PatchRequest**](PatchRequest.md) |  | [required] |

### Return type

[**models::RegistrationResponse**](RegistrationResponse.md)

### Authorization

[bearer_auth](../README.md#bearer_auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## put_service_cors

> models::CorsResponse put_service_cors(service_name, cors_config)
`PUT /gw/services/{serviceName}/cors`

用整份配置替换该服务的跨域设置。`{\"allowAll\": true}` 即可一键放行所有域； 配置在代理面立即生效，预检由网关直接应答。

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_name** | **String** | 服务名 | [required] |
**cors_config** | [**CorsConfig**](CorsConfig.md) |  | [required] |

### Return type

[**models::CorsResponse**](CorsResponse.md)

### Authorization

[bearer_auth](../README.md#bearer_auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## register_service

> models::RegistrationResponse register_service(service_name, register_request)
`PUT /gw/services/{serviceName}`

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_name** | **String** | 服务名 | [required] |
**register_request** | [**RegisterRequest**](RegisterRequest.md) |  | [required] |

### Return type

[**models::RegistrationResponse**](RegistrationResponse.md)

### Authorization

[bearer_auth](../README.md#bearer_auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unregister_service

> unregister_service(service_name)
`DELETE /gw/services/{serviceName}`

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_name** | **String** | 服务名 | [required] |

### Return type

 (empty response body)

### Authorization

[bearer_auth](../README.md#bearer_auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
