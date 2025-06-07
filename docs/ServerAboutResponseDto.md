# ServerAboutResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**build** | **str** |  | [optional] 
**build_image** | **str** |  | [optional] 
**build_image_url** | **str** |  | [optional] 
**build_url** | **str** |  | [optional] 
**exiftool** | **str** |  | [optional] 
**ffmpeg** | **str** |  | [optional] 
**imagemagick** | **str** |  | [optional] 
**libvips** | **str** |  | [optional] 
**licensed** | **bool** |  | 
**nodejs** | **str** |  | [optional] 
**repository** | **str** |  | [optional] 
**repository_url** | **str** |  | [optional] 
**source_commit** | **str** |  | [optional] 
**source_ref** | **str** |  | [optional] 
**source_url** | **str** |  | [optional] 
**third_party_bug_feature_url** | **str** |  | [optional] 
**third_party_documentation_url** | **str** |  | [optional] 
**third_party_source_url** | **str** |  | [optional] 
**third_party_support_url** | **str** |  | [optional] 
**version** | **str** |  | 
**version_url** | **str** |  | 

## Example

```python
from immich_python_sdk.models.server_about_response_dto import ServerAboutResponseDto

# TODO update the JSON string below
json = "{}"
# create an instance of ServerAboutResponseDto from a JSON string
server_about_response_dto_instance = ServerAboutResponseDto.from_json(json)
# print the JSON string representation of the object
print(ServerAboutResponseDto.to_json())

# convert the object into a dict
server_about_response_dto_dict = server_about_response_dto_instance.to_dict()
# create an instance of ServerAboutResponseDto from a dict
server_about_response_dto_from_dict = ServerAboutResponseDto.from_dict(server_about_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


