# PersonWithFacesResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**birth_date** | **date** |  | 
**color** | **str** | This property was added in v1.126.0 | [optional] 
**faces** | [**List[AssetFaceWithoutPersonResponseDto]**](AssetFaceWithoutPersonResponseDto.md) |  | 
**id** | **str** |  | 
**is_favorite** | **bool** | This property was added in v1.126.0 | [optional] 
**is_hidden** | **bool** |  | 
**name** | **str** |  | 
**thumbnail_path** | **str** |  | 
**updated_at** | **datetime** | This property was added in v1.107.0 | [optional] 

## Example

```python
from immich_python_sdk_asyncio.models.person_with_faces_response_dto import PersonWithFacesResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of PersonWithFacesResponseDto from a JSON string
person_with_faces_response_dto_instance = PersonWithFacesResponseDto.from_json(json)
# print the JSON string representation of the object
print(PersonWithFacesResponseDto.to_json())

# convert the object into a dict
person_with_faces_response_dto_dict = person_with_faces_response_dto_instance.to_dict()
# create an instance of PersonWithFacesResponseDto from a dict
person_with_faces_response_dto_from_dict = PersonWithFacesResponseDto.from_dict(person_with_faces_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


