# immich_python_sdk.SyncApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_sync_ack**](SyncApi.md#delete_sync_ack) | **DELETE** /sync/ack | 
[**get_delta_sync**](SyncApi.md#get_delta_sync) | **POST** /sync/delta-sync | 
[**get_full_sync_for_user**](SyncApi.md#get_full_sync_for_user) | **POST** /sync/full-sync | 
[**get_sync_ack**](SyncApi.md#get_sync_ack) | **GET** /sync/ack | 
[**get_sync_stream**](SyncApi.md#get_sync_stream) | **POST** /sync/stream | 
[**send_sync_ack**](SyncApi.md#send_sync_ack) | **POST** /sync/ack | 


# **delete_sync_ack**
> delete_sync_ack(sync_ack_delete_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.sync_ack_delete_dto import SyncAckDeleteDto
from immich_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk.Configuration(
    host = "https://github.com/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: api_key
configuration.api_key['api_key'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Configure Bearer authorization (JWT): bearer
configuration = immich_python_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with immich_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk.SyncApi(api_client)
    sync_ack_delete_dto = immich_python_sdk.SyncAckDeleteDto() # SyncAckDeleteDto | 

    try:
        api_instance.delete_sync_ack(sync_ack_delete_dto)
    except Exception as e:
        print("Exception when calling SyncApi->delete_sync_ack: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sync_ack_delete_dto** | [**SyncAckDeleteDto**](SyncAckDeleteDto.md)|  | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_delta_sync**
> AssetDeltaSyncResponseDto get_delta_sync(asset_delta_sync_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_delta_sync_dto import AssetDeltaSyncDto
from immich_python_sdk.models.asset_delta_sync_response_dto import AssetDeltaSyncResponseDto
from immich_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk.Configuration(
    host = "https://github.com/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: api_key
configuration.api_key['api_key'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Configure Bearer authorization (JWT): bearer
configuration = immich_python_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with immich_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk.SyncApi(api_client)
    asset_delta_sync_dto = immich_python_sdk.AssetDeltaSyncDto() # AssetDeltaSyncDto | 

    try:
        api_response = api_instance.get_delta_sync(asset_delta_sync_dto)
        print("The response of SyncApi->get_delta_sync:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SyncApi->get_delta_sync: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_delta_sync_dto** | [**AssetDeltaSyncDto**](AssetDeltaSyncDto.md)|  | 

### Return type

[**AssetDeltaSyncResponseDto**](AssetDeltaSyncResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_full_sync_for_user**
> List[AssetResponseDto] get_full_sync_for_user(asset_full_sync_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_full_sync_dto import AssetFullSyncDto
from immich_python_sdk.models.asset_response_dto import AssetResponseDto
from immich_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk.Configuration(
    host = "https://github.com/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: api_key
configuration.api_key['api_key'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Configure Bearer authorization (JWT): bearer
configuration = immich_python_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with immich_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk.SyncApi(api_client)
    asset_full_sync_dto = immich_python_sdk.AssetFullSyncDto() # AssetFullSyncDto | 

    try:
        api_response = api_instance.get_full_sync_for_user(asset_full_sync_dto)
        print("The response of SyncApi->get_full_sync_for_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SyncApi->get_full_sync_for_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_full_sync_dto** | [**AssetFullSyncDto**](AssetFullSyncDto.md)|  | 

### Return type

[**List[AssetResponseDto]**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sync_ack**
> List[SyncAckDto] get_sync_ack()

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.sync_ack_dto import SyncAckDto
from immich_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk.Configuration(
    host = "https://github.com/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: api_key
configuration.api_key['api_key'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Configure Bearer authorization (JWT): bearer
configuration = immich_python_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with immich_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk.SyncApi(api_client)

    try:
        api_response = api_instance.get_sync_ack()
        print("The response of SyncApi->get_sync_ack:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SyncApi->get_sync_ack: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[SyncAckDto]**](SyncAckDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sync_stream**
> get_sync_stream(sync_stream_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.sync_stream_dto import SyncStreamDto
from immich_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk.Configuration(
    host = "https://github.com/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: api_key
configuration.api_key['api_key'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Configure Bearer authorization (JWT): bearer
configuration = immich_python_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with immich_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk.SyncApi(api_client)
    sync_stream_dto = immich_python_sdk.SyncStreamDto() # SyncStreamDto | 

    try:
        api_instance.get_sync_stream(sync_stream_dto)
    except Exception as e:
        print("Exception when calling SyncApi->get_sync_stream: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sync_stream_dto** | [**SyncStreamDto**](SyncStreamDto.md)|  | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_sync_ack**
> send_sync_ack(sync_ack_set_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.sync_ack_set_dto import SyncAckSetDto
from immich_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk.Configuration(
    host = "https://github.com/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: api_key
configuration.api_key['api_key'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Configure Bearer authorization (JWT): bearer
configuration = immich_python_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with immich_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk.SyncApi(api_client)
    sync_ack_set_dto = immich_python_sdk.SyncAckSetDto() # SyncAckSetDto | 

    try:
        api_instance.send_sync_ack(sync_ack_set_dto)
    except Exception as e:
        print("Exception when calling SyncApi->send_sync_ack: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sync_ack_set_dto** | [**SyncAckSetDto**](SyncAckSetDto.md)|  | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

