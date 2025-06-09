# DuplicateDetectionConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**max_distance** | **float** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.duplicate_detection_config import DuplicateDetectionConfig

# TODO update the JSON string below
json = "{}"
# create an instance of DuplicateDetectionConfig from a JSON string
duplicate_detection_config_instance = DuplicateDetectionConfig.from_json(json)
# print the JSON string representation of the object
print(DuplicateDetectionConfig.to_json())

# convert the object into a dict
duplicate_detection_config_dict = duplicate_detection_config_instance.to_dict()
# create an instance of DuplicateDetectionConfig from a dict
duplicate_detection_config_from_dict = DuplicateDetectionConfig.from_dict(duplicate_detection_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


