# immich_python_sdk_asyncio.TimelineApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_time_bucket**](TimelineApi.md#get_time_bucket) | **GET** /timeline/bucket | 
[**get_time_buckets**](TimelineApi.md#get_time_buckets) | **GET** /timeline/buckets | 


# **get_time_bucket**
> TimeBucketAssetResponseDto get_time_bucket(time_bucket, album_id=album_id, is_favorite=is_favorite, is_trashed=is_trashed, key=key, order=order, page=page, page_size=page_size, person_id=person_id, tag_id=tag_id, user_id=user_id, visibility=visibility, with_partners=with_partners, with_stacked=with_stacked)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.asset_order import AssetOrder
from immich_python_sdk_asyncio.models.asset_visibility import AssetVisibility
from immich_python_sdk_asyncio.models.time_bucket_asset_response_dto import TimeBucketAssetResponseDto
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
    api_instance = immich_python_sdk_asyncio.TimelineApi(api_client)
    time_bucket = 'time_bucket_example' # str | 
    album_id = 'album_id_example' # str |  (optional)
    is_favorite = True # bool |  (optional)
    is_trashed = True # bool |  (optional)
    key = 'key_example' # str |  (optional)
    order = immich_python_sdk_asyncio.AssetOrder() # AssetOrder |  (optional)
    page = 3.4 # float |  (optional)
    page_size = 3.4 # float |  (optional)
    person_id = 'person_id_example' # str |  (optional)
    tag_id = 'tag_id_example' # str |  (optional)
    user_id = 'user_id_example' # str |  (optional)
    visibility = immich_python_sdk_asyncio.AssetVisibility() # AssetVisibility |  (optional)
    with_partners = True # bool |  (optional)
    with_stacked = True # bool |  (optional)

    try:
        api_response = await api_instance.get_time_bucket(time_bucket, album_id=album_id, is_favorite=is_favorite, is_trashed=is_trashed, key=key, order=order, page=page, page_size=page_size, person_id=person_id, tag_id=tag_id, user_id=user_id, visibility=visibility, with_partners=with_partners, with_stacked=with_stacked)
        print("The response of TimelineApi->get_time_bucket:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TimelineApi->get_time_bucket: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **time_bucket** | **str**|  | 
 **album_id** | **str**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_trashed** | **bool**|  | [optional] 
 **key** | **str**|  | [optional] 
 **order** | [**AssetOrder**](.md)|  | [optional] 
 **page** | **float**|  | [optional] 
 **page_size** | **float**|  | [optional] 
 **person_id** | **str**|  | [optional] 
 **tag_id** | **str**|  | [optional] 
 **user_id** | **str**|  | [optional] 
 **visibility** | [**AssetVisibility**](.md)|  | [optional] 
 **with_partners** | **bool**|  | [optional] 
 **with_stacked** | **bool**|  | [optional] 

### Return type

[**TimeBucketAssetResponseDto**](TimeBucketAssetResponseDto.md)

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
> List[TimeBucketsResponseDto] get_time_buckets(album_id=album_id, is_favorite=is_favorite, is_trashed=is_trashed, key=key, order=order, person_id=person_id, tag_id=tag_id, user_id=user_id, visibility=visibility, with_partners=with_partners, with_stacked=with_stacked)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.asset_order import AssetOrder
from immich_python_sdk_asyncio.models.asset_visibility import AssetVisibility
from immich_python_sdk_asyncio.models.time_buckets_response_dto import TimeBucketsResponseDto
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
    api_instance = immich_python_sdk_asyncio.TimelineApi(api_client)
    album_id = 'album_id_example' # str |  (optional)
    is_favorite = True # bool |  (optional)
    is_trashed = True # bool |  (optional)
    key = 'key_example' # str |  (optional)
    order = immich_python_sdk_asyncio.AssetOrder() # AssetOrder |  (optional)
    person_id = 'person_id_example' # str |  (optional)
    tag_id = 'tag_id_example' # str |  (optional)
    user_id = 'user_id_example' # str |  (optional)
    visibility = immich_python_sdk_asyncio.AssetVisibility() # AssetVisibility |  (optional)
    with_partners = True # bool |  (optional)
    with_stacked = True # bool |  (optional)

    try:
        api_response = await api_instance.get_time_buckets(album_id=album_id, is_favorite=is_favorite, is_trashed=is_trashed, key=key, order=order, person_id=person_id, tag_id=tag_id, user_id=user_id, visibility=visibility, with_partners=with_partners, with_stacked=with_stacked)
        print("The response of TimelineApi->get_time_buckets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TimelineApi->get_time_buckets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **album_id** | **str**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **is_trashed** | **bool**|  | [optional] 
 **key** | **str**|  | [optional] 
 **order** | [**AssetOrder**](.md)|  | [optional] 
 **person_id** | **str**|  | [optional] 
 **tag_id** | **str**|  | [optional] 
 **user_id** | **str**|  | [optional] 
 **visibility** | [**AssetVisibility**](.md)|  | [optional] 
 **with_partners** | **bool**|  | [optional] 
 **with_stacked** | **bool**|  | [optional] 

### Return type

[**List[TimeBucketsResponseDto]**](TimeBucketsResponseDto.md)

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

