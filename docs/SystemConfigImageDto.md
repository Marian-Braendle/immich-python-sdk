# SystemConfigImageDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**colorspace** | [**Colorspace**](Colorspace.md) |  | 
**extract_embedded** | **bool** |  | 
**fullsize** | [**SystemConfigGeneratedFullsizeImageDto**](SystemConfigGeneratedFullsizeImageDto.md) |  | 
**preview** | [**SystemConfigGeneratedImageDto**](SystemConfigGeneratedImageDto.md) |  | 
**thumbnail** | [**SystemConfigGeneratedImageDto**](SystemConfigGeneratedImageDto.md) |  | 

## Example

```python
from immich_python_sdk_asyncio.models.system_config_image_dto import SystemConfigImageDto

# TODO update the JSON string below
json = "{}"
# create an instance of SystemConfigImageDto from a JSON string
system_config_image_dto_instance = SystemConfigImageDto.from_json(json)
# print the JSON string representation of the object
print(SystemConfigImageDto.to_json())

# convert the object into a dict
system_config_image_dto_dict = system_config_image_dto_instance.to_dict()
# create an instance of SystemConfigImageDto from a dict
system_config_image_dto_from_dict = SystemConfigImageDto.from_dict(system_config_image_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


