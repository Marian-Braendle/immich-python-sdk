# SystemConfigFacesDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_import** | **bool** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.system_config_faces_dto import SystemConfigFacesDto

# TODO update the JSON string below
json = "{}"
# create an instance of SystemConfigFacesDto from a JSON string
system_config_faces_dto_instance = SystemConfigFacesDto.from_json(json)
# print the JSON string representation of the object
print(SystemConfigFacesDto.to_json())

# convert the object into a dict
system_config_faces_dto_dict = system_config_faces_dto_instance.to_dict()
# create an instance of SystemConfigFacesDto from a dict
system_config_faces_dto_from_dict = SystemConfigFacesDto.from_dict(system_config_faces_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


