# immich_python_sdk_asyncio.TrashApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**empty_trash**](TrashApi.md#empty_trash) | **POST** /trash/empty | 
[**restore_assets**](TrashApi.md#restore_assets) | **POST** /trash/restore/assets | 
[**restore_trash**](TrashApi.md#restore_trash) | **POST** /trash/restore | 


# **empty_trash**
> TrashResponseDto empty_trash()

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.trash_response_dto import TrashResponseDto
from immich_python_sdk_asyncio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk_asyncio.Configuration(
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
configuration = immich_python_sdk_asyncio.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
async with immich_python_sdk_asyncio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk_asyncio.TrashApi(api_client)

    try:
        api_response = await api_instance.empty_trash()
        print("The response of TrashApi->empty_trash:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TrashApi->empty_trash: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**TrashResponseDto**](TrashResponseDto.md)

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

# **restore_assets**
> TrashResponseDto restore_assets(bulk_ids_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.bulk_ids_dto import BulkIdsDto
from immich_python_sdk_asyncio.models.trash_response_dto import TrashResponseDto
from immich_python_sdk_asyncio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk_asyncio.Configuration(
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
configuration = immich_python_sdk_asyncio.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
async with immich_python_sdk_asyncio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk_asyncio.TrashApi(api_client)
    bulk_ids_dto = immich_python_sdk_asyncio.BulkIdsDto() # BulkIdsDto | 

    try:
        api_response = await api_instance.restore_assets(bulk_ids_dto)
        print("The response of TrashApi->restore_assets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TrashApi->restore_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_ids_dto** | [**BulkIdsDto**](BulkIdsDto.md)|  | 

### Return type

[**TrashResponseDto**](TrashResponseDto.md)

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

# **restore_trash**
> TrashResponseDto restore_trash()

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.trash_response_dto import TrashResponseDto
from immich_python_sdk_asyncio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://github.com/api
# See configuration.py for a list of all supported configuration parameters.
configuration = immich_python_sdk_asyncio.Configuration(
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
configuration = immich_python_sdk_asyncio.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
async with immich_python_sdk_asyncio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immich_python_sdk_asyncio.TrashApi(api_client)

    try:
        api_response = await api_instance.restore_trash()
        print("The response of TrashApi->restore_trash:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TrashApi->restore_trash: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**TrashResponseDto**](TrashResponseDto.md)

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

