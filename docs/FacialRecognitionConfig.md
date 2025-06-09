# FacialRecognitionConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**max_distance** | **float** |  | 
**min_faces** | **int** |  | 
**min_score** | **float** |  | 
**model_name** | **str** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.facial_recognition_config import FacialRecognitionConfig

# TODO update the JSON string below
json = "{}"
# create an instance of FacialRecognitionConfig from a JSON string
facial_recognition_config_instance = FacialRecognitionConfig.from_json(json)
# print the JSON string representation of the object
print(FacialRecognitionConfig.to_json())

# convert the object into a dict
facial_recognition_config_dict = facial_recognition_config_instance.to_dict()
# create an instance of FacialRecognitionConfig from a dict
facial_recognition_config_from_dict = FacialRecognitionConfig.from_dict(facial_recognition_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


