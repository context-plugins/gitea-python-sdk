
# Create Oauth 2 Application Options

CreateOAuth2ApplicationOptions holds options to create an oauth2 application

*This model accepts additional fields of type Any.*

## Structure

`CreateOauth2ApplicationOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `confidential_client` | `bool` | Optional | Whether the client is confidential |
| `name` | `str` | Optional | The name of the OAuth2 application |
| `redirect_uris` | `List[str]` | Optional | The list of allowed redirect URIs |
| `skip_secondary_authorization` | `bool` | Optional | Whether to skip secondary authorization |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_oauth_2_application_options import CreateOauth2ApplicationOptions

create_oauth_2_application_options = CreateOauth2ApplicationOptions(
    confidential_client=False,
    name='name6',
    redirect_uris=[
        'redirect_uris9',
        'redirect_uris0'
    ],
    skip_secondary_authorization=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

