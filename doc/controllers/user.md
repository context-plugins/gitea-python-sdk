# User

```python
user_api = client.user
```

## Class Name

`UserApi`

## Methods

* [User Get Current](../../doc/controllers/user.md#user-get-current)
* [Get User Workflow Jobs](../../doc/controllers/user.md#get-user-workflow-jobs)
* [Get User Runners](../../doc/controllers/user.md#get-user-runners)
* [User Create Runner Registration Token](../../doc/controllers/user.md#user-create-runner-registration-token)
* [Get User Runner](../../doc/controllers/user.md#get-user-runner)
* [Delete User Runner](../../doc/controllers/user.md#delete-user-runner)
* [Update User Runner](../../doc/controllers/user.md#update-user-runner)
* [Get User Workflow Runs](../../doc/controllers/user.md#get-user-workflow-runs)
* [Update User Secret](../../doc/controllers/user.md#update-user-secret)
* [Delete User Secret](../../doc/controllers/user.md#delete-user-secret)
* [Get User Variables List](../../doc/controllers/user.md#get-user-variables-list)
* [Get User Variable](../../doc/controllers/user.md#get-user-variable)
* [Update User Variable](../../doc/controllers/user.md#update-user-variable)
* [Create User Variable](../../doc/controllers/user.md#create-user-variable)
* [Delete User Variable](../../doc/controllers/user.md#delete-user-variable)
* [User Get Oauth 2 Application](../../doc/controllers/user.md#user-get-oauth-2-application)
* [User Create OAuth 2 Application](../../doc/controllers/user.md#user-create-oauth-2-application)
* [User Get OAuth 2 Application 1](../../doc/controllers/user.md#user-get-oauth-2-application-1)
* [User Delete OAuth 2 Application](../../doc/controllers/user.md#user-delete-oauth-2-application)
* [User Update OAuth 2 Application](../../doc/controllers/user.md#user-update-oauth-2-application)
* [User Update Avatar](../../doc/controllers/user.md#user-update-avatar)
* [User Delete Avatar](../../doc/controllers/user.md#user-delete-avatar)
* [User List Blocks](../../doc/controllers/user.md#user-list-blocks)
* [User Check User Block](../../doc/controllers/user.md#user-check-user-block)
* [User Block User](../../doc/controllers/user.md#user-block-user)
* [User Unblock User](../../doc/controllers/user.md#user-unblock-user)
* [User List Emails](../../doc/controllers/user.md#user-list-emails)
* [User Add Email](../../doc/controllers/user.md#user-add-email)
* [User Delete Email](../../doc/controllers/user.md#user-delete-email)
* [User Current List Followers](../../doc/controllers/user.md#user-current-list-followers)
* [User Current List Following](../../doc/controllers/user.md#user-current-list-following)
* [User Current Check Following](../../doc/controllers/user.md#user-current-check-following)
* [User Current Put Follow](../../doc/controllers/user.md#user-current-put-follow)
* [User Current Delete Follow](../../doc/controllers/user.md#user-current-delete-follow)
* [Get Verification Token](../../doc/controllers/user.md#get-verification-token)
* [User Verify GPG Key](../../doc/controllers/user.md#user-verify-gpg-key)
* [User Current List GPG Keys](../../doc/controllers/user.md#user-current-list-gpg-keys)
* [User Current Post GPG Key](../../doc/controllers/user.md#user-current-post-gpg-key)
* [User Current Get GPG Key](../../doc/controllers/user.md#user-current-get-gpg-key)
* [User Current Delete GPG Key](../../doc/controllers/user.md#user-current-delete-gpg-key)
* [User List Hooks](../../doc/controllers/user.md#user-list-hooks)
* [User Create Hook](../../doc/controllers/user.md#user-create-hook)
* [User Get Hook](../../doc/controllers/user.md#user-get-hook)
* [User Delete Hook](../../doc/controllers/user.md#user-delete-hook)
* [User Edit Hook](../../doc/controllers/user.md#user-edit-hook)
* [User Current List Keys](../../doc/controllers/user.md#user-current-list-keys)
* [User Current Post Key](../../doc/controllers/user.md#user-current-post-key)
* [User Current Get Key](../../doc/controllers/user.md#user-current-get-key)
* [User Current Delete Key](../../doc/controllers/user.md#user-current-delete-key)
* [User Current List Repos](../../doc/controllers/user.md#user-current-list-repos)
* [Get User Settings](../../doc/controllers/user.md#get-user-settings)
* [Update User Settings](../../doc/controllers/user.md#update-user-settings)
* [User Current List Starred](../../doc/controllers/user.md#user-current-list-starred)
* [User Current Check Starring](../../doc/controllers/user.md#user-current-check-starring)
* [User Current Put Star](../../doc/controllers/user.md#user-current-put-star)
* [User Current Delete Star](../../doc/controllers/user.md#user-current-delete-star)
* [User Get Stop Watches](../../doc/controllers/user.md#user-get-stop-watches)
* [User Current List Subscriptions](../../doc/controllers/user.md#user-current-list-subscriptions)
* [User List Teams](../../doc/controllers/user.md#user-list-teams)
* [User Current Tracked Times](../../doc/controllers/user.md#user-current-tracked-times)
* [User Search](../../doc/controllers/user.md#user-search)
* [User Get](../../doc/controllers/user.md#user-get)
* [User List Activity Feeds](../../doc/controllers/user.md#user-list-activity-feeds)
* [User List Followers](../../doc/controllers/user.md#user-list-followers)
* [User List Following](../../doc/controllers/user.md#user-list-following)
* [User Check Following](../../doc/controllers/user.md#user-check-following)
* [User List GPG Keys](../../doc/controllers/user.md#user-list-gpg-keys)
* [User Get Heatmap Data](../../doc/controllers/user.md#user-get-heatmap-data)
* [User List Keys](../../doc/controllers/user.md#user-list-keys)
* [User List Repos](../../doc/controllers/user.md#user-list-repos)
* [User List Starred](../../doc/controllers/user.md#user-list-starred)
* [User List Subscriptions](../../doc/controllers/user.md#user-list-subscriptions)
* [User Get Tokens](../../doc/controllers/user.md#user-get-tokens)
* [User Create Token](../../doc/controllers/user.md#user-create-token)
* [User Delete Access Token](../../doc/controllers/user.md#user-delete-access-token)


# User Get Current

Get the authenticated user

```python
def user_get_current(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: User

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`User`](../../doc/models/user.md).

## Example Usage

```python
result = user_api.user_get_current()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get User Workflow Jobs

Get workflow jobs

```python
def get_user_workflow_jobs(self,
                          status=None,
                          page=None,
                          limit=None,
                          sort=None,
                          order=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | `str` | Query, Optional | workflow status (pending, queued, in_progress, failure, success, skipped) |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |
| `sort` | `str` | Query, Optional | sort jobs by attribute. Supported values are "id". Default is "id" |
| `order` | `str` | Query, Optional | sort order, either "asc" (ascending) or "desc" (descending). Default is "asc" |

## Response Type

**200**: WorkflowJobsList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionWorkflowJobsResponse`](../../doc/models/action-workflow-jobs-response.md).

## Example Usage

```python
result = user_api.get_user_workflow_jobs()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Get User Runners

Get user-level runners

```python
def get_user_runners(self,
                    disabled=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disabled` | `bool` | Query, Optional | filter by disabled status (true or false) |

## Response Type

**200**: RunnerList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionRunnersResponse`](../../doc/models/action-runners-response.md).

## Example Usage

```python
result = user_api.get_user_runners()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Create Runner Registration Token

Get a user's actions runner registration token

```python
def user_create_runner_registration_token(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: RegistrationToken is response related to registration token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = user_api.user_create_runner_registration_token()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get User Runner

Get a user-level runner

```python
def get_user_runner(self,
                   runner_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `runner_id` | `str` | Template, Required | id of the runner |

## Response Type

**200**: Runner

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionRunner`](../../doc/models/action-runner.md).

## Example Usage

```python
runner_id = 'runner_id0'

result = user_api.get_user_runner(runner_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Delete User Runner

Delete a user-level runner

```python
def delete_user_runner(self,
                      runner_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `runner_id` | `str` | Template, Required | id of the runner |

## Response Type

**204**: runner has been deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
runner_id = 'runner_id0'

result = user_api.delete_user_runner(runner_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Update User Runner

Update a user-level runner

```python
def update_user_runner(self,
                      runner_id,
                      body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `runner_id` | `str` | Template, Required | id of the runner |
| `body` | [`EditActionRunnerOptionRepresentsTheEditableFieldsForARunner`](../../doc/models/edit-action-runner-option-represents-the-editable-fields-for-a-runner.md) | Body, Optional | - |

## Response Type

**200**: Runner

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionRunner`](../../doc/models/action-runner.md).

## Example Usage

```python
runner_id = 'runner_id0'

result = user_api.update_user_runner(runner_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Get User Workflow Runs

Get workflow runs

```python
def get_user_workflow_runs(self,
                          event=None,
                          branch=None,
                          status=None,
                          actor=None,
                          head_sha=None,
                          page=None,
                          limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `event` | `str` | Query, Optional | workflow event name |
| `branch` | `str` | Query, Optional | workflow branch |
| `status` | `str` | Query, Optional | workflow status (pending, queued, in_progress, failure, success, skipped) |
| `actor` | `str` | Query, Optional | triggered by user |
| `head_sha` | `str` | Query, Optional | triggering sha of the workflow run |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: WorkflowRunsList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionWorkflowRunsResponse`](../../doc/models/action-workflow-runs-response.md).

## Example Usage

```python
result = user_api.get_user_workflow_runs()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Update User Secret

Create or Update a secret value in a user scope

```python
def update_user_secret(self,
                      secretname,
                      body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `secretname` | `str` | Template, Required | name of the secret |
| `body` | [`CreateOrUpdateSecretOption`](../../doc/models/create-or-update-secret-option.md) | Body, Optional | - |

## Response Type

**204**: response when updating a secret

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
secretname = 'secretname4'

result = user_api.update_user_secret(secretname)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Delete User Secret

Delete a secret in a user scope

```python
def delete_user_secret(self,
                      secretname)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `secretname` | `str` | Template, Required | name of the secret |

## Response Type

**204**: delete one secret of the user

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
secretname = 'secretname4'

result = user_api.delete_user_secret(secretname)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Get User Variables List

Get the user-level list of variables which is created by current doer

```python
def get_user_variables_list(self,
                           page=None,
                           limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: VariableList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[ActionVariable]`](../../doc/models/action-variable.md).

## Example Usage

```python
result = user_api.get_user_variables_list()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Get User Variable

Get a user-level variable which is created by current doer

```python
def get_user_variable(self,
                     variablename)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `variablename` | `str` | Template, Required | name of the variable |

## Response Type

**200**: ActionVariable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionVariable`](../../doc/models/action-variable.md).

## Example Usage

```python
variablename = 'variablename4'

result = user_api.get_user_variable(variablename)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Update User Variable

Update a user-level variable which is created by current doer

```python
def update_user_variable(self,
                        variablename,
                        body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `variablename` | `str` | Template, Required | name of the variable |
| `body` | [`UpdateVariableOption`](../../doc/models/update-variable-option.md) | Body, Optional | - |

## Response Type

**204**: response when updating a variable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
variablename = 'variablename4'

result = user_api.update_user_variable(variablename)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Create User Variable

Create a user-level variable

```python
def create_user_variable(self,
                        variablename,
                        body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `variablename` | `str` | Template, Required | name of the variable |
| `body` | [`CreateVariableOption`](../../doc/models/create-variable-option.md) | Body, Optional | - |

## Response Type

**201**: successfully created the user-level variable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
variablename = 'variablename4'

result = user_api.create_user_variable(variablename)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 409 | variable name already exists. | `ApiException` |


# Delete User Variable

Delete a user-level variable which is created by current doer

```python
def delete_user_variable(self,
                        variablename)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `variablename` | `str` | Template, Required | name of the variable |

## Response Type

**204**: response when deleting a variable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
variablename = 'variablename4'

result = user_api.delete_user_variable(variablename)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Get Oauth 2 Application

List the authenticated user's oauth2 applications

```python
def user_get_oauth_2_application(self,
                                page=None,
                                limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: OAuth2ApplicationList represents a list of OAuth2 applications.

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Oauth2ApplicationRepresentsAnOauth2Application]`](../../doc/models/oauth-2-application-represents-an-oauth-2-application.md).

## Example Usage

```python
result = user_api.user_get_oauth_2_application()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Create OAuth 2 Application

creates a new OAuth2 application

```python
def user_create_oauth_2_application(self,
                                   body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateOauth2ApplicationOptions`](../../doc/models/create-oauth-2-application-options.md) | Body, Required | - |

## Response Type

**201**: OAuth2Application

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Oauth2ApplicationRepresentsAnOauth2Application`](../../doc/models/oauth-2-application-represents-an-oauth-2-application.md).

## Example Usage

```python
body = CreateOauth2ApplicationOptions()

result = user_api.user_create_oauth_2_application(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |


# User Get OAuth 2 Application 1

get an OAuth2 Application

```python
def user_get_oauth_2_application_1(self,
                                  id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | Application ID to be found |

## Response Type

**200**: OAuth2Application

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Oauth2ApplicationRepresentsAnOauth2Application`](../../doc/models/oauth-2-application-represents-an-oauth-2-application.md).

## Example Usage

```python
id = 112

result = user_api.user_get_oauth_2_application_1(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Delete OAuth 2 Application

delete an OAuth2 Application

```python
def user_delete_oauth_2_application(self,
                                   id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | token to be deleted |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

result = user_api.user_delete_oauth_2_application(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Update OAuth 2 Application

update an OAuth2 Application, this includes regenerating the client secret

```python
def user_update_oauth_2_application(self,
                                   id,
                                   body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | application to be updated |
| `body` | [`CreateOauth2ApplicationOptions`](../../doc/models/create-oauth-2-application-options.md) | Body, Required | - |

## Response Type

**200**: OAuth2Application

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Oauth2ApplicationRepresentsAnOauth2Application`](../../doc/models/oauth-2-application-represents-an-oauth-2-application.md).

## Example Usage

```python
id = 112

body = CreateOauth2ApplicationOptions()

result = user_api.user_update_oauth_2_application(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Update Avatar

Update Avatar

```python
def user_update_avatar(self,
                      body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`UpdateUserAvatarOption`](../../doc/models/update-user-avatar-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = user_api.user_update_avatar()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Delete Avatar

Delete Avatar

```python
def user_delete_avatar(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = user_api.user_delete_avatar()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User List Blocks

List users blocked by the authenticated user

```python
def user_list_blocks(self,
                    page=None,
                    limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
result = user_api.user_list_blocks()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Check User Block

Check if a user is blocked by the authenticated user

```python
def user_check_user_block(self,
                         username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to check |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

result = user_api.user_check_user_block(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Block User

Block a user

```python
def user_block_user(self,
                   username,
                   note=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to block |
| `note` | `str` | Query, Optional | optional note for the block |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

result = user_api.user_block_user(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# User Unblock User

Unblock a user

```python
def user_unblock_user(self,
                     username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to unblock |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

result = user_api.user_unblock_user(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# User List Emails

List the authenticated user's email addresses

```python
def user_list_emails(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: EmailList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Email]`](../../doc/models/email.md).

## Example Usage

```python
result = user_api.user_list_emails()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Add Email

Add email addresses

```python
def user_add_email(self,
                  body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateEmailOption`](../../doc/models/create-email-option.md) | Body, Optional | - |

## Response Type

**201**: EmailList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Email]`](../../doc/models/email.md).

## Example Usage

```python
result = user_api.user_add_email()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# User Delete Email

Delete email addresses

```python
def user_delete_email(self,
                     body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DeleteEmailOption`](../../doc/models/delete-email-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = user_api.user_delete_email()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current List Followers

List the authenticated user's followers

```python
def user_current_list_followers(self,
                               page=None,
                               limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
result = user_api.user_current_list_followers()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current List Following

List the users that the authenticated user is following

```python
def user_current_list_following(self,
                               page=None,
                               limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
result = user_api.user_current_list_following()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current Check Following

Check whether a user is followed by the authenticated user

```python
def user_current_check_following(self,
                                username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to check for authenticated followers |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

result = user_api.user_current_check_following(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current Put Follow

Follow a user

```python
def user_current_put_follow(self,
                           username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to follow |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

result = user_api.user_current_put_follow(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current Delete Follow

Unfollow a user

```python
def user_current_delete_follow(self,
                              username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to unfollow |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

result = user_api.user_current_delete_follow(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Get Verification Token

Get a Token to verify

```python
def get_verification_token(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: APIString is a string response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `str`.

## Example Usage

```python
result = user_api.get_verification_token()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Verify GPG Key

Verify a GPG key

```python
def user_verify_gpg_key(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**201**: GPGKey

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GpgKey`](../../doc/models/gpg-key.md).

## Example Usage

```python
result = user_api.user_verify_gpg_key()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# User Current List GPG Keys

List the authenticated user's GPG keys

```python
def user_current_list_gpg_keys(self,
                              page=None,
                              limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: GPGKeyList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[GpgKey]`](../../doc/models/gpg-key.md).

## Example Usage

```python
result = user_api.user_current_list_gpg_keys()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current Post GPG Key

Create a GPG key

```python
def user_current_post_gpg_key(self,
                             form=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `form` | [`CreateGpgKeyOption`](../../doc/models/create-gpg-key-option.md) | Body, Optional | - |

## Response Type

**201**: GPGKey

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GpgKey`](../../doc/models/gpg-key.md).

## Example Usage

```python
result = user_api.user_current_post_gpg_key()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# User Current Get GPG Key

Get a GPG key

```python
def user_current_get_gpg_key(self,
                            id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of key to get |

## Response Type

**200**: GPGKey

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GpgKey`](../../doc/models/gpg-key.md).

## Example Usage

```python
id = 112

result = user_api.user_current_get_gpg_key(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current Delete GPG Key

Remove a GPG key

```python
def user_current_delete_gpg_key(self,
                               id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of key to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

result = user_api.user_current_delete_gpg_key(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Hooks

List the authenticated user's webhooks

```python
def user_list_hooks(self,
                   page=None,
                   limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: HookList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Hook]`](../../doc/models/hook.md).

## Example Usage

```python
result = user_api.user_list_hooks()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Create Hook

Create a hook

```python
def user_create_hook(self,
                    body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateHookOption`](../../doc/models/create-hook-option.md) | Body, Required | - |

## Response Type

**201**: Hook

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Hook`](../../doc/models/hook.md).

## Example Usage

```python
body = CreateHookOption(
    config={
        'key0': 'config0'
    },
    mtype=Type.MSTEAMS,
    active=False
)

result = user_api.user_create_hook(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Get Hook

Get a hook

```python
def user_get_hook(self,
                 id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the hook to get |

## Response Type

**200**: Hook

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Hook`](../../doc/models/hook.md).

## Example Usage

```python
id = 112

result = user_api.user_get_hook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Delete Hook

Delete a hook

```python
def user_delete_hook(self,
                    id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the hook to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

result = user_api.user_delete_hook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Edit Hook

Update a hook

```python
def user_edit_hook(self,
                  id,
                  body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the hook to update |
| `body` | [`EditHookOption`](../../doc/models/edit-hook-option.md) | Body, Optional | - |

## Response Type

**200**: Hook

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Hook`](../../doc/models/hook.md).

## Example Usage

```python
id = 112

result = user_api.user_edit_hook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current List Keys

List the authenticated user's public keys

```python
def user_current_list_keys(self,
                          fingerprint=None,
                          page=None,
                          limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fingerprint` | `str` | Query, Optional | fingerprint of the key |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: PublicKeyList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[PublicKey]`](../../doc/models/public-key.md).

## Example Usage

```python
result = user_api.user_current_list_keys()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current Post Key

Create a public key

```python
def user_current_post_key(self,
                         body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateKeyOption`](../../doc/models/create-key-option.md) | Body, Optional | - |

## Response Type

**201**: PublicKey

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`PublicKey`](../../doc/models/public-key.md).

## Example Usage

```python
result = user_api.user_current_post_key()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# User Current Get Key

Get a public key

```python
def user_current_get_key(self,
                        id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of key to get |

## Response Type

**200**: PublicKey

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`PublicKey`](../../doc/models/public-key.md).

## Example Usage

```python
id = 112

result = user_api.user_current_get_key(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current Delete Key

Delete a public key

```python
def user_current_delete_key(self,
                           id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of key to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

result = user_api.user_current_delete_key(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current List Repos

List the repos that the authenticated user owns

```python
def user_current_list_repos(self,
                           page=None,
                           limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
result = user_api.user_current_list_repos()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get User Settings

Get user settings

```python
def get_user_settings(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: UserSettings

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[UserSettings]`](../../doc/models/user-settings.md).

## Example Usage

```python
result = user_api.get_user_settings()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Update User Settings

Update user settings

```python
def update_user_settings(self,
                        body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`UserSettingsOptions`](../../doc/models/user-settings-options.md) | Body, Optional | - |

## Response Type

**200**: UserSettings

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[UserSettings]`](../../doc/models/user-settings.md).

## Example Usage

```python
result = user_api.update_user_settings()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current List Starred

The repos that the authenticated user has starred

```python
def user_current_list_starred(self,
                             page=None,
                             limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
result = user_api.user_current_list_starred()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# User Current Check Starring

Whether the authenticated is starring the repo

```python
def user_current_check_starring(self,
                               owner,
                               repo)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = user_api.user_current_check_starring(
    owner,
    repo
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current Put Star

Star the given repo

```python
def user_current_put_star(self,
                         owner,
                         repo)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo to star |
| `repo` | `str` | Template, Required | name of the repo to star |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = user_api.user_current_put_star(
    owner,
    repo
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Current Delete Star

Unstar the given repo

```python
def user_current_delete_star(self,
                            owner,
                            repo)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo to unstar |
| `repo` | `str` | Template, Required | name of the repo to unstar |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = user_api.user_current_delete_star(
    owner,
    repo
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Get Stop Watches

Get list of all existing stopwatches

```python
def user_get_stop_watches(self,
                         page=None,
                         limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: StopWatchList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[StopWatch]`](../../doc/models/stop-watch.md).

## Example Usage

```python
result = user_api.user_get_stop_watches()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current List Subscriptions

List repositories watched by the authenticated user

```python
def user_current_list_subscriptions(self,
                                   page=None,
                                   limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
result = user_api.user_current_list_subscriptions()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User List Teams

List all the teams a user belongs to

```python
def user_list_teams(self,
                   page=None,
                   limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: TeamList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Team]`](../../doc/models/team.md).

## Example Usage

```python
result = user_api.user_list_teams()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Current Tracked Times

List the current user's tracked times

```python
def user_current_tracked_times(self,
                              page=None,
                              limit=None,
                              since=None,
                              before=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |
| `since` | `datetime` | Query, Optional | Only show times updated after the given time. This is a timestamp in RFC 3339 format |
| `before` | `datetime` | Query, Optional | Only show times updated before the given time. This is a timestamp in RFC 3339 format |

## Response Type

**200**: TrackedTimeList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[TrackedTime]`](../../doc/models/tracked-time.md).

## Example Usage

```python
result = user_api.user_current_tracked_times()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Search

Search for users

```python
def user_search(self,
               q=None,
               uid=None,
               page=None,
               limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `str` | Query, Optional | keyword |
| `uid` | `int` | Query, Optional | ID of the user to search for |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: SearchResults of a successful search

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`UserSearchResponse`](../../doc/models/user-search-response.md).

## Example Usage

```python
result = user_api.user_search()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# User Get

Get a user

```python
def user_get(self,
            username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose data is to be listed |

## Response Type

**200**: User

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`User`](../../doc/models/user.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_get(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Activity Feeds

List a user's activity feeds

```python
def user_list_activity_feeds(self,
                            username,
                            only_performed_by=None,
                            date=None,
                            page=None,
                            limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose activity feeds are to be listed |
| `only_performed_by` | `bool` | Query, Optional | if true, only show actions performed by the requested user |
| `date` | `date` | Query, Optional | the date of the activities to be found |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: ActivityFeedsList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Activity]`](../../doc/models/activity.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_activity_feeds(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Followers

List the given user's followers

```python
def user_list_followers(self,
                       username,
                       page=None,
                       limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose followers are to be listed |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_followers(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Following

List the users that the given user is following

```python
def user_list_following(self,
                       username,
                       page=None,
                       limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose followed users are to be listed |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_following(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Check Following

Check if one user is following another user

```python
def user_check_following(self,
                        username,
                        target)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the following user |
| `target` | `str` | Template, Required | username of the followed user |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

target = 'target2'

result = user_api.user_check_following(
    username,
    target
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


# User List GPG Keys

List the given user's GPG keys

```python
def user_list_gpg_keys(self,
                      username,
                      page=None,
                      limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose GPG key list is to be obtained |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: GPGKeyList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[GpgKey]`](../../doc/models/gpg-key.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_gpg_keys(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Get Heatmap Data

Get a user's heatmap

```python
def user_get_heatmap_data(self,
                         username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose heatmap is to be obtained |

## Response Type

**200**: UserHeatmapData

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[UserHeatmapData]`](../../doc/models/user-heatmap-data.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_get_heatmap_data(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Keys

List the given user's public keys

```python
def user_list_keys(self,
                  username,
                  fingerprint=None,
                  page=None,
                  limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose public keys are to be listed |
| `fingerprint` | `str` | Query, Optional | fingerprint of the key |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: PublicKeyList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[PublicKey]`](../../doc/models/public-key.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_keys(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Repos

List the repos owned by the given user

```python
def user_list_repos(self,
                   username,
                   page=None,
                   limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose owned repos are to be listed |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_repos(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Starred

The repos that the given user has starred

```python
def user_list_starred(self,
                     username,
                     page=None,
                     limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose starred repos are to be listed |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_starred(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User List Subscriptions

List the repositories watched by a user

```python
def user_list_subscriptions(self,
                           username,
                           page=None,
                           limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose watched repos are to be listed |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_list_subscriptions(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# User Get Tokens

List the authenticated user's access tokens

```python
def user_get_tokens(self,
                   username,
                   page=None,
                   limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of to user whose access tokens are to be listed |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: AccessTokenList represents a list of API access token.

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[AccessTokenRepresentsAnApiAccessToken]`](../../doc/models/access-token-represents-an-api-access-token.md).

## Example Usage

```python
username = 'username0'

result = user_api.user_get_tokens(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# User Create Token

Create an access token

```python
def user_create_token(self,
                     username,
                     body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose token is to be created |
| `body` | [`CreateAccessTokenOption`](../../doc/models/create-access-token-option.md) | Body, Optional | - |

## Response Type

**201**: AccessToken represents an API access token.

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`AccessTokenRepresentsAnApiAccessToken`](../../doc/models/access-token-represents-an-api-access-token.md).

## Example Usage

```python
username = 'username0'

body = CreateAccessTokenOption(
    name='name6',
    scopes=[
        'all',
        'read:activitypub',
        'read:issue',
        'write:misc',
        'read:notification',
        'read:organization',
        'read:package',
        'read:repository',
        'read:user'
    ]
)

result = user_api.user_create_token(
    username,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | APIError is error format response | `ApiException` |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# User Delete Access Token

delete an access token

```python
def user_delete_access_token(self,
                            username,
                            token)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose token is to be deleted |
| `token` | `str` | Template, Required | token to be deleted, identified by ID and if not available by name |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

token = 'token6'

result = user_api.user_delete_access_token(
    username,
    token
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIError is error format response | `ApiException` |

