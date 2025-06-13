# UserAdminResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**avatar_color** | [**UserAvatarColor**](UserAvatarColor.md) |  | 
**created_at** | **datetime** |  | 
**deleted_at** | **datetime** |  | 
**email** | **str** |  | 
**id** | **str** |  | 
**is_admin** | **bool** |  | 
**license** | [**UserLicense**](UserLicense.md) |  | 
**name** | **str** |  | 
**oauth_id** | **str** |  | 
**profile_changed_at** | **datetime** |  | 
**profile_image_path** | **str** |  | 
**quota_size_in_bytes** | **int** |  | 
**quota_usage_in_bytes** | **int** |  | 
**should_change_password** | **bool** |  | 
**status** | [**UserStatus**](UserStatus.md) |  | 
**storage_label** | **str** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from immich_python_sdk.models.user_admin_response_dto import UserAdminResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of UserAdminResponseDto from a JSON string
user_admin_response_dto_instance = UserAdminResponseDto.from_json(json)
# print the JSON string representation of the object
print(UserAdminResponseDto.to_json())

# convert the object into a dict
user_admin_response_dto_dict = user_admin_response_dto_instance.to_dict()
# create an instance of UserAdminResponseDto from a dict
user_admin_response_dto_from_dict = UserAdminResponseDto.from_dict(user_admin_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


