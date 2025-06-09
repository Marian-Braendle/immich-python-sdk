# immich_python_sdk_asyncio.MapApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_map_markers**](MapApi.md#get_map_markers) | **GET** /map/markers | 
[**reverse_geocode**](MapApi.md#reverse_geocode) | **GET** /map/reverse-geocode | 


# **get_map_markers**
> List[MapMarkerResponseDto] get_map_markers(file_created_after=file_created_after, file_created_before=file_created_before, is_archived=is_archived, is_favorite=is_favorite, with_partners=with_partners, with_shared_albums=with_shared_albums)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.map_marker_response_dto import MapMarkerResponseDto
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
    api_instance = immich_python_sdk_asyncio.MapApi(api_client)
    file_created_after = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    file_created_before = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    is_archived = True # bool |  (optional)
    is_favorite = True # bool |  (optional)
    with_partners = True # bool |  (optional)
    with_shared_albums = True # bool |  (optional)

    try:
        api_response = await api_instance.get_map_markers(file_created_after=file_created_after, file_created_before=file_created_before, is_archived=is_archived, is_favorite=is_favorite, with_partners=with_partners, with_shared_albums=with_shared_albums)
        print("The response of MapApi->get_map_markers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MapApi->get_map_markers: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_created_after** | **datetime**|  | [optional] 
 **file_created_before** | **datetime**|  | [optional] 
 **is_archived** | **bool**|  | [optional] 
 **is_favorite** | **bool**|  | [optional] 
 **with_partners** | **bool**|  | [optional] 
 **with_shared_albums** | **bool**|  | [optional] 

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

# **reverse_geocode**
> List[MapReverseGeocodeResponseDto] reverse_geocode(lat, lon)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.map_reverse_geocode_response_dto import MapReverseGeocodeResponseDto
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
    api_instance = immich_python_sdk_asyncio.MapApi(api_client)
    lat = 3.4 # float | 
    lon = 3.4 # float | 

    try:
        api_response = await api_instance.reverse_geocode(lat, lon)
        print("The response of MapApi->reverse_geocode:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MapApi->reverse_geocode: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lat** | **float**|  | 
 **lon** | **float**|  | 

### Return type

[**List[MapReverseGeocodeResponseDto]**](MapReverseGeocodeResponseDto.md)

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

