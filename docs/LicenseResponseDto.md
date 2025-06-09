# LicenseResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activated_at** | **datetime** |  | 
**activation_key** | **str** |  | 
**license_key** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.license_response_dto import LicenseResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of LicenseResponseDto from a JSON string
license_response_dto_instance = LicenseResponseDto.from_json(json)
# print the JSON string representation of the object
print(LicenseResponseDto.to_json())

# convert the object into a dict
license_response_dto_dict = license_response_dto_instance.to_dict()
# create an instance of LicenseResponseDto from a dict
license_response_dto_from_dict = LicenseResponseDto.from_dict(license_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


