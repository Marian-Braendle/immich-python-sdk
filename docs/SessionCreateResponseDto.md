# SessionCreateResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **str** |  | 
**current** | **bool** |  | 
**device_os** | **str** |  | 
**device_type** | **str** |  | 
**expires_at** | **str** |  | [optional] 
**id** | **str** |  | 
**token** | **str** |  | 
**updated_at** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.session_create_response_dto import SessionCreateResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of SessionCreateResponseDto from a JSON string
session_create_response_dto_instance = SessionCreateResponseDto.from_json(json)
# print the JSON string representation of the object
print(SessionCreateResponseDto.to_json())

# convert the object into a dict
session_create_response_dto_dict = session_create_response_dto_instance.to_dict()
# create an instance of SessionCreateResponseDto from a dict
session_create_response_dto_from_dict = SessionCreateResponseDto.from_dict(session_create_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


