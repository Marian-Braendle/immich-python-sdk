# ServerConfigDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**external_domain** | **str** |  | 
**is_initialized** | **bool** |  | 
**is_onboarded** | **bool** |  | 
**login_page_message** | **str** |  | 
**map_dark_style_url** | **str** |  | 
**map_light_style_url** | **str** |  | 
**oauth_button_text** | **str** |  | 
**public_users** | **bool** |  | 
**trash_days** | **int** |  | 
**user_delete_delay** | **int** |  | 

## Example

```python
from immich_python_sdk.models.server_config_dto import ServerConfigDto

# TODO update the JSON string below
json = "{}"
# create an instance of ServerConfigDto from a JSON string
server_config_dto_instance = ServerConfigDto.from_json(json)
# print the JSON string representation of the object
print(ServerConfigDto.to_json())

# convert the object into a dict
server_config_dto_dict = server_config_dto_instance.to_dict()
# create an instance of ServerConfigDto from a dict
server_config_dto_from_dict = ServerConfigDto.from_dict(server_config_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


