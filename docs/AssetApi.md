# immich_python_sdk.AssetApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_bulk_upload**](AssetApi.md#check_bulk_upload) | **POST** /asset/bulk-upload-check | 
[**check_existing_assets**](AssetApi.md#check_existing_assets) | **POST** /asset/exist | 
[**delete_assets**](AssetApi.md#delete_assets) | **DELETE** /asset | 
[**download_archive**](AssetApi.md#download_archive) | **POST** /asset/download/archive | 
[**download_file**](AssetApi.md#download_file) | **POST** /asset/download/{id} | 
[**empty_trash**](AssetApi.md#empty_trash) | **POST** /asset/trash/empty | 
[**get_all_assets**](AssetApi.md#get_all_assets) | **GET** /asset | 
[**get_all_user_assets_by_device_id**](AssetApi.md#get_all_user_assets_by_device_id) | **GET** /asset/device/{deviceId} | 
[**get_asset_by_id**](AssetApi.md#get_asset_by_id) | **GET** /asset/assetById/{id} | 
[**get_asset_search_terms**](AssetApi.md#get_asset_search_terms) | **GET** /asset/search-terms | 
[**get_asset_statistics**](AssetApi.md#get_asset_statistics) | **GET** /asset/statistics | 
[**get_asset_thumbnail**](AssetApi.md#get_asset_thumbnail) | **GET** /asset/thumbnail/{id} | 
[**get_curated_locations**](AssetApi.md#get_curated_locations) | **GET** /asset/curated-locations | 
[**get_curated_objects**](AssetApi.md#get_curated_objects) | **GET** /asset/curated-objects | 
[**get_download_info**](AssetApi.md#get_download_info) | **POST** /asset/download/info | 
[**get_map_markers**](AssetApi.md#get_map_markers) | **GET** /asset/map-marker | 
[**get_memory_lane**](AssetApi.md#get_memory_lane) | **GET** /asset/memory-lane | 
[**get_random**](AssetApi.md#get_random) | **GET** /asset/random | 
[**get_time_bucket**](AssetApi.md#get_time_bucket) | **GET** /asset/time-bucket | 
[**get_time_buckets**](AssetApi.md#get_time_buckets) | **GET** /asset/time-buckets | 
[**get_user_assets_by_device_id**](AssetApi.md#get_user_assets_by_device_id) | **GET** /asset/{deviceId} | Use /asset/device/:deviceId instead - Remove in 1.92 release
[**restore_assets**](AssetApi.md#restore_assets) | **POST** /asset/restore | 
[**restore_trash**](AssetApi.md#restore_trash) | **POST** /asset/trash/restore | 
[**run_asset_jobs**](AssetApi.md#run_asset_jobs) | **POST** /asset/jobs | 
[**search_assets**](AssetApi.md#search_assets) | **GET** /assets | 
[**serve_file**](AssetApi.md#serve_file) | **GET** /asset/file/{id} | 
[**update_asset**](AssetApi.md#update_asset) | **PUT** /asset/{id} | 
[**update_assets**](AssetApi.md#update_assets) | **PUT** /asset | 
[**update_stack_parent**](AssetApi.md#update_stack_parent) | **PUT** /asset/stack/parent | 
[**upload_file**](AssetApi.md#upload_file) | **POST** /asset/upload | 


# **check_bulk_upload**
> AssetBulkUploadCheckResponseDto check_bulk_upload(asset_bulk_upload_check_dto)

Checks if assets exist by checksums

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_bulk_upload_check_dto import AssetBulkUploadCheckDto
from immich_python_sdk.models.asset_bulk_upload_check_response_dto import AssetBulkUploadCheckResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    asset_bulk_upload_check_dto = immich_python_sdk.AssetBulkUploadCheckDto() # AssetBulkUploadCheckDto | 

    try:
        api_response = api_instance.check_bulk_upload(asset_bulk_upload_check_dto)
        print("The response of AssetApi->check_bulk_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->check_bulk_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_bulk_upload_check_dto** | [**AssetBulkUploadCheckDto**](AssetBulkUploadCheckDto.md)|  | 

### Return type

[**AssetBulkUploadCheckResponseDto**](AssetBulkUploadCheckResponseDto.md)

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

# **check_existing_assets**
> CheckExistingAssetsResponseDto check_existing_assets(check_existing_assets_dto)

Checks if multiple assets exist on the server and returns all existing - used by background backup

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.check_existing_assets_dto import CheckExistingAssetsDto
from immich_python_sdk.models.check_existing_assets_response_dto import CheckExistingAssetsResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    check_existing_assets_dto = immich_python_sdk.CheckExistingAssetsDto() # CheckExistingAssetsDto | 

    try:
        api_response = api_instance.check_existing_assets(check_existing_assets_dto)
        print("The response of AssetApi->check_existing_assets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->check_existing_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **check_existing_assets_dto** | [**CheckExistingAssetsDto**](CheckExistingAssetsDto.md)|  | 

### Return type

[**CheckExistingAssetsResponseDto**](CheckExistingAssetsResponseDto.md)

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

# **delete_assets**
> delete_assets(asset_bulk_delete_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_bulk_delete_dto import AssetBulkDeleteDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    asset_bulk_delete_dto = immich_python_sdk.AssetBulkDeleteDto() # AssetBulkDeleteDto | 

    try:
        api_instance.delete_assets(asset_bulk_delete_dto)
    except Exception as e:
        print("Exception when calling AssetApi->delete_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_bulk_delete_dto** | [**AssetBulkDeleteDto**](AssetBulkDeleteDto.md)|  | 

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

# **download_archive**
> bytearray download_archive(asset_ids_dto, key=key)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_ids_dto import AssetIdsDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    asset_ids_dto = immich_python_sdk.AssetIdsDto() # AssetIdsDto | 
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.download_archive(asset_ids_dto, key=key)
        print("The response of AssetApi->download_archive:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->download_archive: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_ids_dto** | [**AssetIdsDto**](AssetIdsDto.md)|  | 
 **key** | **str**|  | [optional] 

### Return type

**bytearray**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_file**
> bytearray download_file(id, key=key)

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
    api_instance = immich_python_sdk.AssetApi(api_client)
    id = 'id_example' # str | 
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.download_file(id, key=key)
        print("The response of AssetApi->download_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->download_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **key** | **str**|  | [optional] 

### Return type

**bytearray**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **empty_trash**
> empty_trash()

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
    api_instance = immich_python_sdk.AssetApi(api_client)

    try:
        api_instance.empty_trash()
    except Exception as e:
        print("Exception when calling AssetApi->empty_trash: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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

# **get_all_assets**
> List[AssetResponseDto] get_all_assets(skip=skip, take=take, user_id=user_id, is_favorite=is_favorite, is_archived=is_archived, updated_after=updated_after, updated_before=updated_before, if_none_match=if_none_match)

Get all AssetEntity belong to the user

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    skip = 56 # int |  (optional)
    take = 56 # int |  (optional)
    user_id = 'user_id_example' # str |  (optional)
    is_favorite = True # bool |  (optional)
    is_archived = True # bool |  (optional)
    updated_after = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    updated_before = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    if_none_match = 'if_none_match_example' # str | ETag of data already cached on the client (optional)

    try:
        api_response = api_instance.get_all_assets(skip=skip, take=take, user_id=user_id, is_favorite=is_favorite, is_archived=is_archived, updated_after=updated_after, updated_before=updated_before, if_none_match=if_none_match)
        print("The response of AssetApi->get_all_assets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_all_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **skip** | **int**|  | [optional] 
 **take** | **int**|  | [optional] 
 **user_id** | **str**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_archived** | **bool**|  | [optional] 
 **updated_after** | **datetime**|  | [optional] 
 **updated_before** | **datetime**|  | [optional] 
 **if_none_match** | **str**| ETag of data already cached on the client | [optional] 

### Return type

[**List[AssetResponseDto]**](AssetResponseDto.md)

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

# **get_all_user_assets_by_device_id**
> List[str] get_all_user_assets_by_device_id(device_id)

Get all asset of a device that are in the database, ID only.

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
    api_instance = immich_python_sdk.AssetApi(api_client)
    device_id = 'device_id_example' # str | 

    try:
        api_response = api_instance.get_all_user_assets_by_device_id(device_id)
        print("The response of AssetApi->get_all_user_assets_by_device_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_all_user_assets_by_device_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_id** | **str**|  | 

### Return type

**List[str]**

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

# **get_asset_by_id**
> AssetResponseDto get_asset_by_id(id, key=key)

Get a single asset's information

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    id = 'id_example' # str | 
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.get_asset_by_id(id, key=key)
        print("The response of AssetApi->get_asset_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_asset_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **key** | **str**|  | [optional] 

### Return type

[**AssetResponseDto**](AssetResponseDto.md)

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

# **get_asset_search_terms**
> List[str] get_asset_search_terms()

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
    api_instance = immich_python_sdk.AssetApi(api_client)

    try:
        api_response = api_instance.get_asset_search_terms()
        print("The response of AssetApi->get_asset_search_terms:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_asset_search_terms: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**List[str]**

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

# **get_asset_statistics**
> AssetStatsResponseDto get_asset_statistics(is_archived=is_archived, is_favorite=is_favorite, is_trashed=is_trashed)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_stats_response_dto import AssetStatsResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    is_archived = True # bool |  (optional)
    is_favorite = True # bool |  (optional)
    is_trashed = True # bool |  (optional)

    try:
        api_response = api_instance.get_asset_statistics(is_archived=is_archived, is_favorite=is_favorite, is_trashed=is_trashed)
        print("The response of AssetApi->get_asset_statistics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_asset_statistics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **is_archived** | **bool**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_trashed** | **bool**|  | [optional] 

### Return type

[**AssetStatsResponseDto**](AssetStatsResponseDto.md)

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

# **get_asset_thumbnail**
> bytearray get_asset_thumbnail(id, format=format, key=key)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.thumbnail_format import ThumbnailFormat
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    id = 'id_example' # str | 
    format = immich_python_sdk.ThumbnailFormat() # ThumbnailFormat |  (optional)
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.get_asset_thumbnail(id, format=format, key=key)
        print("The response of AssetApi->get_asset_thumbnail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_asset_thumbnail: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **format** | [**ThumbnailFormat**](.md)|  | [optional] 
 **key** | **str**|  | [optional] 

### Return type

**bytearray**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_curated_locations**
> List[CuratedLocationsResponseDto] get_curated_locations()

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.curated_locations_response_dto import CuratedLocationsResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)

    try:
        api_response = api_instance.get_curated_locations()
        print("The response of AssetApi->get_curated_locations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_curated_locations: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[CuratedLocationsResponseDto]**](CuratedLocationsResponseDto.md)

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

# **get_curated_objects**
> List[CuratedObjectsResponseDto] get_curated_objects()

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.curated_objects_response_dto import CuratedObjectsResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)

    try:
        api_response = api_instance.get_curated_objects()
        print("The response of AssetApi->get_curated_objects:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_curated_objects: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[CuratedObjectsResponseDto]**](CuratedObjectsResponseDto.md)

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

# **get_download_info**
> DownloadResponseDto get_download_info(download_info_dto, key=key)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.download_info_dto import DownloadInfoDto
from immich_python_sdk.models.download_response_dto import DownloadResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    download_info_dto = immich_python_sdk.DownloadInfoDto() # DownloadInfoDto | 
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.get_download_info(download_info_dto, key=key)
        print("The response of AssetApi->get_download_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_download_info: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **download_info_dto** | [**DownloadInfoDto**](DownloadInfoDto.md)|  | 
 **key** | **str**|  | [optional] 

### Return type

[**DownloadResponseDto**](DownloadResponseDto.md)

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

# **get_map_markers**
> List[MapMarkerResponseDto] get_map_markers(is_archived=is_archived, is_favorite=is_favorite, file_created_after=file_created_after, file_created_before=file_created_before)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.map_marker_response_dto import MapMarkerResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    is_archived = True # bool |  (optional)
    is_favorite = True # bool |  (optional)
    file_created_after = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    file_created_before = '2013-10-20T19:20:30+01:00' # datetime |  (optional)

    try:
        api_response = api_instance.get_map_markers(is_archived=is_archived, is_favorite=is_favorite, file_created_after=file_created_after, file_created_before=file_created_before)
        print("The response of AssetApi->get_map_markers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_map_markers: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **is_archived** | **bool**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **file_created_after** | **datetime**|  | [optional] 
 **file_created_before** | **datetime**|  | [optional] 

### Return type

[**List[MapMarkerResponseDto]**](MapMarkerResponseDto.md)

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

# **get_memory_lane**
> List[MemoryLaneResponseDto] get_memory_lane(day, month)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.memory_lane_response_dto import MemoryLaneResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    day = 56 # int | 
    month = 56 # int | 

    try:
        api_response = api_instance.get_memory_lane(day, month)
        print("The response of AssetApi->get_memory_lane:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_memory_lane: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **day** | **int**|  | 
 **month** | **int**|  | 

### Return type

[**List[MemoryLaneResponseDto]**](MemoryLaneResponseDto.md)

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

# **get_random**
> List[AssetResponseDto] get_random(count=count)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    count = 3.4 # float |  (optional)

    try:
        api_response = api_instance.get_random(count=count)
        print("The response of AssetApi->get_random:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_random: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **count** | **float**|  | [optional] 

### Return type

[**List[AssetResponseDto]**](AssetResponseDto.md)

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

# **get_time_bucket**
> List[AssetResponseDto] get_time_bucket(size, time_bucket, user_id=user_id, album_id=album_id, person_id=person_id, is_archived=is_archived, is_favorite=is_favorite, is_trashed=is_trashed, with_stacked=with_stacked, with_partners=with_partners, key=key)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_response_dto import AssetResponseDto
from immich_python_sdk.models.time_bucket_size import TimeBucketSize
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    size = immich_python_sdk.TimeBucketSize() # TimeBucketSize | 
    time_bucket = 'time_bucket_example' # str | 
    user_id = 'user_id_example' # str |  (optional)
    album_id = 'album_id_example' # str |  (optional)
    person_id = 'person_id_example' # str |  (optional)
    is_archived = True # bool |  (optional)
    is_favorite = True # bool |  (optional)
    is_trashed = True # bool |  (optional)
    with_stacked = True # bool |  (optional)
    with_partners = True # bool |  (optional)
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.get_time_bucket(size, time_bucket, user_id=user_id, album_id=album_id, person_id=person_id, is_archived=is_archived, is_favorite=is_favorite, is_trashed=is_trashed, with_stacked=with_stacked, with_partners=with_partners, key=key)
        print("The response of AssetApi->get_time_bucket:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_time_bucket: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **size** | [**TimeBucketSize**](.md)|  | 
 **time_bucket** | **str**|  | 
 **user_id** | **str**|  | [optional] 
 **album_id** | **str**|  | [optional] 
 **person_id** | **str**|  | [optional] 
 **is_archived** | **bool**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_trashed** | **bool**|  | [optional] 
 **with_stacked** | **bool**|  | [optional] 
 **with_partners** | **bool**|  | [optional] 
 **key** | **str**|  | [optional] 

### Return type

[**List[AssetResponseDto]**](AssetResponseDto.md)

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

# **get_time_buckets**
> List[TimeBucketResponseDto] get_time_buckets(size, user_id=user_id, album_id=album_id, person_id=person_id, is_archived=is_archived, is_favorite=is_favorite, is_trashed=is_trashed, with_stacked=with_stacked, with_partners=with_partners, key=key)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.time_bucket_response_dto import TimeBucketResponseDto
from immich_python_sdk.models.time_bucket_size import TimeBucketSize
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    size = immich_python_sdk.TimeBucketSize() # TimeBucketSize | 
    user_id = 'user_id_example' # str |  (optional)
    album_id = 'album_id_example' # str |  (optional)
    person_id = 'person_id_example' # str |  (optional)
    is_archived = True # bool |  (optional)
    is_favorite = True # bool |  (optional)
    is_trashed = True # bool |  (optional)
    with_stacked = True # bool |  (optional)
    with_partners = True # bool |  (optional)
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.get_time_buckets(size, user_id=user_id, album_id=album_id, person_id=person_id, is_archived=is_archived, is_favorite=is_favorite, is_trashed=is_trashed, with_stacked=with_stacked, with_partners=with_partners, key=key)
        print("The response of AssetApi->get_time_buckets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_time_buckets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **size** | [**TimeBucketSize**](.md)|  | 
 **user_id** | **str**|  | [optional] 
 **album_id** | **str**|  | [optional] 
 **person_id** | **str**|  | [optional] 
 **is_archived** | **bool**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_trashed** | **bool**|  | [optional] 
 **with_stacked** | **bool**|  | [optional] 
 **with_partners** | **bool**|  | [optional] 
 **key** | **str**|  | [optional] 

### Return type

[**List[TimeBucketResponseDto]**](TimeBucketResponseDto.md)

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

# **get_user_assets_by_device_id**
> List[str] get_user_assets_by_device_id(device_id)

Use /asset/device/:deviceId instead - Remove in 1.92 release

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
    api_instance = immich_python_sdk.AssetApi(api_client)
    device_id = 'device_id_example' # str | 

    try:
        # Use /asset/device/:deviceId instead - Remove in 1.92 release
        api_response = api_instance.get_user_assets_by_device_id(device_id)
        print("The response of AssetApi->get_user_assets_by_device_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->get_user_assets_by_device_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_id** | **str**|  | 

### Return type

**List[str]**

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
> restore_assets(bulk_ids_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.bulk_ids_dto import BulkIdsDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    bulk_ids_dto = immich_python_sdk.BulkIdsDto() # BulkIdsDto | 

    try:
        api_instance.restore_assets(bulk_ids_dto)
    except Exception as e:
        print("Exception when calling AssetApi->restore_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_ids_dto** | [**BulkIdsDto**](BulkIdsDto.md)|  | 

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

# **restore_trash**
> restore_trash()

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
    api_instance = immich_python_sdk.AssetApi(api_client)

    try:
        api_instance.restore_trash()
    except Exception as e:
        print("Exception when calling AssetApi->restore_trash: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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

# **run_asset_jobs**
> run_asset_jobs(asset_jobs_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_jobs_dto import AssetJobsDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    asset_jobs_dto = immich_python_sdk.AssetJobsDto() # AssetJobsDto | 

    try:
        api_instance.run_asset_jobs(asset_jobs_dto)
    except Exception as e:
        print("Exception when calling AssetApi->run_asset_jobs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_jobs_dto** | [**AssetJobsDto**](AssetJobsDto.md)|  | 

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

# **search_assets**
> List[AssetResponseDto] search_assets(id=id, library_id=library_id, type=type, order=order, device_asset_id=device_asset_id, device_id=device_id, checksum=checksum, is_archived=is_archived, is_encoded=is_encoded, is_external=is_external, is_favorite=is_favorite, is_motion=is_motion, is_offline=is_offline, is_read_only=is_read_only, is_visible=is_visible, with_deleted=with_deleted, with_stacked=with_stacked, with_exif=with_exif, with_people=with_people, created_before=created_before, created_after=created_after, updated_before=updated_before, updated_after=updated_after, trashed_before=trashed_before, trashed_after=trashed_after, taken_before=taken_before, taken_after=taken_after, original_file_name=original_file_name, original_path=original_path, resize_path=resize_path, webp_path=webp_path, encoded_video_path=encoded_video_path, city=city, state=state, country=country, make=make, model=model, lens_model=lens_model, page=page, size=size)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_order import AssetOrder
from immich_python_sdk.models.asset_response_dto import AssetResponseDto
from immich_python_sdk.models.asset_type_enum import AssetTypeEnum
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    id = 'id_example' # str |  (optional)
    library_id = 'library_id_example' # str |  (optional)
    type = immich_python_sdk.AssetTypeEnum() # AssetTypeEnum |  (optional)
    order = immich_python_sdk.AssetOrder() # AssetOrder |  (optional)
    device_asset_id = 'device_asset_id_example' # str |  (optional)
    device_id = 'device_id_example' # str |  (optional)
    checksum = 'checksum_example' # str |  (optional)
    is_archived = True # bool |  (optional)
    is_encoded = True # bool |  (optional)
    is_external = True # bool |  (optional)
    is_favorite = True # bool |  (optional)
    is_motion = True # bool |  (optional)
    is_offline = True # bool |  (optional)
    is_read_only = True # bool |  (optional)
    is_visible = True # bool |  (optional)
    with_deleted = True # bool |  (optional)
    with_stacked = True # bool |  (optional)
    with_exif = True # bool |  (optional)
    with_people = True # bool |  (optional)
    created_before = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    created_after = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    updated_before = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    updated_after = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    trashed_before = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    trashed_after = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    taken_before = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    taken_after = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    original_file_name = 'original_file_name_example' # str |  (optional)
    original_path = 'original_path_example' # str |  (optional)
    resize_path = 'resize_path_example' # str |  (optional)
    webp_path = 'webp_path_example' # str |  (optional)
    encoded_video_path = 'encoded_video_path_example' # str |  (optional)
    city = 'city_example' # str |  (optional)
    state = 'state_example' # str |  (optional)
    country = 'country_example' # str |  (optional)
    make = 'make_example' # str |  (optional)
    model = 'model_example' # str |  (optional)
    lens_model = 'lens_model_example' # str |  (optional)
    page = 3.4 # float |  (optional)
    size = 3.4 # float |  (optional)

    try:
        api_response = api_instance.search_assets(id=id, library_id=library_id, type=type, order=order, device_asset_id=device_asset_id, device_id=device_id, checksum=checksum, is_archived=is_archived, is_encoded=is_encoded, is_external=is_external, is_favorite=is_favorite, is_motion=is_motion, is_offline=is_offline, is_read_only=is_read_only, is_visible=is_visible, with_deleted=with_deleted, with_stacked=with_stacked, with_exif=with_exif, with_people=with_people, created_before=created_before, created_after=created_after, updated_before=updated_before, updated_after=updated_after, trashed_before=trashed_before, trashed_after=trashed_after, taken_before=taken_before, taken_after=taken_after, original_file_name=original_file_name, original_path=original_path, resize_path=resize_path, webp_path=webp_path, encoded_video_path=encoded_video_path, city=city, state=state, country=country, make=make, model=model, lens_model=lens_model, page=page, size=size)
        print("The response of AssetApi->search_assets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->search_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | [optional] 
 **library_id** | **str**|  | [optional] 
 **type** | [**AssetTypeEnum**](.md)|  | [optional] 
 **order** | [**AssetOrder**](.md)|  | [optional] 
 **device_asset_id** | **str**|  | [optional] 
 **device_id** | **str**|  | [optional] 
 **checksum** | **str**|  | [optional] 
 **is_archived** | **bool**|  | [optional] 
 **is_encoded** | **bool**|  | [optional] 
 **is_external** | **bool**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_motion** | **bool**|  | [optional] 
 **is_offline** | **bool**|  | [optional] 
 **is_read_only** | **bool**|  | [optional] 
 **is_visible** | **bool**|  | [optional] 
 **with_deleted** | **bool**|  | [optional] 
 **with_stacked** | **bool**|  | [optional] 
 **with_exif** | **bool**|  | [optional] 
 **with_people** | **bool**|  | [optional] 
 **created_before** | **datetime**|  | [optional] 
 **created_after** | **datetime**|  | [optional] 
 **updated_before** | **datetime**|  | [optional] 
 **updated_after** | **datetime**|  | [optional] 
 **trashed_before** | **datetime**|  | [optional] 
 **trashed_after** | **datetime**|  | [optional] 
 **taken_before** | **datetime**|  | [optional] 
 **taken_after** | **datetime**|  | [optional] 
 **original_file_name** | **str**|  | [optional] 
 **original_path** | **str**|  | [optional] 
 **resize_path** | **str**|  | [optional] 
 **webp_path** | **str**|  | [optional] 
 **encoded_video_path** | **str**|  | [optional] 
 **city** | **str**|  | [optional] 
 **state** | **str**|  | [optional] 
 **country** | **str**|  | [optional] 
 **make** | **str**|  | [optional] 
 **model** | **str**|  | [optional] 
 **lens_model** | **str**|  | [optional] 
 **page** | **float**|  | [optional] 
 **size** | **float**|  | [optional] 

### Return type

[**List[AssetResponseDto]**](AssetResponseDto.md)

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

# **serve_file**
> bytearray serve_file(id, is_thumb=is_thumb, is_web=is_web, key=key)

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
    api_instance = immich_python_sdk.AssetApi(api_client)
    id = 'id_example' # str | 
    is_thumb = True # bool |  (optional)
    is_web = True # bool |  (optional)
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.serve_file(id, is_thumb=is_thumb, is_web=is_web, key=key)
        print("The response of AssetApi->serve_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->serve_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **is_thumb** | **bool**|  | [optional] 
 **is_web** | **bool**|  | [optional] 
 **key** | **str**|  | [optional] 

### Return type

**bytearray**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_asset**
> AssetResponseDto update_asset(id, update_asset_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_response_dto import AssetResponseDto
from immich_python_sdk.models.update_asset_dto import UpdateAssetDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    id = 'id_example' # str | 
    update_asset_dto = immich_python_sdk.UpdateAssetDto() # UpdateAssetDto | 

    try:
        api_response = api_instance.update_asset(id, update_asset_dto)
        print("The response of AssetApi->update_asset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->update_asset: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_asset_dto** | [**UpdateAssetDto**](UpdateAssetDto.md)|  | 

### Return type

[**AssetResponseDto**](AssetResponseDto.md)

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

# **update_assets**
> update_assets(asset_bulk_update_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_bulk_update_dto import AssetBulkUpdateDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    asset_bulk_update_dto = immich_python_sdk.AssetBulkUpdateDto() # AssetBulkUpdateDto | 

    try:
        api_instance.update_assets(asset_bulk_update_dto)
    except Exception as e:
        print("Exception when calling AssetApi->update_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_bulk_update_dto** | [**AssetBulkUpdateDto**](AssetBulkUpdateDto.md)|  | 

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

# **update_stack_parent**
> update_stack_parent(update_stack_parent_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.update_stack_parent_dto import UpdateStackParentDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    update_stack_parent_dto = immich_python_sdk.UpdateStackParentDto() # UpdateStackParentDto | 

    try:
        api_instance.update_stack_parent(update_stack_parent_dto)
    except Exception as e:
        print("Exception when calling AssetApi->update_stack_parent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_stack_parent_dto** | [**UpdateStackParentDto**](UpdateStackParentDto.md)|  | 

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

# **upload_file**
> AssetFileUploadResponseDto upload_file(asset_data, device_asset_id, device_id, file_created_at, file_modified_at, key=key, duration=duration, is_archived=is_archived, is_external=is_external, is_favorite=is_favorite, is_offline=is_offline, is_read_only=is_read_only, is_visible=is_visible, library_id=library_id, live_photo_data=live_photo_data, sidecar_data=sidecar_data)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_file_upload_response_dto import AssetFileUploadResponseDto
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
    api_instance = immich_python_sdk.AssetApi(api_client)
    asset_data = None # bytearray | 
    device_asset_id = 'device_asset_id_example' # str | 
    device_id = 'device_id_example' # str | 
    file_created_at = '2013-10-20T19:20:30+01:00' # datetime | 
    file_modified_at = '2013-10-20T19:20:30+01:00' # datetime | 
    key = 'key_example' # str |  (optional)
    duration = 'duration_example' # str |  (optional)
    is_archived = True # bool |  (optional)
    is_external = True # bool |  (optional)
    is_favorite = True # bool |  (optional)
    is_offline = True # bool |  (optional)
    is_read_only = True # bool |  (optional)
    is_visible = True # bool |  (optional)
    library_id = 'library_id_example' # str |  (optional)
    live_photo_data = None # bytearray |  (optional)
    sidecar_data = None # bytearray |  (optional)

    try:
        api_response = api_instance.upload_file(asset_data, device_asset_id, device_id, file_created_at, file_modified_at, key=key, duration=duration, is_archived=is_archived, is_external=is_external, is_favorite=is_favorite, is_offline=is_offline, is_read_only=is_read_only, is_visible=is_visible, library_id=library_id, live_photo_data=live_photo_data, sidecar_data=sidecar_data)
        print("The response of AssetApi->upload_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetApi->upload_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_data** | **bytearray**|  | 
 **device_asset_id** | **str**|  | 
 **device_id** | **str**|  | 
 **file_created_at** | **datetime**|  | 
 **file_modified_at** | **datetime**|  | 
 **key** | **str**|  | [optional] 
 **duration** | **str**|  | [optional] 
 **is_archived** | **bool**|  | [optional] 
 **is_external** | **bool**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_offline** | **bool**|  | [optional] 
 **is_read_only** | **bool**|  | [optional] 
 **is_visible** | **bool**|  | [optional] 
 **library_id** | **str**|  | [optional] 
 **live_photo_data** | **bytearray**|  | [optional] 
 **sidecar_data** | **bytearray**|  | [optional] 

### Return type

[**AssetFileUploadResponseDto**](AssetFileUploadResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

