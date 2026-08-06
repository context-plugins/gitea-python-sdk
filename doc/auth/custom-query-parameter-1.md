
# Custom Query Parameter



Documentation for accessing and setting credentials for SudoParam.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| sudo | `str` | Sudo API request as the user provided as the key. Admin privileges are required. | `sudo` |



**Note:** Auth credentials can be set using `SudoParamCredentials` object, passed in as named parameter `sudo_param_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```python
from gitea.gitea_client import GiteaClient
from gitea.http.auth.sudo_param import SudoParamCredentials

client = GiteaClient(
    sudo_param_credentials=SudoParamCredentials(
        sudo='sudo'
    )
)
```


