# MemoriesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [default to True]

## Example

```python
from immich_python_sdk_asyncio.models.memories_response import MemoriesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MemoriesResponse from a JSON string
memories_response_instance = MemoriesResponse.from_json(json)
# print the JSON string representation of the object
print(MemoriesResponse.to_json())

# convert the object into a dict
memories_response_dict = memories_response_instance.to_dict()
# create an instance of MemoriesResponse from a dict
memories_response_from_dict = MemoriesResponse.from_dict(memories_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


