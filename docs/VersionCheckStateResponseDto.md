# VersionCheckStateResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checked_at** | **str** |  | 
**release_version** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.version_check_state_response_dto import VersionCheckStateResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of VersionCheckStateResponseDto from a JSON string
version_check_state_response_dto_instance = VersionCheckStateResponseDto.from_json(json)
# print the JSON string representation of the object
print(VersionCheckStateResponseDto.to_json())

# convert the object into a dict
version_check_state_response_dto_dict = version_check_state_response_dto_instance.to_dict()
# create an instance of VersionCheckStateResponseDto from a dict
version_check_state_response_dto_from_dict = VersionCheckStateResponseDto.from_dict(version_check_state_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


