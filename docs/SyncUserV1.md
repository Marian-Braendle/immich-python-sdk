# SyncUserV1


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted_at** | **datetime** |  | 
**email** | **str** |  | 
**id** | **str** |  | 
**name** | **str** |  | 

## Example

```python
from immich_python_sdk.models.sync_user_v1 import SyncUserV1

# TODO update the JSON string below
json = "{}"
# create an instance of SyncUserV1 from a JSON string
sync_user_v1_instance = SyncUserV1.from_json(json)
# print the JSON string representation of the object
print(SyncUserV1.to_json())

# convert the object into a dict
sync_user_v1_dict = sync_user_v1_instance.to_dict()
# create an instance of SyncUserV1 from a dict
sync_user_v1_from_dict = SyncUserV1.from_dict(sync_user_v1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


