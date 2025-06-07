# SystemConfigTemplateEmailsDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**album_invite_template** | **str** |  | 
**album_update_template** | **str** |  | 
**welcome_template** | **str** |  | 

## Example

```python
from immich_python_sdk.models.system_config_template_emails_dto import SystemConfigTemplateEmailsDto

# TODO update the JSON string below
json = "{}"
# create an instance of SystemConfigTemplateEmailsDto from a JSON string
system_config_template_emails_dto_instance = SystemConfigTemplateEmailsDto.from_json(json)
# print the JSON string representation of the object
print(SystemConfigTemplateEmailsDto.to_json())

# convert the object into a dict
system_config_template_emails_dto_dict = system_config_template_emails_dto_instance.to_dict()
# create an instance of SystemConfigTemplateEmailsDto from a dict
system_config_template_emails_dto_from_dict = SystemConfigTemplateEmailsDto.from_dict(system_config_template_emails_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


