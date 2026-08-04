
# Custom Query Parameter



Documentation for accessing and setting credentials for Token.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| token | `str` | This authentication option is deprecated for removal in Gitea 1.23. Please use AuthorizationHeaderToken instead. | `token` |



**Note:** Auth credentials can be set using `TokenCredentials` object, passed in as named parameter `token_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```python
from giteaapi.giteaapi_client import GiteaapiClient
from giteaapi.http.auth.token import TokenCredentials

client = GiteaapiClient(
    token_credentials=TokenCredentials(
        token='token'
    )
)
```


