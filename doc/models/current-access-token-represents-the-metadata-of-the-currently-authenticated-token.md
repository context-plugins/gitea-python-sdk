
# Current Access Token Represents the Metadata of the Currently Authenticated Token

*This model accepts additional fields of type Any.*

## Structure

`CurrentAccessTokenRepresentsTheMetadataOfTheCurrentlyAuthenticatedToken`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | The timestamp when the token was created |
| `id` | `int` | Optional | The unique identifier of the access token |
| `last_used_at` | `datetime` | Optional | The timestamp when the token was last used |
| `name` | `str` | Optional | The name of the access token |
| `scopes` | `List[str]` | Optional | The scopes granted to this access token |
| `user` | [`UserMetaRepresentsMinimalUserInformationForTheTokenOwner`](../../doc/models/user-meta-represents-minimal-user-information-for-the-token-owner.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.current_access_token_represents_the_metadata_of_the_currently_authenticated_token import CurrentAccessTokenRepresentsTheMetadataOfTheCurrentlyAuthenticatedToken

current_access_token_represents_the_metadata_of_the_currently_authenticated_token = CurrentAccessTokenRepresentsTheMetadataOfTheCurrentlyAuthenticatedToken(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id=188,
    last_used_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    name='name6',
    scopes=[
        'scopes4',
        'scopes3'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

