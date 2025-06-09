# immich_python_sdk_asyncio.UsersAdminApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_user_admin**](UsersAdminApi.md#create_user_admin) | **POST** /admin/users | 
[**delete_user_admin**](UsersAdminApi.md#delete_user_admin) | **DELETE** /admin/users/{id} | 
[**get_user_admin**](UsersAdminApi.md#get_user_admin) | **GET** /admin/users/{id} | 
[**get_user_preferences_admin**](UsersAdminApi.md#get_user_preferences_admin) | **GET** /admin/users/{id}/preferences | 
[**get_user_statistics_admin**](UsersAdminApi.md#get_user_statistics_admin) | **GET** /admin/users/{id}/statistics | 
[**restore_user_admin**](UsersAdminApi.md#restore_user_admin) | **POST** /admin/users/{id}/restore | 
[**search_users_admin**](UsersAdminApi.md#search_users_admin) | **GET** /admin/users | 
[**update_user_admin**](UsersAdminApi.md#update_user_admin) | **PUT** /admin/users/{id} | 
[**update_user_preferences_admin**](UsersAdminApi.md#update_user_preferences_admin) | **PUT** /admin/users/{id}/preferences | 


# **create_user_admin**
> UserAdminResponseDto create_user_admin(user_admin_create_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_admin_create_dto import UserAdminCreateDto
from immich_python_sdk_asyncio.models.user_admin_response_dto import UserAdminResponseDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    user_admin_create_dto = immich_python_sdk_asyncio.UserAdminCreateDto() # UserAdminCreateDto | 

    try:
        api_response = await api_instance.create_user_admin(user_admin_create_dto)
        print("The response of UsersAdminApi->create_user_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->create_user_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_admin_create_dto** | [**UserAdminCreateDto**](UserAdminCreateDto.md)|  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

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

# **delete_user_admin**
> UserAdminResponseDto delete_user_admin(id, user_admin_delete_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_admin_delete_dto import UserAdminDeleteDto
from immich_python_sdk_asyncio.models.user_admin_response_dto import UserAdminResponseDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str | 
    user_admin_delete_dto = immich_python_sdk_asyncio.UserAdminDeleteDto() # UserAdminDeleteDto | 

    try:
        api_response = await api_instance.delete_user_admin(id, user_admin_delete_dto)
        print("The response of UsersAdminApi->delete_user_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->delete_user_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **user_admin_delete_dto** | [**UserAdminDeleteDto**](UserAdminDeleteDto.md)|  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

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

# **get_user_admin**
> UserAdminResponseDto get_user_admin(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_admin_response_dto import UserAdminResponseDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = await api_instance.get_user_admin(id)
        print("The response of UsersAdminApi->get_user_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->get_user_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

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

# **get_user_preferences_admin**
> UserPreferencesResponseDto get_user_preferences_admin(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_preferences_response_dto import UserPreferencesResponseDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = await api_instance.get_user_preferences_admin(id)
        print("The response of UsersAdminApi->get_user_preferences_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->get_user_preferences_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**UserPreferencesResponseDto**](UserPreferencesResponseDto.md)

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

# **get_user_statistics_admin**
> AssetStatsResponseDto get_user_statistics_admin(id, is_favorite=is_favorite, is_trashed=is_trashed, visibility=visibility)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.asset_stats_response_dto import AssetStatsResponseDto
from immich_python_sdk_asyncio.models.asset_visibility import AssetVisibility
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str | 
    is_favorite = True # bool |  (optional)
    is_trashed = True # bool |  (optional)
    visibility = immich_python_sdk_asyncio.AssetVisibility() # AssetVisibility |  (optional)

    try:
        api_response = await api_instance.get_user_statistics_admin(id, is_favorite=is_favorite, is_trashed=is_trashed, visibility=visibility)
        print("The response of UsersAdminApi->get_user_statistics_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->get_user_statistics_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
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

# **restore_user_admin**
> UserAdminResponseDto restore_user_admin(id)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_admin_response_dto import UserAdminResponseDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str | 

    try:
        api_response = await api_instance.restore_user_admin(id)
        print("The response of UsersAdminApi->restore_user_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->restore_user_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

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

# **search_users_admin**
> List[UserAdminResponseDto] search_users_admin(id=id, with_deleted=with_deleted)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_admin_response_dto import UserAdminResponseDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str |  (optional)
    with_deleted = True # bool |  (optional)

    try:
        api_response = await api_instance.search_users_admin(id=id, with_deleted=with_deleted)
        print("The response of UsersAdminApi->search_users_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->search_users_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | [optional] 
 **with_deleted** | **bool**|  | [optional] 

### Return type

[**List[UserAdminResponseDto]**](UserAdminResponseDto.md)

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

# **update_user_admin**
> UserAdminResponseDto update_user_admin(id, user_admin_update_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_admin_response_dto import UserAdminResponseDto
from immich_python_sdk_asyncio.models.user_admin_update_dto import UserAdminUpdateDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str | 
    user_admin_update_dto = immich_python_sdk_asyncio.UserAdminUpdateDto() # UserAdminUpdateDto | 

    try:
        api_response = await api_instance.update_user_admin(id, user_admin_update_dto)
        print("The response of UsersAdminApi->update_user_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->update_user_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **user_admin_update_dto** | [**UserAdminUpdateDto**](UserAdminUpdateDto.md)|  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

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

# **update_user_preferences_admin**
> UserPreferencesResponseDto update_user_preferences_admin(id, user_preferences_update_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.user_preferences_response_dto import UserPreferencesResponseDto
from immich_python_sdk_asyncio.models.user_preferences_update_dto import UserPreferencesUpdateDto
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
    api_instance = immich_python_sdk_asyncio.UsersAdminApi(api_client)
    id = 'id_example' # str | 
    user_preferences_update_dto = immich_python_sdk_asyncio.UserPreferencesUpdateDto() # UserPreferencesUpdateDto | 

    try:
        api_response = await api_instance.update_user_preferences_admin(id, user_preferences_update_dto)
        print("The response of UsersAdminApi->update_user_preferences_admin:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersAdminApi->update_user_preferences_admin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **user_preferences_update_dto** | [**UserPreferencesUpdateDto**](UserPreferencesUpdateDto.md)|  | 

### Return type

[**UserPreferencesResponseDto**](UserPreferencesResponseDto.md)

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

