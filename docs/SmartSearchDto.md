# SmartSearchDto


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
**language** | **str** |  | [optional] 
**lens_model** | **str** |  | [optional] 
**library_id** | **str** |  | [optional] 
**make** | **str** |  | [optional] 
**model** | **str** |  | [optional] 
**page** | **float** |  | [optional] 
**person_ids** | **List[str]** |  | [optional] 
**query** | **str** |  | 
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

## Example

```python
from immich_python_sdk.models.smart_search_dto import SmartSearchDto

# TODO update the JSON string below
json = "{}"
# create an instance of SmartSearchDto from a JSON string
smart_search_dto_instance = SmartSearchDto.from_json(json)
# print the JSON string representation of the object
print(SmartSearchDto.to_json())

# convert the object into a dict
smart_search_dto_dict = smart_search_dto_instance.to_dict()
# create an instance of SmartSearchDto from a dict
smart_search_dto_from_dict = SmartSearchDto.from_dict(smart_search_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


