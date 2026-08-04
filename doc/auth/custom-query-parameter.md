
# Custom Query Parameter



Documentation for accessing and setting credentials for AccessToken.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| access_token | `str` | This authentication option is deprecated for removal in Gitea 1.23. Please use AuthorizationHeaderToken instead. | `access_token` |



**Note:** Auth credentials can be set using `AccessTokenCredentials` object, passed in as named parameter `access_token_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```python
from giteaapi.giteaapi_client import GiteaapiClient
from giteaapi.http.auth.access_token import AccessTokenCredentials

client = GiteaapiClient(
    access_token_credentials=AccessTokenCredentials(
        access_token='access_token'
    )
)
```


