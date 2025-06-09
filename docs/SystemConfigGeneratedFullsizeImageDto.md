# SystemConfigGeneratedFullsizeImageDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**format** | [**ImageFormat**](ImageFormat.md) |  | 
**quality** | **int** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.system_config_generated_fullsize_image_dto import SystemConfigGeneratedFullsizeImageDto

# TODO update the JSON string below
json = "{}"
# create an instance of SystemConfigGeneratedFullsizeImageDto from a JSON string
system_config_generated_fullsize_image_dto_instance = SystemConfigGeneratedFullsizeImageDto.from_json(json)
# print the JSON string representation of the object
print(SystemConfigGeneratedFullsizeImageDto.to_json())

# convert the object into a dict
system_config_generated_fullsize_image_dto_dict = system_config_generated_fullsize_image_dto_instance.to_dict()
# create an instance of SystemConfigGeneratedFullsizeImageDto from a dict
system_config_generated_fullsize_image_dto_from_dict = SystemConfigGeneratedFullsizeImageDto.from_dict(system_config_generated_fullsize_image_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


