# SyncAlbumV1


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **datetime** |  | 
**description** | **str** |  | 
**id** | **str** |  | 
**is_activity_enabled** | **bool** |  | 
**name** | **str** |  | 
**order** | [**AssetOrder**](AssetOrder.md) |  | 
**owner_id** | **str** |  | 
**thumbnail_asset_id** | **str** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from immich_python_sdk.models.sync_album_v1 import SyncAlbumV1

# TODO update the JSON string below
json = "{}"
# create an instance of SyncAlbumV1 from a JSON string
sync_album_v1_instance = SyncAlbumV1.from_json(json)
# print the JSON string representation of the object
print(SyncAlbumV1.to_json())

# convert the object into a dict
sync_album_v1_dict = sync_album_v1_instance.to_dict()
# create an instance of SyncAlbumV1 from a dict
sync_album_v1_from_dict = SyncAlbumV1.from_dict(sync_album_v1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


