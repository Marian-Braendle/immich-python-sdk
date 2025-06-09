# UpdateAssetDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date_time_original** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**is_favorite** | **bool** |  | [optional] 
**latitude** | **float** |  | [optional] 
**live_photo_video_id** | **str** |  | [optional] 
**longitude** | **float** |  | [optional] 
**rating** | **float** |  | [optional] 
**visibility** | [**AssetVisibility**](AssetVisibility.md) |  | [optional] 

## Example

```python
from immich_python_sdk_asyncio.models.update_asset_dto import UpdateAssetDto

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAssetDto from a JSON string
update_asset_dto_instance = UpdateAssetDto.from_json(json)
# print the JSON string representation of the object
print(UpdateAssetDto.to_json())

# convert the object into a dict
update_asset_dto_dict = update_asset_dto_instance.to_dict()
# create an instance of UpdateAssetDto from a dict
update_asset_dto_from_dict = UpdateAssetDto.from_dict(update_asset_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


