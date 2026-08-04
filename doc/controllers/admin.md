# Admin

```python
admin_api = client.admin
```

## Class Name

`AdminApi`

## Methods

* [List Admin Workflow Jobs](../../doc/controllers/admin.md#list-admin-workflow-jobs)
* [Get Admin Runners](../../doc/controllers/admin.md#get-admin-runners)
* [Admin Create Runner Registration Token](../../doc/controllers/admin.md#admin-create-runner-registration-token)
* [Get Admin Runner](../../doc/controllers/admin.md#get-admin-runner)
* [Delete Admin Runner](../../doc/controllers/admin.md#delete-admin-runner)
* [Update Admin Runner](../../doc/controllers/admin.md#update-admin-runner)
* [List Admin Workflow Runs](../../doc/controllers/admin.md#list-admin-workflow-runs)
* [Admin Cron List](../../doc/controllers/admin.md#admin-cron-list)
* [Admin Cron Run](../../doc/controllers/admin.md#admin-cron-run)
* [Admin Get All Emails](../../doc/controllers/admin.md#admin-get-all-emails)
* [Admin Search Emails](../../doc/controllers/admin.md#admin-search-emails)
* [Admin List Hooks](../../doc/controllers/admin.md#admin-list-hooks)
* [Admin Create Hook](../../doc/controllers/admin.md#admin-create-hook)
* [Admin Get Hook](../../doc/controllers/admin.md#admin-get-hook)
* [Admin Delete Hook](../../doc/controllers/admin.md#admin-delete-hook)
* [Admin Edit Hook](../../doc/controllers/admin.md#admin-edit-hook)
* [Admin Get All Orgs](../../doc/controllers/admin.md#admin-get-all-orgs)
* [Admin Unadopted List](../../doc/controllers/admin.md#admin-unadopted-list)
* [Admin Adopt Repository](../../doc/controllers/admin.md#admin-adopt-repository)
* [Admin Delete Unadopted Repository](../../doc/controllers/admin.md#admin-delete-unadopted-repository)
* [Admin Search Users](../../doc/controllers/admin.md#admin-search-users)
* [Admin Create User](../../doc/controllers/admin.md#admin-create-user)
* [Admin Delete User](../../doc/controllers/admin.md#admin-delete-user)
* [Admin Edit User](../../doc/controllers/admin.md#admin-edit-user)
* [Admin List User Badges](../../doc/controllers/admin.md#admin-list-user-badges)
* [Admin Add User Badges](../../doc/controllers/admin.md#admin-add-user-badges)
* [Admin Delete User Badges](../../doc/controllers/admin.md#admin-delete-user-badges)
* [Admin Create Public Key](../../doc/controllers/admin.md#admin-create-public-key)
* [Admin Delete User Public Key](../../doc/controllers/admin.md#admin-delete-user-public-key)
* [Admin Create Org](../../doc/controllers/admin.md#admin-create-org)
* [Admin Rename User](../../doc/controllers/admin.md#admin-rename-user)
* [Admin Create Repo](../../doc/controllers/admin.md#admin-create-repo)


# List Admin Workflow Jobs

Lists all jobs

```python
def list_admin_workflow_jobs(self,
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
result = admin_api.list_admin_workflow_jobs()

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


# Get Admin Runners

Get all runners

```python
def get_admin_runners(self,
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
result = admin_api.get_admin_runners()

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


# Admin Create Runner Registration Token

Get a global actions runner registration token

```python
def admin_create_runner_registration_token(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: RegistrationToken is response related to registration token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = admin_api.admin_create_runner_registration_token()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Admin Runner

Get a global runner

```python
def get_admin_runner(self,
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

result = admin_api.get_admin_runner(runner_id)

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


# Delete Admin Runner

Delete a global runner

```python
def delete_admin_runner(self,
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

result = admin_api.delete_admin_runner(runner_id)

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


# Update Admin Runner

Update a global runner

```python
def update_admin_runner(self,
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

result = admin_api.update_admin_runner(runner_id)

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


# List Admin Workflow Runs

Lists all runs

```python
def list_admin_workflow_runs(self,
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
result = admin_api.list_admin_workflow_runs()

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


# Admin Cron List

List cron tasks

```python
def admin_cron_list(self,
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

**200**: CronList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Cron]`](../../doc/models/cron.md).

## Example Usage

```python
result = admin_api.admin_cron_list()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# Admin Cron Run

Run cron task

```python
def admin_cron_run(self,
                  task)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `task` | `str` | Template, Required | task to run |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
task = 'task4'

result = admin_api.admin_cron_run(task)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Admin Get All Emails

List all emails

```python
def admin_get_all_emails(self,
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

**200**: EmailList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Email]`](../../doc/models/email.md).

## Example Usage

```python
result = admin_api.admin_get_all_emails()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# Admin Search Emails

Search all emails

```python
def admin_search_emails(self,
                       q=None,
                       page=None,
                       limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `str` | Query, Optional | keyword |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: EmailList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Email]`](../../doc/models/email.md).

## Example Usage

```python
result = admin_api.admin_search_emails()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# Admin List Hooks

List system's webhooks

```python
def admin_list_hooks(self,
                    page=None,
                    limit=None,
                    mtype="system")
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |
| `mtype` | [`Type3`](../../doc/models/type-3.md) | Query, Optional | system, default or both kinds of webhooks<br><br>**Default**: `"system"` |

## Response Type

**200**: HookList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Hook]`](../../doc/models/hook.md).

## Example Usage

```python
mtype = Type3.SYSTEM

result = admin_api.admin_list_hooks(
    mtype=mtype
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Create Hook

Create a hook

```python
def admin_create_hook(self,
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

result = admin_api.admin_create_hook(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Get Hook

Get a hook

```python
def admin_get_hook(self,
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

result = admin_api.admin_get_hook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Delete Hook

Delete a hook

```python
def admin_delete_hook(self,
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

result = admin_api.admin_delete_hook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Edit Hook

Update a hook

```python
def admin_edit_hook(self,
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

result = admin_api.admin_edit_hook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Get All Orgs

List all organizations

```python
def admin_get_all_orgs(self,
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

**200**: OrganizationList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Organization]`](../../doc/models/organization.md).

## Example Usage

```python
result = admin_api.admin_get_all_orgs()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# Admin Unadopted List

List unadopted repositories

```python
def admin_unadopted_list(self,
                        page=None,
                        limit=None,
                        pattern=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |
| `pattern` | `str` | Query, Optional | pattern of repositories to search for |

## Response Type

**200**: StringSlice

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[str]`.

## Example Usage

```python
result = admin_api.admin_unadopted_list()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# Admin Adopt Repository

Adopt unadopted files as a repository

```python
def admin_adopt_repository(self,
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

result = admin_api.admin_adopt_repository(
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


# Admin Delete Unadopted Repository

Delete unadopted files

```python
def admin_delete_unadopted_repository(self,
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

result = admin_api.admin_delete_unadopted_repository(
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


# Admin Search Users

Search users according filter conditions

```python
def admin_search_users(self,
                      source_id=None,
                      login_name=None,
                      page=None,
                      limit=None,
                      sort=None,
                      order=None,
                      q=None,
                      visibility=None,
                      is_active=None,
                      is_admin=None,
                      is_restricted=None,
                      is_2_fa_enabled=None,
                      is_prohibit_login=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `source_id` | `int` | Query, Optional | ID of the user's login source to search for |
| `login_name` | `str` | Query, Optional | identifier of the user, provided by the external authenticator |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |
| `sort` | `str` | Query, Optional | sort users by attribute. Supported values are "name", "created", "updated" and "id". Default is "name" |
| `order` | `str` | Query, Optional | sort order, either "asc" (ascending) or "desc" (descending). Default is "asc", ignored if "sort" is not specified. |
| `q` | `str` | Query, Optional | search term (username, full name, email) |
| `visibility` | `str` | Query, Optional | visibility filter. Supported values are "public", "limited" and "private". |
| `is_active` | `bool` | Query, Optional | filter active users |
| `is_admin` | `bool` | Query, Optional | filter admin users |
| `is_restricted` | `bool` | Query, Optional | filter restricted users |
| `is_2_fa_enabled` | `bool` | Query, Optional | filter 2FA enabled users |
| `is_prohibit_login` | `bool` | Query, Optional | filter login prohibited users |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
result = admin_api.admin_search_users()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin Create User

Create a user

```python
def admin_create_user(self,
                     body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateUserOption`](../../doc/models/create-user-option.md) | Body, Optional | - |

## Response Type

**201**: User

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`User`](../../doc/models/user.md).

## Example Usage

```python
body = CreateUserOption(
    email='email0',
    username='username4',
    login_name='empty'
)

result = admin_api.admin_create_user(
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin Delete User

Delete a user

```python
def admin_delete_user(self,
                     username,
                     purge=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to delete |
| `purge` | `bool` | Query, Optional | purge the user from the system completely |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

result = admin_api.admin_delete_user(username)

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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin Edit User

Edit an existing user

```python
def admin_edit_user(self,
                   username,
                   body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose data is to be edited |
| `body` | [`EditUserOption`](../../doc/models/edit-user-option.md) | Body, Optional | - |

## Response Type

**200**: User

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`User`](../../doc/models/user.md).

## Example Usage

```python
username = 'username0'

body = EditUserOption(
    login_name='empty',
    source_id=28
)

result = admin_api.admin_edit_user(
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin List User Badges

List a user's badges

```python
def admin_list_user_badges(self,
                          username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose badges are to be listed |

## Response Type

**200**: BadgeList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Badge]`](../../doc/models/badge.md).

## Example Usage

```python
username = 'username0'

result = admin_api.admin_list_user_badges(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Admin Add User Badges

Add a badge to a user

```python
def admin_add_user_badges(self,
                         username,
                         body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user to whom a badge is to be added |
| `body` | [`UserBadgeOption`](../../doc/models/user-badge-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

body = UserBadgeOption(
    badge_slugs=[
        'badge1',
        'badge2'
    ]
)

result = admin_api.admin_add_user_badges(
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
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |


# Admin Delete User Badges

Remove a badge from a user

```python
def admin_delete_user_badges(self,
                            username,
                            body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose badge is to be deleted |
| `body` | [`UserBadgeOption`](../../doc/models/user-badge-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

body = UserBadgeOption(
    badge_slugs=[
        'badge1',
        'badge2'
    ]
)

result = admin_api.admin_delete_user_badges(
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
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin Create Public Key

Add a public key on behalf of a user

```python
def admin_create_public_key(self,
                           username,
                           key=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user who is to receive a public key |
| `key` | [`CreateKeyOption`](../../doc/models/create-key-option.md) | Body, Optional | - |

## Response Type

**201**: PublicKey

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`PublicKey`](../../doc/models/public-key.md).

## Example Usage

```python
username = 'username0'

result = admin_api.admin_create_public_key(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin Delete User Public Key

Delete a user's public key

```python
def admin_delete_user_public_key(self,
                                username,
                                id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose public key is to be deleted |
| `id` | `int` | Template, Required | id of the key to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

id = 112

result = admin_api.admin_delete_user_public_key(
    username,
    id
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


# Admin Create Org

Create an organization

```python
def admin_create_org(self,
                    username,
                    organization)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user who will own the created organization |
| `organization` | [`CreateOrgOption`](../../doc/models/create-org-option.md) | Body, Required | - |

## Response Type

**201**: Organization

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Organization`](../../doc/models/organization.md).

## Example Usage

```python
username = 'username0'

organization = CreateOrgOption(
    username='username6'
)

result = admin_api.admin_create_org(
    username,
    organization
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin Rename User

Rename a user

```python
def admin_rename_user(self,
                     username,
                     body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | current username of the user |
| `body` | [`RenameUserOption`](../../doc/models/rename-user-option.md) | Body, Required | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
username = 'username0'

body = RenameUserOption(
    new_username='new_username0'
)

result = admin_api.admin_rename_user(
    username,
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
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Admin Create Repo

Create a repository on behalf of a user

```python
def admin_create_repo(self,
                     username,
                     repository)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user who will own the created repository |
| `repository` | [`CreateRepoOption`](../../doc/models/create-repo-option.md) | Body, Required | - |

## Response Type

**201**: Repository

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Repository`](../../doc/models/repository.md).

## Example Usage

```python
username = 'username0'

repository = CreateRepoOption(
    name='name0'
)

result = admin_api.admin_create_repo(
    username,
    repository
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
| 404 | APINotFound is a not found empty response | `ApiException` |
| 409 | APIError is error format response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |

