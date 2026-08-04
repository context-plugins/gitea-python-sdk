
# Custom Header Signature



Documentation for accessing and setting credentials for TOTPHeader.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| X-GITEA-OTP | `str` | Must be used in combination with BasicAuth if two-factor authentication is enabled. | `x_gitea_otp` |



**Note:** Auth credentials can be set using `TotpHeaderCredentials` object, passed in as named parameter `totp_header_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```python
from giteaapi.giteaapi_client import GiteaapiClient
from giteaapi.http.auth.totp_header import TotpHeaderCredentials

client = GiteaapiClient(
    totp_header_credentials=TotpHeaderCredentials(
        x_gitea_otp='X-GITEA-OTP'
    )
)
```


