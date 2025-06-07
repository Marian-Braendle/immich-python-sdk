# AssetResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checksum** | **str** | base64 encoded sha1 hash | 
**device_asset_id** | **str** |  | 
**device_id** | **str** |  | 
**duplicate_id** | **str** |  | [optional] 
**duration** | **str** |  | 
**exif_info** | [**ExifResponseDto**](ExifResponseDto.md) |  | [optional] 
**file_created_at** | **datetime** |  | 
**file_modified_at** | **datetime** |  | 
**has_metadata** | **bool** |  | 
**id** | **str** |  | 
**is_archived** | **bool** |  | 
**is_favorite** | **bool** |  | 
**is_offline** | **bool** |  | 
**is_trashed** | **bool** |  | 
**library_id** | **str** | This property was deprecated in v1.106.0 | [optional] 
**live_photo_video_id** | **str** |  | [optional] 
**local_date_time** | **datetime** |  | 
**original_file_name** | **str** |  | 
**original_mime_type** | **str** |  | [optional] 
**original_path** | **str** |  | 
**owner** | [**UserResponseDto**](UserResponseDto.md) |  | [optional] 
**owner_id** | **str** |  | 
**people** | [**List[PersonWithFacesResponseDto]**](PersonWithFacesResponseDto.md) |  | [optional] 
**resized** | **bool** | This property was deprecated in v1.113.0 | [optional] 
**stack** | [**AssetStackResponseDto**](AssetStackResponseDto.md) |  | [optional] 
**tags** | [**List[TagResponseDto]**](TagResponseDto.md) |  | [optional] 
**thumbhash** | **str** |  | 
**type** | [**AssetTypeEnum**](AssetTypeEnum.md) |  | 
**unassigned_faces** | [**List[AssetFaceWithoutPersonResponseDto]**](AssetFaceWithoutPersonResponseDto.md) |  | [optional] 
**updated_at** | **datetime** |  | 
**visibility** | [**AssetVisibility**](AssetVisibility.md) |  | 

## Example

```python
from immich_python_sdk.models.asset_response_dto import AssetResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of AssetResponseDto from a JSON string
asset_response_dto_instance = AssetResponseDto.from_json(json)
# print the JSON string representation of the object
print(AssetResponseDto.to_json())

# convert the object into a dict
asset_response_dto_dict = asset_response_dto_instance.to_dict()
# create an instance of AssetResponseDto from a dict
asset_response_dto_from_dict = AssetResponseDto.from_dict(asset_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


