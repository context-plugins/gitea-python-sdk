
# Custom Header Signature



Documentation for accessing and setting credentials for SudoHeader.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| Sudo | `str` | Sudo API request as the user provided as the key. Admin privileges are required. | `sudo` |



**Note:** Auth credentials can be set using `SudoHeaderCredentials` object, passed in as named parameter `sudo_header_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```python
from gitea.gitea_client import GiteaClient
from gitea.http.auth.sudo_header import SudoHeaderCredentials

client = GiteaClient(
    sudo_header_credentials=SudoHeaderCredentials(
        sudo='Sudo'
    )
)
```


