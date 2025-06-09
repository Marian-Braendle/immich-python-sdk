# SystemConfigTemplatesDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | [**SystemConfigTemplateEmailsDto**](SystemConfigTemplateEmailsDto.md) |  | 

## Example

```python
from immich_python_sdk_asyncio.models.system_config_templates_dto import SystemConfigTemplatesDto

# TODO update the JSON string below
json = "{}"
# create an instance of SystemConfigTemplatesDto from a JSON string
system_config_templates_dto_instance = SystemConfigTemplatesDto.from_json(json)
# print the JSON string representation of the object
print(SystemConfigTemplatesDto.to_json())

# convert the object into a dict
system_config_templates_dto_dict = system_config_templates_dto_instance.to_dict()
# create an instance of SystemConfigTemplatesDto from a dict
system_config_templates_dto_from_dict = SystemConfigTemplatesDto.from_dict(system_config_templates_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


