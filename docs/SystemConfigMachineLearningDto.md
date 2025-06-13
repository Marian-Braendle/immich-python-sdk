# SystemConfigMachineLearningDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**clip** | [**CLIPConfig**](CLIPConfig.md) |  | 
**duplicate_detection** | [**DuplicateDetectionConfig**](DuplicateDetectionConfig.md) |  | 
**enabled** | **bool** |  | 
**facial_recognition** | [**FacialRecognitionConfig**](FacialRecognitionConfig.md) |  | 
**url** | **str** | This property was deprecated in v1.122.0 | [optional] 
**urls** | **List[str]** |  | 

## Example

```python
from immich_python_sdk.models.system_config_machine_learning_dto import SystemConfigMachineLearningDto

# TODO update the JSON string below
json = "{}"
# create an instance of SystemConfigMachineLearningDto from a JSON string
system_config_machine_learning_dto_instance = SystemConfigMachineLearningDto.from_json(json)
# print the JSON string representation of the object
print(SystemConfigMachineLearningDto.to_json())

# convert the object into a dict
system_config_machine_learning_dto_dict = system_config_machine_learning_dto_instance.to_dict()
# create an instance of SystemConfigMachineLearningDto from a dict
system_config_machine_learning_dto_from_dict = SystemConfigMachineLearningDto.from_dict(system_config_machine_learning_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


