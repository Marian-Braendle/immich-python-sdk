# SyncAssetV1


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checksum** | **str** |  | 
**deleted_at** | **datetime** |  | 
**file_created_at** | **datetime** |  | 
**file_modified_at** | **datetime** |  | 
**id** | **str** |  | 
**is_favorite** | **bool** |  | 
**local_date_time** | **datetime** |  | 
**owner_id** | **str** |  | 
**thumbhash** | **str** |  | 
**type** | **str** |  | 
**visibility** | **str** |  | 

## Example

```python
from immich_python_sdk.models.sync_asset_v1 import SyncAssetV1

# TODO update the JSON string below
json = "{}"
# create an instance of SyncAssetV1 from a JSON string
sync_asset_v1_instance = SyncAssetV1.from_json(json)
# print the JSON string representation of the object
print(SyncAssetV1.to_json())

# convert the object into a dict
sync_asset_v1_dict = sync_asset_v1_instance.to_dict()
# create an instance of SyncAssetV1 from a dict
sync_asset_v1_from_dict = SyncAssetV1.from_dict(sync_asset_v1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


