# DatabaseBackupConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cron_expression** | **str** |  | 
**enabled** | **bool** |  | 
**keep_last_amount** | **float** |  | 

## Example

```python
from immich_python_sdk.models.database_backup_config import DatabaseBackupConfig

# TODO update the JSON string below
json = "{}"
# create an instance of DatabaseBackupConfig from a JSON string
database_backup_config_instance = DatabaseBackupConfig.from_json(json)
# print the JSON string representation of the object
print(DatabaseBackupConfig.to_json())

# convert the object into a dict
database_backup_config_dict = database_backup_config_instance.to_dict()
# create an instance of DatabaseBackupConfig from a dict
database_backup_config_from_dict = DatabaseBackupConfig.from_dict(database_backup_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


