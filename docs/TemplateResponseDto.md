# TemplateResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**html** | **str** |  | 
**name** | **str** |  | 

## Example

```python
from immich_python_sdk.models.template_response_dto import TemplateResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of TemplateResponseDto from a JSON string
template_response_dto_instance = TemplateResponseDto.from_json(json)
# print the JSON string representation of the object
print(TemplateResponseDto.to_json())

# convert the object into a dict
template_response_dto_dict = template_response_dto_instance.to_dict()
# create an instance of TemplateResponseDto from a dict
template_response_dto_from_dict = TemplateResponseDto.from_dict(template_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


