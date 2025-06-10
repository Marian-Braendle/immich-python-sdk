# immich_python_sdk.AssetsApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_bulk_upload**](AssetsApi.md#check_bulk_upload) | **POST** /assets/bulk-upload-check | checkBulkUpload
[**check_existing_assets**](AssetsApi.md#check_existing_assets) | **POST** /assets/exist | checkExistingAssets
[**delete_assets**](AssetsApi.md#delete_assets) | **DELETE** /assets | 
[**download_asset**](AssetsApi.md#download_asset) | **GET** /assets/{id}/original | 
[**get_all_user_assets_by_device_id**](AssetsApi.md#get_all_user_assets_by_device_id) | **GET** /assets/device/{deviceId} | getAllUserAssetsByDeviceId
[**get_asset_info**](AssetsApi.md#get_asset_info) | **GET** /assets/{id} | 
[**get_asset_statistics**](AssetsApi.md#get_asset_statistics) | **GET** /assets/statistics | 
[**get_random**](AssetsApi.md#get_random) | **GET** /assets/random | 
[**play_asset_video**](AssetsApi.md#play_asset_video) | **GET** /assets/{id}/video/playback | 
[**replace_asset**](AssetsApi.md#replace_asset) | **PUT** /assets/{id}/original | replaceAsset
[**run_asset_jobs**](AssetsApi.md#run_asset_jobs) | **POST** /assets/jobs | 
[**update_asset**](AssetsApi.md#update_asset) | **PUT** /assets/{id} | 
[**update_assets**](AssetsApi.md#update_assets) | **PUT** /assets | 
[**upload_asset**](AssetsApi.md#upload_asset) | **POST** /assets | 
[**view_asset**](AssetsApi.md#view_asset) | **GET** /assets/{id}/thumbnail | 


# **check_bulk_upload**
> AssetBulkUploadCheckResponseDto check_bulk_upload(asset_bulk_upload_check_dto)

checkBulkUpload

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    asset_bulk_upload_check_dto = immich_python_sdk.AssetBulkUploadCheckDto() # AssetBulkUploadCheckDto | 

    try:
        # checkBulkUpload
        api_response = api_instance.check_bulk_upload(asset_bulk_upload_check_dto)
        print("The response of AssetsApi->check_bulk_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->check_bulk_upload: %s\n" % e)
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

checkExistingAssets

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    check_existing_assets_dto = immich_python_sdk.CheckExistingAssetsDto() # CheckExistingAssetsDto | 

    try:
        # checkExistingAssets
        api_response = api_instance.check_existing_assets(check_existing_assets_dto)
        print("The response of AssetsApi->check_existing_assets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->check_existing_assets: %s\n" % e)
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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    asset_bulk_delete_dto = immich_python_sdk.AssetBulkDeleteDto() # AssetBulkDeleteDto | 

    try:
        api_instance.delete_assets(asset_bulk_delete_dto)
    except Exception as e:
        print("Exception when calling AssetsApi->delete_assets: %s\n" % e)
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

# **download_asset**
> bytearray download_asset(id, key=key)

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    id = 'id_example' # str | 
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.download_asset(id, key=key)
        print("The response of AssetsApi->download_asset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->download_asset: %s\n" % e)
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

# **get_all_user_assets_by_device_id**
> List[str] get_all_user_assets_by_device_id(device_id)

getAllUserAssetsByDeviceId

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    device_id = 'device_id_example' # str | 

    try:
        # getAllUserAssetsByDeviceId
        api_response = api_instance.get_all_user_assets_by_device_id(device_id)
        print("The response of AssetsApi->get_all_user_assets_by_device_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->get_all_user_assets_by_device_id: %s\n" % e)
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

# **get_asset_info**
> AssetResponseDto get_asset_info(id, key=key)

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    id = 'id_example' # str | 
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.get_asset_info(id, key=key)
        print("The response of AssetsApi->get_asset_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->get_asset_info: %s\n" % e)
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

# **get_asset_statistics**
> AssetStatsResponseDto get_asset_statistics(is_favorite=is_favorite, is_trashed=is_trashed, visibility=visibility)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_stats_response_dto import AssetStatsResponseDto
from immich_python_sdk.models.asset_visibility import AssetVisibility
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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    is_favorite = True # bool |  (optional)
    is_trashed = True # bool |  (optional)
    visibility = immich_python_sdk.AssetVisibility() # AssetVisibility |  (optional)

    try:
        api_response = api_instance.get_asset_statistics(is_favorite=is_favorite, is_trashed=is_trashed, visibility=visibility)
        print("The response of AssetsApi->get_asset_statistics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->get_asset_statistics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **is_favorite** | **bool**|  | [optional] 
 **is_trashed** | **bool**|  | [optional] 
 **visibility** | [**AssetVisibility**](.md)|  | [optional] 

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

# **get_random**
> List[AssetResponseDto] get_random(count=count)

This property was deprecated in v1.116.0

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    count = 3.4 # float |  (optional)

    try:
        api_response = api_instance.get_random(count=count)
        print("The response of AssetsApi->get_random:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->get_random: %s\n" % e)
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

# **play_asset_video**
> bytearray play_asset_video(id, key=key)

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    id = 'id_example' # str | 
    key = 'key_example' # str |  (optional)

    try:
        api_response = api_instance.play_asset_video(id, key=key)
        print("The response of AssetsApi->play_asset_video:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->play_asset_video: %s\n" % e)
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

# **replace_asset**
> AssetMediaResponseDto replace_asset(id, asset_data, device_asset_id, device_id, file_created_at, file_modified_at, key=key, duration=duration)

replaceAsset

Replace the asset with new file, without changing its id

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_media_response_dto import AssetMediaResponseDto
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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    id = 'id_example' # str | 
    asset_data = None # bytearray | 
    device_asset_id = 'device_asset_id_example' # str | 
    device_id = 'device_id_example' # str | 
    file_created_at = '2013-10-20T19:20:30+01:00' # datetime | 
    file_modified_at = '2013-10-20T19:20:30+01:00' # datetime | 
    key = 'key_example' # str |  (optional)
    duration = 'duration_example' # str |  (optional)

    try:
        # replaceAsset
        api_response = api_instance.replace_asset(id, asset_data, device_asset_id, device_id, file_created_at, file_modified_at, key=key, duration=duration)
        print("The response of AssetsApi->replace_asset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->replace_asset: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **asset_data** | **bytearray**|  | 
 **device_asset_id** | **str**|  | 
 **device_id** | **str**|  | 
 **file_created_at** | **datetime**|  | 
 **file_modified_at** | **datetime**|  | 
 **key** | **str**|  | [optional] 
 **duration** | **str**|  | [optional] 

### Return type

[**AssetMediaResponseDto**](AssetMediaResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    asset_jobs_dto = immich_python_sdk.AssetJobsDto() # AssetJobsDto | 

    try:
        api_instance.run_asset_jobs(asset_jobs_dto)
    except Exception as e:
        print("Exception when calling AssetsApi->run_asset_jobs: %s\n" % e)
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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    id = 'id_example' # str | 
    update_asset_dto = immich_python_sdk.UpdateAssetDto() # UpdateAssetDto | 

    try:
        api_response = api_instance.update_asset(id, update_asset_dto)
        print("The response of AssetsApi->update_asset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->update_asset: %s\n" % e)
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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    asset_bulk_update_dto = immich_python_sdk.AssetBulkUpdateDto() # AssetBulkUpdateDto | 

    try:
        api_instance.update_assets(asset_bulk_update_dto)
    except Exception as e:
        print("Exception when calling AssetsApi->update_assets: %s\n" % e)
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

# **upload_asset**
> AssetMediaResponseDto upload_asset(asset_data, device_asset_id, device_id, file_created_at, file_modified_at, key=key, x_immich_checksum=x_immich_checksum, duration=duration, is_favorite=is_favorite, live_photo_video_id=live_photo_video_id, sidecar_data=sidecar_data, visibility=visibility)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_media_response_dto import AssetMediaResponseDto
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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    asset_data = None # bytearray | 
    device_asset_id = 'device_asset_id_example' # str | 
    device_id = 'device_id_example' # str | 
    file_created_at = '2013-10-20T19:20:30+01:00' # datetime | 
    file_modified_at = '2013-10-20T19:20:30+01:00' # datetime | 
    key = 'key_example' # str |  (optional)
    x_immich_checksum = 'x_immich_checksum_example' # str | sha1 checksum that can be used for duplicate detection before the file is uploaded (optional)
    duration = 'duration_example' # str |  (optional)
    is_favorite = True # bool |  (optional)
    live_photo_video_id = 'live_photo_video_id_example' # str |  (optional)
    sidecar_data = None # bytearray |  (optional)
    visibility = immich_python_sdk.AssetVisibility() # AssetVisibility |  (optional)

    try:
        api_response = api_instance.upload_asset(asset_data, device_asset_id, device_id, file_created_at, file_modified_at, key=key, x_immich_checksum=x_immich_checksum, duration=duration, is_favorite=is_favorite, live_photo_video_id=live_photo_video_id, sidecar_data=sidecar_data, visibility=visibility)
        print("The response of AssetsApi->upload_asset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->upload_asset: %s\n" % e)
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
 **x_immich_checksum** | **str**| sha1 checksum that can be used for duplicate detection before the file is uploaded | [optional] 
 **duration** | **str**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **live_photo_video_id** | **str**|  | [optional] 
 **sidecar_data** | **bytearray**|  | [optional] 
 **visibility** | [**AssetVisibility**](AssetVisibility.md)|  | [optional] 

### Return type

[**AssetMediaResponseDto**](AssetMediaResponseDto.md)

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

# **view_asset**
> bytearray view_asset(id, key=key, size=size)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_media_size import AssetMediaSize
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
    api_instance = immich_python_sdk.AssetsApi(api_client)
    id = 'id_example' # str | 
    key = 'key_example' # str |  (optional)
    size = immich_python_sdk.AssetMediaSize() # AssetMediaSize |  (optional)

    try:
        api_response = api_instance.view_asset(id, key=key, size=size)
        print("The response of AssetsApi->view_asset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->view_asset: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **key** | **str**|  | [optional] 
 **size** | [**AssetMediaSize**](.md)|  | [optional] 

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

