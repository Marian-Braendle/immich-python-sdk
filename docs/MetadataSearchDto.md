# MetadataSearchDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checksum** | **str** |  | [optional] 
**city** | **str** |  | [optional] 
**country** | **str** |  | [optional] 
**created_after** | **datetime** |  | [optional] 
**created_before** | **datetime** |  | [optional] 
**description** | **str** |  | [optional] 
**device_asset_id** | **str** |  | [optional] 
**device_id** | **str** |  | [optional] 
**encoded_video_path** | **str** |  | [optional] 
**id** | **str** |  | [optional] 
**is_encoded** | **bool** |  | [optional] 
**is_favorite** | **bool** |  | [optional] 
**is_motion** | **bool** |  | [optional] 
**is_not_in_album** | **bool** |  | [optional] 
**is_offline** | **bool** |  | [optional] 
**lens_model** | **str** |  | [optional] 
**library_id** | **str** |  | [optional] 
**make** | **str** |  | [optional] 
**model** | **str** |  | [optional] 
**order** | [**AssetOrder**](AssetOrder.md) |  | [optional] 
**original_file_name** | **str** |  | [optional] 
**original_path** | **str** |  | [optional] 
**page** | **float** |  | [optional] 
**person_ids** | **List[str]** |  | [optional] 
**preview_path** | **str** |  | [optional] 
**rating** | **float** |  | [optional] 
**size** | **float** |  | [optional] 
**state** | **str** |  | [optional] 
**tag_ids** | **List[str]** |  | [optional] 
**taken_after** | **datetime** |  | [optional] 
**taken_before** | **datetime** |  | [optional] 
**thumbnail_path** | **str** |  | [optional] 
**trashed_after** | **datetime** |  | [optional] 
**trashed_before** | **datetime** |  | [optional] 
**type** | [**AssetTypeEnum**](AssetTypeEnum.md) |  | [optional] 
**updated_after** | **datetime** |  | [optional] 
**updated_before** | **datetime** |  | [optional] 
**visibility** | [**AssetVisibility**](AssetVisibility.md) |  | [optional] 
**with_deleted** | **bool** |  | [optional] 
**with_exif** | **bool** |  | [optional] 
**with_people** | **bool** |  | [optional] 
**with_stacked** | **bool** |  | [optional] 

## Example

```python
from immich_python_sdk_asyncio.models.metadata_search_dto import MetadataSearchDto

# TODO update the JSON string below
json = "{}"
# create an instance of MetadataSearchDto from a JSON string
metadata_search_dto_instance = MetadataSearchDto.from_json(json)
# print the JSON string representation of the object
print(MetadataSearchDto.to_json())

# convert the object into a dict
metadata_search_dto_dict = metadata_search_dto_instance.to_dict()
# create an instance of MetadataSearchDto from a dict
metadata_search_dto_from_dict = MetadataSearchDto.from_dict(metadata_search_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


