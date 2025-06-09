# SyncAlbumUserV1


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**album_id** | **str** |  | 
**role** | **str** |  | 
**user_id** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.sync_album_user_v1 import SyncAlbumUserV1

# TODO update the JSON string below
json = "{}"
# create an instance of SyncAlbumUserV1 from a JSON string
sync_album_user_v1_instance = SyncAlbumUserV1.from_json(json)
# print the JSON string representation of the object
print(SyncAlbumUserV1.to_json())

# convert the object into a dict
sync_album_user_v1_dict = sync_album_user_v1_instance.to_dict()
# create an instance of SyncAlbumUserV1 from a dict
sync_album_user_v1_from_dict = SyncAlbumUserV1.from_dict(sync_album_user_v1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


