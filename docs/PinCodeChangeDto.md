# PinCodeChangeDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**new_pin_code** | **str** |  | 
**password** | **str** |  | [optional] 
**pin_code** | **str** |  | [optional] 

## Example

```python
from immich_python_sdk.models.pin_code_change_dto import PinCodeChangeDto

# TODO update the JSON string below
json = "{}"
# create an instance of PinCodeChangeDto from a JSON string
pin_code_change_dto_instance = PinCodeChangeDto.from_json(json)
# print the JSON string representation of the object
print(PinCodeChangeDto.to_json())

# convert the object into a dict
pin_code_change_dto_dict = pin_code_change_dto_instance.to_dict()
# create an instance of PinCodeChangeDto from a dict
pin_code_change_dto_from_dict = PinCodeChangeDto.from_dict(pin_code_change_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


