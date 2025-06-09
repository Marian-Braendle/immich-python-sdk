# DuplicateResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assets** | [**List[AssetResponseDto]**](AssetResponseDto.md) |  | 
**duplicate_id** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.duplicate_response_dto import DuplicateResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of DuplicateResponseDto from a JSON string
duplicate_response_dto_instance = DuplicateResponseDto.from_json(json)
# print the JSON string representation of the object
print(DuplicateResponseDto.to_json())

# convert the object into a dict
duplicate_response_dto_dict = duplicate_response_dto_instance.to_dict()
# create an instance of DuplicateResponseDto from a dict
duplicate_response_dto_from_dict = DuplicateResponseDto.from_dict(duplicate_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


