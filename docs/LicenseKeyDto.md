# LicenseKeyDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activation_key** | **str** |  | 
**license_key** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.license_key_dto import LicenseKeyDto

# TODO update the JSON string below
json = "{}"
# create an instance of LicenseKeyDto from a JSON string
license_key_dto_instance = LicenseKeyDto.from_json(json)
# print the JSON string representation of the object
print(LicenseKeyDto.to_json())

# convert the object into a dict
license_key_dto_dict = license_key_dto_instance.to_dict()
# create an instance of LicenseKeyDto from a dict
license_key_dto_from_dict = LicenseKeyDto.from_dict(license_key_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


