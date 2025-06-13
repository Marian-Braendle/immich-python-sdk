# PartnerResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**avatar_color** | [**UserAvatarColor**](UserAvatarColor.md) |  | 
**email** | **str** |  | 
**id** | **str** |  | 
**in_timeline** | **bool** |  | [optional] 
**name** | **str** |  | 
**profile_changed_at** | **datetime** |  | 
**profile_image_path** | **str** |  | 

## Example

```python
from immich_python_sdk.models.partner_response_dto import PartnerResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of PartnerResponseDto from a JSON string
partner_response_dto_instance = PartnerResponseDto.from_json(json)
# print the JSON string representation of the object
print(PartnerResponseDto.to_json())

# convert the object into a dict
partner_response_dto_dict = partner_response_dto_instance.to_dict()
# create an instance of PartnerResponseDto from a dict
partner_response_dto_from_dict = PartnerResponseDto.from_dict(partner_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


