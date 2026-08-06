
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| default_host | `str` | *Default*: `"www.example.com/api/v1"` |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| http_client_instance | `Union[Session, HttpClientProvider]` | The Http Client passed from the sdk user for making requests |
| override_http_client_configuration | `bool` | The value which determines to override properties of the passed Http Client from the sdk user |
| http_call_back | `HttpCallBack` | The callback value that is invoked before and after an HTTP call is made to an endpoint |
| timeout | `float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `int` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| backoff_factor | `float` | A backoff factor to apply between attempts after the second try. <br> **Default: 2** |
| retry_statuses | `Array of int` | The http statuses on which retry is to be done. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array of string` | The http methods on which retry is to be done. <br> **Default: ["GET", "PUT", "GET", "PUT"]** |
| proxy_settings | [`ProxySettings`](../doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](../doc/logging-configuration.md) | The SDK logging configuration for API calls |
| access_token_credentials | [`AccessTokenCredentials`](auth/custom-query-parameter.md) | The credential object for Custom Query Parameter |
| authorization_header_token_credentials | [`AuthorizationHeaderTokenCredentials`](auth/custom-header-signature.md) | The credential object for Custom Header Signature |
| basic_auth_credentials | [`BasicAuthCredentials`](auth/basic-authentication.md) | The credential object for Basic Authentication |
| sudo_header_credentials | [`SudoHeaderCredentials`](auth/custom-header-signature-1.md) | The credential object for Custom Header Signature |
| sudo_param_credentials | [`SudoParamCredentials`](auth/custom-query-parameter-1.md) | The credential object for Custom Query Parameter |
| totp_header_credentials | [`TotpHeaderCredentials`](auth/custom-header-signature-2.md) | The credential object for Custom Header Signature |
| token_credentials | [`TokenCredentials`](auth/custom-query-parameter-2.md) | The credential object for Custom Query Parameter |

The API client can be initialized as follows:

## Code-Based Client Initialization

```python
import logging

from gitea.configuration import Environment
from gitea.gitea_client import GiteaClient
from gitea.http.auth.access_token import AccessTokenCredentials
from gitea.http.auth.authorization_header_token import AuthorizationHeaderTokenCredentials
from gitea.http.auth.basic_auth import BasicAuthCredentials
from gitea.http.auth.sudo_header import SudoHeaderCredentials
from gitea.http.auth.sudo_param import SudoParamCredentials
from gitea.http.auth.token import TokenCredentials
from gitea.http.auth.totp_header import TotpHeaderCredentials
from gitea.logging.configuration.api_logging_configuration import LoggingConfiguration
from gitea.logging.configuration.api_logging_configuration import RequestLoggingConfiguration
from gitea.logging.configuration.api_logging_configuration import ResponseLoggingConfiguration

client = GiteaClient(
    access_token_credentials=AccessTokenCredentials(
        access_token='access_token'
    ),
    authorization_header_token_credentials=AuthorizationHeaderTokenCredentials(
        authorization='Authorization'
    ),
    basic_auth_credentials=BasicAuthCredentials(
        username='Username',
        password='Password'
    ),
    sudo_header_credentials=SudoHeaderCredentials(
        sudo='Sudo'
    ),
    sudo_param_credentials=SudoParamCredentials(
        sudo='sudo'
    ),
    totp_header_credentials=TotpHeaderCredentials(
        x_gitea_otp='X-GITEA-OTP'
    ),
    token_credentials=TokenCredentials(
        token='token'
    ),
    environment=Environment.PRODUCTION,
    default_host='www.example.com/api/v1',
    logging_configuration=LoggingConfiguration(
        log_level=logging.INFO,
        request_logging_config=RequestLoggingConfiguration(
            log_body=True
        ),
        response_logging_config=ResponseLoggingConfiguration(
            log_headers=True
        )
    )
)
```

## Environment-Based Client Initialization

```python
from gitea.gitea_client import GiteaClient

# Specify the path to your .env file if it’s located outside the project’s root directory.
client = GiteaClient.from_environment(dotenv_path='/path/to/.env')
```

See the [Environment-Based Client Initialization](../doc/environment-based-client-initialization.md) section for details.

## Gitea API Client

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

## Apis

| Name | Description |
|  --- | --- |
| admin | Gets AdminApi |
| miscellaneous | Gets MiscellaneousApi |
| notification | Gets NotificationApi |
| organization | Gets OrganizationApi |
| package | Gets PackageApi |
| issue | Gets IssueApi |
| repository | Gets RepositoryApi |
| settings | Gets SettingsApi |
| user | Gets UserApi |

