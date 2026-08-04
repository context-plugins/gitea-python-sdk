
# Oauth 2 Application Represents an Oauth 2 Application

*This model accepts additional fields of type Any.*

## Structure

`Oauth2ApplicationRepresentsAnOauth2Application`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `client_id` | `str` | Optional | The client ID of the OAuth2 application |
| `client_secret` | `str` | Optional | The client secret of the OAuth2 application |
| `confidential_client` | `bool` | Optional | Whether the client is confidential |
| `created` | `datetime` | Optional | The timestamp when the application was created |
| `id` | `int` | Optional | The unique identifier of the OAuth2 application |
| `name` | `str` | Optional | The name of the OAuth2 application |
| `redirect_uris` | `List[str]` | Optional | The list of allowed redirect URIs |
| `skip_secondary_authorization` | `bool` | Optional | Whether to skip secondary authorization |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.oauth_2_application_represents_an_oauth_2_application import Oauth2ApplicationRepresentsAnOauth2Application

oauth_2_application_represents_an_oauth_2_application = Oauth2ApplicationRepresentsAnOauth2Application(
    client_id='client_id2',
    client_secret='client_secret8',
    confidential_client=False,
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id=34,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

