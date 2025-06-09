# immich_python_sdk_asyncio.JobsApi

All URIs are relative to *https://github.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_job**](JobsApi.md#create_job) | **POST** /jobs | 
[**get_all_jobs_status**](JobsApi.md#get_all_jobs_status) | **GET** /jobs | 
[**send_job_command**](JobsApi.md#send_job_command) | **PUT** /jobs/{id} | 


# **create_job**
> create_job(job_create_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.job_create_dto import JobCreateDto
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
    api_instance = immich_python_sdk_asyncio.JobsApi(api_client)
    job_create_dto = immich_python_sdk_asyncio.JobCreateDto() # JobCreateDto | 

    try:
        await api_instance.create_job(job_create_dto)
    except Exception as e:
        print("Exception when calling JobsApi->create_job: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_create_dto** | [**JobCreateDto**](JobCreateDto.md)|  | 

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
**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_jobs_status**
> AllJobStatusResponseDto get_all_jobs_status()

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.all_job_status_response_dto import AllJobStatusResponseDto
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
    api_instance = immich_python_sdk_asyncio.JobsApi(api_client)

    try:
        api_response = await api_instance.get_all_jobs_status()
        print("The response of JobsApi->get_all_jobs_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling JobsApi->get_all_jobs_status: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AllJobStatusResponseDto**](AllJobStatusResponseDto.md)

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

# **send_job_command**
> JobStatusDto send_job_command(id, job_command_dto)

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (api_key):
* Bearer (JWT) Authentication (bearer):

```python
import immich_python_sdk_asyncio
from immich_python_sdk_asyncio.models.job_command_dto import JobCommandDto
from immich_python_sdk_asyncio.models.job_name import JobName
from immich_python_sdk_asyncio.models.job_status_dto import JobStatusDto
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
    api_instance = immich_python_sdk_asyncio.JobsApi(api_client)
    id = immich_python_sdk_asyncio.JobName() # JobName | 
    job_command_dto = immich_python_sdk_asyncio.JobCommandDto() # JobCommandDto | 

    try:
        api_response = await api_instance.send_job_command(id, job_command_dto)
        print("The response of JobsApi->send_job_command:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling JobsApi->send_job_command: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**JobName**](.md)|  | 
 **job_command_dto** | [**JobCommandDto**](JobCommandDto.md)|  | 

### Return type

[**JobStatusDto**](JobStatusDto.md)

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

