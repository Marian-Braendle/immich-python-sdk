# UserLicense


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activated_at** | **datetime** |  | 
**activation_key** | **str** |  | 
**license_key** | **str** |  | 

## Example

```python
from immich_python_sdk.models.user_license import UserLicense

# TODO update the JSON string below
json = "{}"
# create an instance of UserLicense from a JSON string
user_license_instance = UserLicense.from_json(json)
# print the JSON string representation of the object
print(UserLicense.to_json())

# convert the object into a dict
user_license_dict = user_license_instance.to_dict()
# create an instance of UserLicense from a dict
user_license_from_dict = UserLicense.from_dict(user_license_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


