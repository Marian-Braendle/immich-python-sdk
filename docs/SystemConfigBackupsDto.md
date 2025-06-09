# SystemConfigBackupsDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**database** | [**DatabaseBackupConfig**](DatabaseBackupConfig.md) |  | 

## Example

```python
from immich_python_sdk_asyncio.models.system_config_backups_dto import SystemConfigBackupsDto

# TODO update the JSON string below
json = "{}"
# create an instance of SystemConfigBackupsDto from a JSON string
system_config_backups_dto_instance = SystemConfigBackupsDto.from_json(json)
# print the JSON string representation of the object
print(SystemConfigBackupsDto.to_json())

# convert the object into a dict
system_config_backups_dto_dict = system_config_backups_dto_instance.to_dict()
# create an instance of SystemConfigBackupsDto from a dict
system_config_backups_dto_from_dict = SystemConfigBackupsDto.from_dict(system_config_backups_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


