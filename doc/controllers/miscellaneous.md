# Miscellaneous

```python
miscellaneous_api = client.miscellaneous
```

## Class Name

`MiscellaneousApi`

## Methods

* [List Gitignores Templates](../../doc/controllers/miscellaneous.md#list-gitignores-templates)
* [Get Gitignore Template Info](../../doc/controllers/miscellaneous.md#get-gitignore-template-info)
* [List Label Templates](../../doc/controllers/miscellaneous.md#list-label-templates)
* [Get Label Template Info](../../doc/controllers/miscellaneous.md#get-label-template-info)
* [List License Templates](../../doc/controllers/miscellaneous.md#list-license-templates)
* [Get License Template Info](../../doc/controllers/miscellaneous.md#get-license-template-info)
* [Render Markdown](../../doc/controllers/miscellaneous.md#render-markdown)
* [Render Markdown Raw](../../doc/controllers/miscellaneous.md#render-markdown-raw)
* [Render Markup](../../doc/controllers/miscellaneous.md#render-markup)
* [Get Signing Key](../../doc/controllers/miscellaneous.md#get-signing-key)
* [Get Signing Key SSH](../../doc/controllers/miscellaneous.md#get-signing-key-ssh)
* [Get Current Token](../../doc/controllers/miscellaneous.md#get-current-token)
* [Delete Current Token](../../doc/controllers/miscellaneous.md#delete-current-token)
* [Get Version](../../doc/controllers/miscellaneous.md#get-version)


# List Gitignores Templates

Returns a list of all gitignore templates

```python
def list_gitignores_templates(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: GitignoreTemplateList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[str]`.

## Example Usage

```python
result = miscellaneous_api.list_gitignores_templates()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Gitignore Template Info

Returns information about a gitignore template

```python
def get_gitignore_template_info(self,
                               name)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Template, Required | name of the template |

## Response Type

**200**: GitignoreTemplateInfo

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GitignoreTemplateInfo`](../../doc/models/gitignore-template-info.md).

## Example Usage

```python
name = 'name0'

result = miscellaneous_api.get_gitignore_template_info(name)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# List Label Templates

Returns a list of all label templates

```python
def list_label_templates(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: LabelTemplateList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[str]`.

## Example Usage

```python
result = miscellaneous_api.list_label_templates()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Label Template Info

Returns all labels in a template

```python
def get_label_template_info(self,
                           name)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Template, Required | name of the template |

## Response Type

**200**: LabelTemplateInfo

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[LabelTemplate]`](../../doc/models/label-template.md).

## Example Usage

```python
name = 'name0'

result = miscellaneous_api.get_label_template_info(name)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# List License Templates

Returns a list of all license templates

```python
def list_license_templates(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: LicenseTemplateList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[LicensesTemplateListEntry]`](../../doc/models/licenses-template-list-entry.md).

## Example Usage

```python
result = miscellaneous_api.list_license_templates()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get License Template Info

Returns information about a license template

```python
def get_license_template_info(self,
                             name)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Template, Required | name of the license |

## Response Type

**200**: LicenseTemplateInfo

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`LicenseTemplateInfo`](../../doc/models/license-template-info.md).

## Example Usage

```python
name = 'name0'

result = miscellaneous_api.get_license_template_info(name)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Render Markdown

Render a markdown document as HTML

```python
def render_markdown(self,
                   body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`MarkdownOption`](../../doc/models/markdown-option.md) | Body, Optional | - |

## Response Type

**200**: MarkdownRender is a rendered markdown document

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `str`.

## Example Usage

```python
result = miscellaneous_api.render_markdown()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Render Markdown Raw

Render raw markdown as HTML

```python
def render_markdown_raw(self,
                       body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Body, Required | Request body to render |

## Response Type

**200**: MarkdownRender is a rendered markdown document

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `str`.

## Example Usage

```python
body = 'body6'

result = miscellaneous_api.render_markdown_raw(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Render Markup

Render a markup document as HTML

```python
def render_markup(self,
                 body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`MarkupOption`](../../doc/models/markup-option.md) | Body, Optional | - |

## Response Type

**200**: MarkupRender is a rendered markup document

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `str`.

## Example Usage

```python
result = miscellaneous_api.render_markup()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Get Signing Key

Get default signing-key.gpg

```python
def get_signing_key(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: GPG armored public key

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `str`.

## Example Usage

```python
result = miscellaneous_api.get_signing_key()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Signing Key SSH

Get default signing-key.pub

```python
def get_signing_key_ssh(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: ssh public key

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `str`.

## Example Usage

```python
result = miscellaneous_api.get_signing_key_ssh()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Current Token

Get the currently authenticated token

```python
def get_current_token(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: CurrentAccessToken represents the currently authenticated access token.

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`CurrentAccessTokenRepresentsTheMetadataOfTheCurrentlyAuthenticatedToken`](../../doc/models/current-access-token-represents-the-metadata-of-the-currently-authenticated-token.md).

## Example Usage

```python
result = miscellaneous_api.get_current_token()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Current Token

Delete the currently authenticated token

```python
def delete_current_token(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**204**: token deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = miscellaneous_api.delete_current_token()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Version

Returns the version of the Gitea application

```python
def get_version(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: ServerVersion

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ServerVersion`](../../doc/models/server-version.md).

## Example Usage

```python
result = miscellaneous_api.get_version()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

