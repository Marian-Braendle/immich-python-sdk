# AssetFaceCreateDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **str** |  | 
**height** | **int** |  | 
**image_height** | **int** |  | 
**image_width** | **int** |  | 
**person_id** | **str** |  | 
**width** | **int** |  | 
**x** | **int** |  | 
**y** | **int** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.asset_face_create_dto import AssetFaceCreateDto

# TODO update the JSON string below
json = "{}"
# create an instance of AssetFaceCreateDto from a JSON string
asset_face_create_dto_instance = AssetFaceCreateDto.from_json(json)
# print the JSON string representation of the object
print(AssetFaceCreateDto.to_json())

# convert the object into a dict
asset_face_create_dto_dict = asset_face_create_dto_instance.to_dict()
# create an instance of AssetFaceCreateDto from a dict
asset_face_create_dto_from_dict = AssetFaceCreateDto.from_dict(asset_face_create_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


