# \GatewayApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_session**](GatewayApi.md#create_session) | **POST** /gw/session | `POST /gw/session`
[**get_health**](GatewayApi.md#get_health) | **GET** /gw/health | `GET /gw/health`
[**get_open_api_document**](GatewayApi.md#get_open_api_document) | **GET** /gw/openapi.json | `GET /gw/openapi.json`
[**shutdown_gateway**](GatewayApi.md#shutdown_gateway) | **POST** /gw/shutdown | `POST /gw/shutdown`
[**stream_events**](GatewayApi.md#stream_events) | **GET** /gw/events | `GET /gw/events`



## create_session

> models::SessionResponse create_session()
`POST /gw/session`

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::SessionResponse**](SessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_health

> models::HealthResponse get_health()
`GET /gw/health`

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::HealthResponse**](HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_open_api_document

> serde_json::Value get_open_api_document()
`GET /gw/openapi.json`

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## shutdown_gateway

> shutdown_gateway(shutdown_request)
`POST /gw/shutdown`

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**shutdown_request** | Option<[**ShutdownRequest**](ShutdownRequest.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[bearer_auth](../README.md#bearer_auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## stream_events

> String stream_events()
`GET /gw/events`

### Parameters

This endpoint does not need any parameter.

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/event-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
