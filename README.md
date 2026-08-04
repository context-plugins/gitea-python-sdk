
# Getting Started with Gitea API

## Introduction

This documentation describes the Gitea API.

## Building

You must have Python `3.7+` installed on your system to install and run this SDK. This SDK package depends on other Python packages like pytest, etc. These dependencies are defined in the `requirements.txt` file that comes with the SDK. To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type `pip --version`. This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including `requirements.txt`) for the SDK.
* Run the command `pip install -r requirements.txt`. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&step=installDependencies)

## Installation

The following section explains how to use the giteaapi library in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&step=pyCharm)

Click on `Open` in PyCharm to browse to your generated SDK directory and then click `OK`.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&step=openProject0)

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&projectName=giteaapi&step=openProject1)

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&projectName=giteaapi&step=createDirectory)

Name the directory as "test".

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&step=nameDirectory)

Add a python file to this project.

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&projectName=giteaapi&step=createFile)

Name it "testSDK".

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&projectName=giteaapi&step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```python
from giteaapi.giteaapi_client import GiteaapiClient
```

![Add a new project in PyCharm - Step 5](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&projectName=giteaapi&libraryName=giteaapi.giteaapi_client&className=GiteaapiClient&step=projectFiles)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on `Run`

![Run Test Project - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Giteaapi-Python&projectName=giteaapi&libraryName=giteaapi.giteaapi_client&className=GiteaapiClient&step=runProject)

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| http_client_instance | `Union[Session, HttpClientProvider]` | The Http Client passed from the sdk user for making requests |
| override_http_client_configuration | `bool` | The value which determines to override properties of the passed Http Client from the sdk user |
| http_call_back | `HttpCallBack` | The callback value that is invoked before and after an HTTP call is made to an endpoint |
| timeout | `float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `int` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| backoff_factor | `float` | A backoff factor to apply between attempts after the second try. <br> **Default: 2** |
| retry_statuses | `Array of int` | The http statuses on which retry is to be done. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array of string` | The http methods on which retry is to be done. <br> **Default: ["GET", "PUT", "GET", "PUT"]** |
| proxy_settings | [`ProxySettings`](doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](doc/logging-configuration.md) | The SDK logging configuration for API calls |
| access_token_credentials | [`AccessTokenCredentials`](doc/auth/custom-query-parameter.md) | The credential object for Custom Query Parameter |
| authorization_header_token_credentials | [`AuthorizationHeaderTokenCredentials`](doc/auth/custom-header-signature.md) | The credential object for Custom Header Signature |
| basic_auth_credentials | [`BasicAuthCredentials`](doc/auth/basic-authentication.md) | The credential object for Basic Authentication |
| sudo_header_credentials | [`SudoHeaderCredentials`](doc/auth/custom-header-signature-1.md) | The credential object for Custom Header Signature |
| sudo_param_credentials | [`SudoParamCredentials`](doc/auth/custom-query-parameter-1.md) | The credential object for Custom Query Parameter |
| totp_header_credentials | [`TotpHeaderCredentials`](doc/auth/custom-header-signature-2.md) | The credential object for Custom Header Signature |
| token_credentials | [`TokenCredentials`](doc/auth/custom-query-parameter-2.md) | The credential object for Custom Query Parameter |

The API client can be initialized as follows:

### Code-Based Client Initialization

```python
import logging

from giteaapi.configuration import Environment
from giteaapi.giteaapi_client import GiteaapiClient
from giteaapi.http.auth.access_token import AccessTokenCredentials
from giteaapi.http.auth.authorization_header_token import AuthorizationHeaderTokenCredentials
from giteaapi.http.auth.basic_auth import BasicAuthCredentials
from giteaapi.http.auth.sudo_header import SudoHeaderCredentials
from giteaapi.http.auth.sudo_param import SudoParamCredentials
from giteaapi.http.auth.token import TokenCredentials
from giteaapi.http.auth.totp_header import TotpHeaderCredentials
from giteaapi.logging.configuration.api_logging_configuration import LoggingConfiguration
from giteaapi.logging.configuration.api_logging_configuration import RequestLoggingConfiguration
from giteaapi.logging.configuration.api_logging_configuration import ResponseLoggingConfiguration

client = GiteaapiClient(
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

### Environment-Based Client Initialization

```python
from giteaapi.giteaapi_client import GiteaapiClient

# Specify the path to your .env file if it’s located outside the project’s root directory.
client = GiteaapiClient.from_environment(dotenv_path='/path/to/.env')
```

See the [Environment-Based Client Initialization](doc/environment-based-client-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`AccessToken (Custom Query Parameter)`](doc/auth/custom-query-parameter.md)
* [`AuthorizationHeaderToken (Custom Header Signature)`](doc/auth/custom-header-signature.md)
* [`BasicAuth (Basic Authentication)`](doc/auth/basic-authentication.md)
* [`SudoHeader (Custom Header Signature)`](doc/auth/custom-header-signature-1.md)
* [`SudoParam (Custom Query Parameter)`](doc/auth/custom-query-parameter-1.md)
* [`TOTPHeader (Custom Header Signature)`](doc/auth/custom-header-signature-2.md)
* [`Token (Custom Query Parameter)`](doc/auth/custom-query-parameter-2.md)

## List of APIs

* [Admin](doc/controllers/admin.md)
* [Miscellaneous](doc/controllers/miscellaneous.md)
* [Notification](doc/controllers/notification.md)
* [Organization](doc/controllers/organization.md)
* [Package](doc/controllers/package.md)
* [Issue](doc/controllers/issue.md)
* [Repository](doc/controllers/repository.md)
* [Settings](doc/controllers/settings.md)
* [User](doc/controllers/user.md)

## SDK Infrastructure

### Configuration

* [ProxySettings](doc/proxy-settings.md)
* [Environment-Based Client Initialization](doc/environment-based-client-initialization.md)
* [AbstractLogger](doc/abstract-logger.md)
* [LoggingConfiguration](doc/logging-configuration.md)
* [RequestLoggingConfiguration](doc/request-logging-configuration.md)
* [ResponseLoggingConfiguration](doc/response-logging-configuration.md)

### HTTP

* [HttpResponse](doc/http-response.md)
* [HttpRequest](doc/http-request.md)

### Utilities

* [ApiResponse](doc/api-response.md)
* [ApiHelper](doc/api-helper.md)
* [HttpDateTime](doc/http-date-time.md)
* [RFC3339DateTime](doc/rfc3339-date-time.md)
* [UnixDateTime](doc/unix-date-time.md)

