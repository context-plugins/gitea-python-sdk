
# User Meta Represents Minimal User Information for the Token Owner

*This model accepts additional fields of type Any.*

## Structure

`UserMetaRepresentsMinimalUserInformationForTheTokenOwner`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Optional | The unique identifier of the user |
| `login` | `str` | Optional | The username of the user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.user_meta_represents_minimal_user_information_for_the_token_owner import UserMetaRepresentsMinimalUserInformationForTheTokenOwner

user_meta_represents_minimal_user_information_for_the_token_owner = UserMetaRepresentsMinimalUserInformationForTheTokenOwner(
    id=6,
    login='login2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

