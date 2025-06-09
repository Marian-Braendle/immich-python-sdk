# RandomSearchDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**city** | **str** |  | [optional] 
**country** | **str** |  | [optional] 
**created_after** | **datetime** |  | [optional] 
**created_before** | **datetime** |  | [optional] 
**device_id** | **str** |  | [optional] 
**is_encoded** | **bool** |  | [optional] 
**is_favorite** | **bool** |  | [optional] 
**is_motion** | **bool** |  | [optional] 
**is_not_in_album** | **bool** |  | [optional] 
**is_offline** | **bool** |  | [optional] 
**lens_model** | **str** |  | [optional] 
**library_id** | **str** |  | [optional] 
**make** | **str** |  | [optional] 
**model** | **str** |  | [optional] 
**person_ids** | **List[str]** |  | [optional] 
**rating** | **float** |  | [optional] 
**size** | **float** |  | [optional] 
**state** | **str** |  | [optional] 
**tag_ids** | **List[str]** |  | [optional] 
**taken_after** | **datetime** |  | [optional] 
**taken_before** | **datetime** |  | [optional] 
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
from immich_python_sdk_asyncio.models.random_search_dto import RandomSearchDto

# TODO update the JSON string below
json = "{}"
# create an instance of RandomSearchDto from a JSON string
random_search_dto_instance = RandomSearchDto.from_json(json)
# print the JSON string representation of the object
print(RandomSearchDto.to_json())

# convert the object into a dict
random_search_dto_dict = random_search_dto_instance.to_dict()
# create an instance of RandomSearchDto from a dict
random_search_dto_from_dict = RandomSearchDto.from_dict(random_search_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


