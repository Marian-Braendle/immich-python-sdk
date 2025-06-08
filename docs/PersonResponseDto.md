# PersonResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**birth_date** | **date** |  | 
**color** | **str** | This property was added in v1.126.0 | [optional] 
**id** | **str** |  | 
**is_favorite** | **bool** | This property was added in v1.126.0 | [optional] 
**is_hidden** | **bool** |  | 
**name** | **str** |  | 
**thumbnail_path** | **str** |  | 
**updated_at** | **datetime** | This property was added in v1.107.0 | [optional] 

## Example

```python
from immich_python_sdk.models.person_response_dto import PersonResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of PersonResponseDto from a JSON string
person_response_dto_instance = PersonResponseDto.from_json(json)
# print the JSON string representation of the object
print(PersonResponseDto.to_json())

# convert the object into a dict
person_response_dto_dict = person_response_dto_instance.to_dict()
# create an instance of PersonResponseDto from a dict
person_response_dto_from_dict = PersonResponseDto.from_dict(person_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


