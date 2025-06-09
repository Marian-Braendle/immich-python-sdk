# StackCreateDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_ids** | **List[str]** | first asset becomes the primary | 

## Example

```python
from immich_python_sdk_asyncio.models.stack_create_dto import StackCreateDto

# TODO update the JSON string below
json = "{}"
# create an instance of StackCreateDto from a JSON string
stack_create_dto_instance = StackCreateDto.from_json(json)
# print the JSON string representation of the object
print(StackCreateDto.to_json())

# convert the object into a dict
stack_create_dto_dict = stack_create_dto_instance.to_dict()
# create an instance of StackCreateDto from a dict
stack_create_dto_from_dict = StackCreateDto.from_dict(stack_create_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


