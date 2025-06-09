# CLIPConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**model_name** | **str** |  | 

## Example

```python
from immich_python_sdk.models.clip_config import CLIPConfig

# TODO update the JSON string below
json = "{}"
# create an instance of CLIPConfig from a JSON string
clip_config_instance = CLIPConfig.from_json(json)
# print the JSON string representation of the object
print(CLIPConfig.to_json())

# convert the object into a dict
clip_config_dict = clip_config_instance.to_dict()
# create an instance of CLIPConfig from a dict
clip_config_from_dict = CLIPConfig.from_dict(clip_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


