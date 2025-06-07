# immich_python_sdk.PeopleApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_person**](PeopleApi.md#create_person) | **POST** /people | 
[**get_all_people**](PeopleApi.md#get_all_people) | **GET** /people | 
[**get_person**](PeopleApi.md#get_person) | **GET** /people/{id} | 
[**get_person_statistics**](PeopleApi.md#get_person_statistics) | **GET** /people/{id}/statistics | 
[**get_person_thumbnail**](PeopleApi.md#get_person_thumbnail) | **GET** /people/{id}/thumbnail | 
[**merge_person**](PeopleApi.md#merge_person) | **POST** /people/{id}/merge | 
[**reassign_faces**](PeopleApi.md#reassign_faces) | **PUT** /people/{id}/reassign | 
[**update_people**](PeopleApi.md#update_people) | **PUT** /people | 
[**update_person**](PeopleApi.md#update_person) | **PUT** /people/{id} | 


# **create_person**
> PersonResponseDto create_person(person_create_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.person_create_dto import PersonCreateDto
from immich_python_sdk.models.person_response_dto import PersonResponseDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    person_create_dto = immich_python_sdk.PersonCreateDto() # PersonCreateDto | 

    try:
        api_response = api_instance.create_person(person_create_dto)
        print("The response of PeopleApi->create_person:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->create_person: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_create_dto** | [**PersonCreateDto**](PersonCreateDto.md)|  | 

### Return type

[**PersonResponseDto**](PersonResponseDto.md)

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

# **get_all_people**
> PeopleResponseDto get_all_people(closest_asset_id=closest_asset_id, closest_person_id=closest_person_id, page=page, size=size, with_hidden=with_hidden)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.people_response_dto import PeopleResponseDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    closest_asset_id = 'closest_asset_id_example' # str |  (optional)
    closest_person_id = 'closest_person_id_example' # str |  (optional)
    page = 1 # float | Page number for pagination (optional) (default to 1)
    size = 500 # float | Number of items per page (optional) (default to 500)
    with_hidden = True # bool |  (optional)

    try:
        api_response = api_instance.get_all_people(closest_asset_id=closest_asset_id, closest_person_id=closest_person_id, page=page, size=size, with_hidden=with_hidden)
        print("The response of PeopleApi->get_all_people:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->get_all_people: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **closest_asset_id** | **str**|  | [optional] 
 **closest_person_id** | **str**|  | [optional] 
 **page** | **float**| Page number for pagination | [optional] [default to 1]
 **size** | **float**| Number of items per page | [optional] [default to 500]
 **with_hidden** | **bool**|  | [optional] 

### Return type

[**PeopleResponseDto**](PeopleResponseDto.md)

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

# **get_person**
> PersonResponseDto get_person(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.person_response_dto import PersonResponseDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = api_instance.get_person(id)
        print("The response of PeopleApi->get_person:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->get_person: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**PersonResponseDto**](PersonResponseDto.md)

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

# **get_person_statistics**
> PersonStatisticsResponseDto get_person_statistics(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.person_statistics_response_dto import PersonStatisticsResponseDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = api_instance.get_person_statistics(id)
        print("The response of PeopleApi->get_person_statistics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->get_person_statistics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**PersonStatisticsResponseDto**](PersonStatisticsResponseDto.md)

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

# **get_person_thumbnail**
> bytearray get_person_thumbnail(id)

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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = api_instance.get_person_thumbnail(id)
        print("The response of PeopleApi->get_person_thumbnail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->get_person_thumbnail: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

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

# **merge_person**
> List[BulkIdResponseDto] merge_person(id, merge_person_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.bulk_id_response_dto import BulkIdResponseDto
from immich_python_sdk.models.merge_person_dto import MergePersonDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    id = 'id_example' # str | 
    merge_person_dto = immich_python_sdk.MergePersonDto() # MergePersonDto | 

    try:
        api_response = api_instance.merge_person(id, merge_person_dto)
        print("The response of PeopleApi->merge_person:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->merge_person: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **merge_person_dto** | [**MergePersonDto**](MergePersonDto.md)|  | 

### Return type

[**List[BulkIdResponseDto]**](BulkIdResponseDto.md)

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

# **reassign_faces**
> List[PersonResponseDto] reassign_faces(id, asset_face_update_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.asset_face_update_dto import AssetFaceUpdateDto
from immich_python_sdk.models.person_response_dto import PersonResponseDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    id = 'id_example' # str | 
    asset_face_update_dto = immich_python_sdk.AssetFaceUpdateDto() # AssetFaceUpdateDto | 

    try:
        api_response = api_instance.reassign_faces(id, asset_face_update_dto)
        print("The response of PeopleApi->reassign_faces:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->reassign_faces: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **asset_face_update_dto** | [**AssetFaceUpdateDto**](AssetFaceUpdateDto.md)|  | 

### Return type

[**List[PersonResponseDto]**](PersonResponseDto.md)

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

# **update_people**
> List[BulkIdResponseDto] update_people(people_update_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.bulk_id_response_dto import BulkIdResponseDto
from immich_python_sdk.models.people_update_dto import PeopleUpdateDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    people_update_dto = immich_python_sdk.PeopleUpdateDto() # PeopleUpdateDto | 

    try:
        api_response = api_instance.update_people(people_update_dto)
        print("The response of PeopleApi->update_people:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->update_people: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **people_update_dto** | [**PeopleUpdateDto**](PeopleUpdateDto.md)|  | 

### Return type

[**List[BulkIdResponseDto]**](BulkIdResponseDto.md)

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

# **update_person**
> PersonResponseDto update_person(id, person_update_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk
from immich_python_sdk.models.person_response_dto import PersonResponseDto
from immich_python_sdk.models.person_update_dto import PersonUpdateDto
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
    api_instance = immich_python_sdk.PeopleApi(api_client)
    id = 'id_example' # str | 
    person_update_dto = immich_python_sdk.PersonUpdateDto() # PersonUpdateDto | 

    try:
        api_response = api_instance.update_person(id, person_update_dto)
        print("The response of PeopleApi->update_person:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PeopleApi->update_person: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **person_update_dto** | [**PersonUpdateDto**](PersonUpdateDto.md)|  | 

### Return type

[**PersonResponseDto**](PersonResponseDto.md)

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

