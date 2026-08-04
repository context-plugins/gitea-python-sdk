# Settings

```python
settings_api = client.settings
```

## Class Name

`SettingsApi`

## Methods

* [Get General API Settings](../../doc/controllers/settings.md#get-general-api-settings)
* [Get General Attachment Settings](../../doc/controllers/settings.md#get-general-attachment-settings)
* [Get General Repository Settings](../../doc/controllers/settings.md#get-general-repository-settings)
* [Get General UI Settings](../../doc/controllers/settings.md#get-general-ui-settings)


# Get General API Settings

Get instance's global settings for api

```python
def get_general_api_settings(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: GeneralAPISettings

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GeneralApiSettings`](../../doc/models/general-api-settings.md).

## Example Usage

```python
result = settings_api.get_general_api_settings()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get General Attachment Settings

Get instance's global settings for Attachment

```python
def get_general_attachment_settings(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: GeneralAttachmentSettings

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GeneralAttachmentSettings`](../../doc/models/general-attachment-settings.md).

## Example Usage

```python
result = settings_api.get_general_attachment_settings()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get General Repository Settings

Get instance's global settings for repositories

```python
def get_general_repository_settings(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: GeneralRepoSettings

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GeneralRepoSettings`](../../doc/models/general-repo-settings.md).

## Example Usage

```python
result = settings_api.get_general_repository_settings()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get General UI Settings

Get instance's global settings for ui

```python
def get_general_ui_settings(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: GeneralUISettings

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GeneralUiSettings`](../../doc/models/general-ui-settings.md).

## Example Usage

```python
result = settings_api.get_general_ui_settings()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

