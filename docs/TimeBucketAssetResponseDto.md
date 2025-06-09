# TimeBucketAssetResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**city** | **List[Optional[str]]** |  | 
**country** | **List[Optional[str]]** |  | 
**duration** | **List[Optional[str]]** |  | 
**id** | **List[str]** |  | 
**is_favorite** | **List[bool]** |  | 
**is_image** | **List[bool]** |  | 
**is_trashed** | **List[bool]** |  | 
**live_photo_video_id** | **List[Optional[str]]** |  | 
**local_date_time** | **List[str]** |  | 
**owner_id** | **List[str]** |  | 
**projection_type** | **List[Optional[str]]** |  | 
**ratio** | **List[float]** |  | 
**stack** | **List[Optional[List[str]]]** | (stack ID, stack asset count) tuple | [optional] 
**thumbhash** | **List[Optional[str]]** |  | 
**visibility** | [**List[AssetVisibility]**](AssetVisibility.md) |  | 

## Example

```python
from immich_python_sdk_asyncio.models.time_bucket_asset_response_dto import TimeBucketAssetResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of TimeBucketAssetResponseDto from a JSON string
time_bucket_asset_response_dto_instance = TimeBucketAssetResponseDto.from_json(json)
# print the JSON string representation of the object
print(TimeBucketAssetResponseDto.to_json())

# convert the object into a dict
time_bucket_asset_response_dto_dict = time_bucket_asset_response_dto_instance.to_dict()
# create an instance of TimeBucketAssetResponseDto from a dict
time_bucket_asset_response_dto_from_dict = TimeBucketAssetResponseDto.from_dict(time_bucket_asset_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


