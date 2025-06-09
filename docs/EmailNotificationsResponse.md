# EmailNotificationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**album_invite** | **bool** |  | 
**album_update** | **bool** |  | 
**enabled** | **bool** |  | 

## Example

```python
from immich_python_sdk_asyncio.models.email_notifications_response import EmailNotificationsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of EmailNotificationsResponse from a JSON string
email_notifications_response_instance = EmailNotificationsResponse.from_json(json)
# print the JSON string representation of the object
print(EmailNotificationsResponse.to_json())

# convert the object into a dict
email_notifications_response_dict = email_notifications_response_instance.to_dict()
# create an instance of EmailNotificationsResponse from a dict
email_notifications_response_from_dict = EmailNotificationsResponse.from_dict(email_notifications_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


