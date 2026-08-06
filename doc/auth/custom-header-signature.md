
# Custom Header Signature



Documentation for accessing and setting credentials for AuthorizationHeaderToken.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| Authorization | `str` | API tokens must be prepended with "token" followed by a space. | `authorization` |



**Note:** Auth credentials can be set using `AuthorizationHeaderTokenCredentials` object, passed in as named parameter `authorization_header_token_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```python
from gitea.gitea_client import GiteaClient
from gitea.http.auth.authorization_header_token import AuthorizationHeaderTokenCredentials

client = GiteaClient(
    authorization_header_token_credentials=AuthorizationHeaderTokenCredentials(
        authorization='Authorization'
    )
)
```


