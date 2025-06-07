# PeopleResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [default to True]
**sidebar_web** | **bool** |  | [default to False]

## Example

```python
from immich_python_sdk.models.people_response import PeopleResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PeopleResponse from a JSON string
people_response_instance = PeopleResponse.from_json(json)
# print the JSON string representation of the object
print(PeopleResponse.to_json())

# convert the object into a dict
people_response_dict = people_response_instance.to_dict()
# create an instance of PeopleResponse from a dict
people_response_from_dict = PeopleResponse.from_dict(people_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


