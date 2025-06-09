# EmailNotificationsUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**album_invite** | **bool** |  | [optional] 
**album_update** | **bool** |  | [optional] 
**enabled** | **bool** |  | [optional] 

## Example

```python
from immich_python_sdk_asyncio.models.email_notifications_update import EmailNotificationsUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of EmailNotificationsUpdate from a JSON string
email_notifications_update_instance = EmailNotificationsUpdate.from_json(json)
# print the JSON string representation of the object
print(EmailNotificationsUpdate.to_json())

# convert the object into a dict
email_notifications_update_dict = email_notifications_update_instance.to_dict()
# create an instance of EmailNotificationsUpdate from a dict
email_notifications_update_from_dict = EmailNotificationsUpdate.from_dict(email_notifications_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


