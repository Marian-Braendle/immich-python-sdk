# immich_python_sdk.LibrariesApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_library**](LibrariesApi.md#create_library) | **POST** /libraries | 
[**delete_library**](LibrariesApi.md#delete_library) | **DELETE** /libraries/{id} | 
[**get_all_libraries**](LibrariesApi.md#get_all_libraries) | **GET** /libraries | 
[**get_library**](LibrariesApi.md#get_library) | **GET** /libraries/{id} | 
[**get_library_statistics**](LibrariesApi.md#get_library_statistics) | **GET** /libraries/{id}/statistics | 
[**scan_library**](LibrariesApi.md#scan_library) | **POST** /libraries/{id}/scan | 
[**update_library**](LibrariesApi.md#update_library) | **PUT** /libraries/{id} | 
[**validate**](LibrariesApi.md#validate) | **POST** /libraries/{id}/validate | 


# **create_library**
> LibraryResponseDto create_library(create_library_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.create_library_dto import CreateLibraryDto
from immich_python_sdk.models.library_response_dto import LibraryResponseDto
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)
    create_library_dto = immich_python_sdk.CreateLibraryDto() # CreateLibraryDto | 

    try:
        api_response = api_instance.create_library(create_library_dto)
        print("The response of LibrariesApi->create_library:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LibrariesApi->create_library: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_library_dto** | [**CreateLibraryDto**](CreateLibraryDto.md)|  | 

### Return type

[**LibraryResponseDto**](LibraryResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_library**
> delete_library(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)
    id = 'id_example' # str | 

    try:
        api_instance.delete_library(id)
    except Exception as e:
        print("Exception when calling LibrariesApi->delete_library: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_libraries**
> List[LibraryResponseDto] get_all_libraries()

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.library_response_dto import LibraryResponseDto
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)

    try:
        api_response = api_instance.get_all_libraries()
        print("The response of LibrariesApi->get_all_libraries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LibrariesApi->get_all_libraries: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[LibraryResponseDto]**](LibraryResponseDto.md)

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

# **get_library**
> LibraryResponseDto get_library(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.library_response_dto import LibraryResponseDto
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = api_instance.get_library(id)
        print("The response of LibrariesApi->get_library:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LibrariesApi->get_library: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**LibraryResponseDto**](LibraryResponseDto.md)

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

# **get_library_statistics**
> LibraryStatsResponseDto get_library_statistics(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.library_stats_response_dto import LibraryStatsResponseDto
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = api_instance.get_library_statistics(id)
        print("The response of LibrariesApi->get_library_statistics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LibrariesApi->get_library_statistics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**LibraryStatsResponseDto**](LibraryStatsResponseDto.md)

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

# **scan_library**
> scan_library(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)
    id = 'id_example' # str | 

    try:
        api_instance.scan_library(id)
    except Exception as e:
        print("Exception when calling LibrariesApi->scan_library: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_library**
> LibraryResponseDto update_library(id, update_library_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.library_response_dto import LibraryResponseDto
from immich_python_sdk.models.update_library_dto import UpdateLibraryDto
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)
    id = 'id_example' # str | 
    update_library_dto = immich_python_sdk.UpdateLibraryDto() # UpdateLibraryDto | 

    try:
        api_response = api_instance.update_library(id, update_library_dto)
        print("The response of LibrariesApi->update_library:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LibrariesApi->update_library: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_library_dto** | [**UpdateLibraryDto**](UpdateLibraryDto.md)|  | 

### Return type

[**LibraryResponseDto**](LibraryResponseDto.md)

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

# **validate**
> ValidateLibraryResponseDto validate(id, validate_library_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.validate_library_dto import ValidateLibraryDto
from immich_python_sdk.models.validate_library_response_dto import ValidateLibraryResponseDto
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
    api_instance = immich_python_sdk.LibrariesApi(api_client)
    id = 'id_example' # str | 
    validate_library_dto = immich_python_sdk.ValidateLibraryDto() # ValidateLibraryDto | 

    try:
        api_response = api_instance.validate(id, validate_library_dto)
        print("The response of LibrariesApi->validate:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LibrariesApi->validate: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **validate_library_dto** | [**ValidateLibraryDto**](ValidateLibraryDto.md)|  | 

### Return type

[**ValidateLibraryResponseDto**](ValidateLibraryResponseDto.md)

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

