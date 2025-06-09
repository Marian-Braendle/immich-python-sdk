# FoldersResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [default to False]
**sidebar_web** | **bool** |  | [default to False]

## Example

```python
from immich_python_sdk_asyncio.models.folders_response import FoldersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FoldersResponse from a JSON string
folders_response_instance = FoldersResponse.from_json(json)
# print the JSON string representation of the object
print(FoldersResponse.to_json())

# convert the object into a dict
folders_response_dict = folders_response_instance.to_dict()
# create an instance of FoldersResponse from a dict
folders_response_from_dict = FoldersResponse.from_dict(folders_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


