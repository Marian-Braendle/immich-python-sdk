# SyncAssetExifV1


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **str** |  | 
**city** | **str** |  | 
**country** | **str** |  | 
**date_time_original** | **datetime** |  | 
**description** | **str** |  | 
**exif_image_height** | **int** |  | 
**exif_image_width** | **int** |  | 
**exposure_time** | **str** |  | 
**f_number** | **int** |  | 
**file_size_in_byte** | **int** |  | 
**focal_length** | **int** |  | 
**fps** | **int** |  | 
**iso** | **int** |  | 
**latitude** | **int** |  | 
**lens_model** | **str** |  | 
**longitude** | **int** |  | 
**make** | **str** |  | 
**model** | **str** |  | 
**modify_date** | **datetime** |  | 
**orientation** | **str** |  | 
**profile_description** | **str** |  | 
**projection_type** | **str** |  | 
**rating** | **int** |  | 
**state** | **str** |  | 
**time_zone** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.sync_asset_exif_v1 import SyncAssetExifV1

# TODO update the JSON string below
json = "{}"
# create an instance of SyncAssetExifV1 from a JSON string
sync_asset_exif_v1_instance = SyncAssetExifV1.from_json(json)
# print the JSON string representation of the object
print(SyncAssetExifV1.to_json())

# convert the object into a dict
sync_asset_exif_v1_dict = sync_asset_exif_v1_instance.to_dict()
# create an instance of SyncAssetExifV1 from a dict
sync_asset_exif_v1_from_dict = SyncAssetExifV1.from_dict(sync_asset_exif_v1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


