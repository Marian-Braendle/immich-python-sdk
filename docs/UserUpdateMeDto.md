# UserUpdateMeDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**avatar_color** | [**UserAvatarColor**](UserAvatarColor.md) |  | [optional] 
**email** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**password** | **str** |  | [optional] 

## Example

```python
from immich_python_sdk_asyncio.models.user_update_me_dto import UserUpdateMeDto

# TODO update the JSON string below
json = "{}"
# create an instance of UserUpdateMeDto from a JSON string
user_update_me_dto_instance = UserUpdateMeDto.from_json(json)
# print the JSON string representation of the object
print(UserUpdateMeDto.to_json())

# convert the object into a dict
user_update_me_dto_dict = user_update_me_dto_instance.to_dict()
# create an instance of UserUpdateMeDto from a dict
user_update_me_dto_from_dict = UserUpdateMeDto.from_dict(user_update_me_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


