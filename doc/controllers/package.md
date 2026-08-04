# Package

```python
package_api = client.package
```

## Class Name

`PackageApi`

## Methods

* [List Packages](../../doc/controllers/package.md#list-packages)
* [List Package Versions](../../doc/controllers/package.md#list-package-versions)
* [Delete Package](../../doc/controllers/package.md#delete-package)
* [Get Latest Package Version](../../doc/controllers/package.md#get-latest-package-version)
* [Link Package](../../doc/controllers/package.md#link-package)
* [Unlink Package](../../doc/controllers/package.md#unlink-package)
* [Get Package](../../doc/controllers/package.md#get-package)
* [Delete Package Version](../../doc/controllers/package.md#delete-package-version)
* [List Package Files](../../doc/controllers/package.md#list-package-files)


# List Packages

Gets all packages of an owner

```python
def list_packages(self,
                 owner,
                 page=None,
                 limit=None,
                 mtype=None,
                 q=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the packages |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |
| `mtype` | [`Type4`](../../doc/models/type-4.md) | Query, Optional | package type filter |
| `q` | `str` | Query, Optional | name filter |

## Response Type

**200**: PackageList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Package]`](../../doc/models/package.md).

## Example Usage

```python
owner = 'owner4'

result = package_api.list_packages(owner)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# List Package Versions

Gets all versions of a package

```python
def list_package_versions(self,
                         owner,
                         mtype,
                         name,
                         page=None,
                         limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: PackageList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Package]`](../../doc/models/package.md).

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

result = package_api.list_package_versions(
    owner,
    mtype,
    name
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Delete Package

Delete a package

```python
def delete_package(self,
                  owner,
                  mtype,
                  name)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

result = package_api.delete_package(
    owner,
    mtype,
    name
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Get Latest Package Version

Gets the latest version of a package

```python
def get_latest_package_version(self,
                              owner,
                              mtype,
                              name)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |

## Response Type

**200**: Package

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Package`](../../doc/models/package.md).

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

result = package_api.get_latest_package_version(
    owner,
    mtype,
    name
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Link Package

Link a package to a repository

```python
def link_package(self,
                owner,
                mtype,
                name,
                repo_name)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |
| `repo_name` | `str` | Template, Required | name of the repository to link. |

## Response Type

**201**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

repo_name = 'repo_name6'

result = package_api.link_package(
    owner,
    mtype,
    name,
    repo_name
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Unlink Package

Unlink a package from a repository

```python
def unlink_package(self,
                  owner,
                  mtype,
                  name)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |

## Response Type

**201**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

result = package_api.unlink_package(
    owner,
    mtype,
    name
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Get Package

Gets a package

```python
def get_package(self,
               owner,
               mtype,
               name,
               version)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |
| `version` | `str` | Template, Required | version of the package |

## Response Type

**200**: Package

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Package`](../../doc/models/package.md).

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

version = 'version4'

result = package_api.get_package(
    owner,
    mtype,
    name,
    version
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Delete Package Version

Delete a package version

```python
def delete_package_version(self,
                          owner,
                          mtype,
                          name,
                          version)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |
| `version` | `str` | Template, Required | version of the package |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

version = 'version4'

result = package_api.delete_package_version(
    owner,
    mtype,
    name,
    version
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# List Package Files

Gets all files of a package

```python
def list_package_files(self,
                      owner,
                      mtype,
                      name,
                      version)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the package |
| `mtype` | `str` | Template, Required | type of the package |
| `name` | `str` | Template, Required | name of the package |
| `version` | `str` | Template, Required | version of the package |

## Response Type

**200**: PackageFileList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[PackageFile]`](../../doc/models/package-file.md).

## Example Usage

```python
owner = 'owner4'

mtype = 'type0'

name = 'name0'

version = 'version4'

result = package_api.list_package_files(
    owner,
    mtype,
    name,
    version
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |

