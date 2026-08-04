# Organization

```python
organization_api = client.organization
```

## Class Name

`OrganizationApi`

## Methods

* [Create Org Repo Deprecated](../../doc/controllers/organization.md#create-org-repo-deprecated)
* [Org Get All](../../doc/controllers/organization.md#org-get-all)
* [Org Create](../../doc/controllers/organization.md#org-create)
* [Org Get](../../doc/controllers/organization.md#org-get)
* [Org Delete](../../doc/controllers/organization.md#org-delete)
* [Org Edit](../../doc/controllers/organization.md#org-edit)
* [Get Org Workflow Jobs](../../doc/controllers/organization.md#get-org-workflow-jobs)
* [Get Org Runners](../../doc/controllers/organization.md#get-org-runners)
* [Org Create Runner Registration Token](../../doc/controllers/organization.md#org-create-runner-registration-token)
* [Get Org Runner](../../doc/controllers/organization.md#get-org-runner)
* [Delete Org Runner](../../doc/controllers/organization.md#delete-org-runner)
* [Update Org Runner](../../doc/controllers/organization.md#update-org-runner)
* [Get Org Workflow Runs](../../doc/controllers/organization.md#get-org-workflow-runs)
* [Org List Actions Secrets](../../doc/controllers/organization.md#org-list-actions-secrets)
* [Update Org Secret](../../doc/controllers/organization.md#update-org-secret)
* [Delete Org Secret](../../doc/controllers/organization.md#delete-org-secret)
* [Get Org Variables List](../../doc/controllers/organization.md#get-org-variables-list)
* [Get Org Variable](../../doc/controllers/organization.md#get-org-variable)
* [Update Org Variable](../../doc/controllers/organization.md#update-org-variable)
* [Create Org Variable](../../doc/controllers/organization.md#create-org-variable)
* [Delete Org Variable](../../doc/controllers/organization.md#delete-org-variable)
* [Org List Activity Feeds](../../doc/controllers/organization.md#org-list-activity-feeds)
* [Org Update Avatar](../../doc/controllers/organization.md#org-update-avatar)
* [Org Delete Avatar](../../doc/controllers/organization.md#org-delete-avatar)
* [Organization List Blocks](../../doc/controllers/organization.md#organization-list-blocks)
* [Organization Check User Block](../../doc/controllers/organization.md#organization-check-user-block)
* [Organization Block User](../../doc/controllers/organization.md#organization-block-user)
* [Organization Unblock User](../../doc/controllers/organization.md#organization-unblock-user)
* [Org List Hooks](../../doc/controllers/organization.md#org-list-hooks)
* [Org Create Hook](../../doc/controllers/organization.md#org-create-hook)
* [Org Get Hook](../../doc/controllers/organization.md#org-get-hook)
* [Org Delete Hook](../../doc/controllers/organization.md#org-delete-hook)
* [Org Edit Hook](../../doc/controllers/organization.md#org-edit-hook)
* [Org List Labels](../../doc/controllers/organization.md#org-list-labels)
* [Org Create Label](../../doc/controllers/organization.md#org-create-label)
* [Org Get Label](../../doc/controllers/organization.md#org-get-label)
* [Org Delete Label](../../doc/controllers/organization.md#org-delete-label)
* [Org Edit Label](../../doc/controllers/organization.md#org-edit-label)
* [Org List Members](../../doc/controllers/organization.md#org-list-members)
* [Org Is Member](../../doc/controllers/organization.md#org-is-member)
* [Org Delete Member](../../doc/controllers/organization.md#org-delete-member)
* [Org List Public Members](../../doc/controllers/organization.md#org-list-public-members)
* [Org Is Public Member](../../doc/controllers/organization.md#org-is-public-member)
* [Org Publicize Member](../../doc/controllers/organization.md#org-publicize-member)
* [Org Conceal Member](../../doc/controllers/organization.md#org-conceal-member)
* [Rename Org](../../doc/controllers/organization.md#rename-org)
* [Org List Repos](../../doc/controllers/organization.md#org-list-repos)
* [Create Org Repo](../../doc/controllers/organization.md#create-org-repo)
* [Org Delete Repos](../../doc/controllers/organization.md#org-delete-repos)
* [Org List Teams](../../doc/controllers/organization.md#org-list-teams)
* [Org Create Team](../../doc/controllers/organization.md#org-create-team)
* [Team Search](../../doc/controllers/organization.md#team-search)
* [Org Get Team](../../doc/controllers/organization.md#org-get-team)
* [Org Delete Team](../../doc/controllers/organization.md#org-delete-team)
* [Org Edit Team](../../doc/controllers/organization.md#org-edit-team)
* [Org List Team Activity Feeds](../../doc/controllers/organization.md#org-list-team-activity-feeds)
* [Org List Team Members](../../doc/controllers/organization.md#org-list-team-members)
* [Org List Team Member](../../doc/controllers/organization.md#org-list-team-member)
* [Org Add Team Member](../../doc/controllers/organization.md#org-add-team-member)
* [Org Remove Team Member](../../doc/controllers/organization.md#org-remove-team-member)
* [Org List Team Repos](../../doc/controllers/organization.md#org-list-team-repos)
* [Org List Team Repo](../../doc/controllers/organization.md#org-list-team-repo)
* [Org Add Team Repository](../../doc/controllers/organization.md#org-add-team-repository)
* [Org Remove Team Repository](../../doc/controllers/organization.md#org-remove-team-repository)
* [Org List Current User Orgs](../../doc/controllers/organization.md#org-list-current-user-orgs)
* [Org List User Orgs](../../doc/controllers/organization.md#org-list-user-orgs)
* [Org Get User Permissions](../../doc/controllers/organization.md#org-get-user-permissions)


# Create Org Repo Deprecated

**This endpoint is deprecated.**

Create a repository in an organization

```python
def create_org_repo_deprecated(self,
                              org,
                              body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of organization |
| `body` | [`CreateRepoOption`](../../doc/models/create-repo-option.md) | Body, Optional | - |

## Response Type

**201**: Repository

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Repository`](../../doc/models/repository.md).

## Example Usage

```python
org = 'org6'

result = organization_api.create_org_repo_deprecated(org)

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


# Org Get All

Get list of organizations

```python
def org_get_all(self,
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
result = organization_api.org_get_all()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Org Create

Create an organization

```python
def org_create(self,
              organization)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `organization` | [`CreateOrgOption`](../../doc/models/create-org-option.md) | Body, Required | - |

## Response Type

**201**: Organization

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Organization`](../../doc/models/organization.md).

## Example Usage

```python
organization = CreateOrgOption(
    username='username6'
)

result = organization_api.org_create(organization)

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


# Org Get

Get an organization

```python
def org_get(self,
           org)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization to get |

## Response Type

**200**: Organization

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Organization`](../../doc/models/organization.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_get(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Delete

Delete an organization

```python
def org_delete(self,
              org)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | organization that is to be deleted |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

result = organization_api.org_delete(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Edit

Edit an organization

```python
def org_edit(self,
            org,
            body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization to edit |
| `body` | [`EditOrgOption`](../../doc/models/edit-org-option.md) | Body, Required | - |

## Response Type

**200**: Organization

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Organization`](../../doc/models/organization.md).

## Example Usage

```python
org = 'org6'

body = EditOrgOption()

result = organization_api.org_edit(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Get Org Workflow Jobs

Get org-level workflow jobs

```python
def get_org_workflow_jobs(self,
                         org,
                         status=None,
                         page=None,
                         limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `status` | `str` | Query, Optional | workflow status (pending, queued, in_progress, failure, success, skipped) |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: WorkflowJobsList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionWorkflowJobsResponse`](../../doc/models/action-workflow-jobs-response.md).

## Example Usage

```python
org = 'org6'

result = organization_api.get_org_workflow_jobs(org)

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


# Get Org Runners

Get org-level runners

```python
def get_org_runners(self,
                   org,
                   disabled=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `disabled` | `bool` | Query, Optional | filter by disabled status (true or false) |

## Response Type

**200**: RunnerList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionRunnersResponse`](../../doc/models/action-runners-response.md).

## Example Usage

```python
org = 'org6'

result = organization_api.get_org_runners(org)

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


# Org Create Runner Registration Token

Get an organization's actions runner registration token

```python
def org_create_runner_registration_token(self,
                                        org)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |

## Response Type

**200**: RegistrationToken is response related to registration token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

result = organization_api.org_create_runner_registration_token(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Org Runner

Get an org-level runner

```python
def get_org_runner(self,
                  org,
                  runner_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `runner_id` | `str` | Template, Required | id of the runner |

## Response Type

**200**: Runner

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionRunner`](../../doc/models/action-runner.md).

## Example Usage

```python
org = 'org6'

runner_id = 'runner_id0'

result = organization_api.get_org_runner(
    org,
    runner_id
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


# Delete Org Runner

Delete an org-level runner

```python
def delete_org_runner(self,
                     org,
                     runner_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `runner_id` | `str` | Template, Required | id of the runner |

## Response Type

**204**: runner has been deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

runner_id = 'runner_id0'

result = organization_api.delete_org_runner(
    org,
    runner_id
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


# Update Org Runner

Update an org-level runner

```python
def update_org_runner(self,
                     org,
                     runner_id,
                     body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `runner_id` | `str` | Template, Required | id of the runner |
| `body` | [`EditActionRunnerOptionRepresentsTheEditableFieldsForARunner`](../../doc/models/edit-action-runner-option-represents-the-editable-fields-for-a-runner.md) | Body, Optional | - |

## Response Type

**200**: Runner

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionRunner`](../../doc/models/action-runner.md).

## Example Usage

```python
org = 'org6'

runner_id = 'runner_id0'

result = organization_api.update_org_runner(
    org,
    runner_id
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Get Org Workflow Runs

Get org-level workflow runs

```python
def get_org_workflow_runs(self,
                         org,
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
| `org` | `str` | Template, Required | name of the organization |
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
org = 'org6'

result = organization_api.get_org_workflow_runs(org)

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


# Org List Actions Secrets

List an organization's actions secrets

```python
def org_list_actions_secrets(self,
                            org,
                            page=None,
                            limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: SecretList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Secret]`](../../doc/models/secret.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_actions_secrets(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Update Org Secret

Create or Update a secret value in an organization

```python
def update_org_secret(self,
                     org,
                     secretname,
                     body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of organization |
| `secretname` | `str` | Template, Required | name of the secret |
| `body` | [`CreateOrUpdateSecretOption`](../../doc/models/create-or-update-secret-option.md) | Body, Optional | - |

## Response Type

**204**: response when updating a secret

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

secretname = 'secretname4'

result = organization_api.update_org_secret(
    org,
    secretname
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


# Delete Org Secret

Delete a secret in an organization

```python
def delete_org_secret(self,
                     org,
                     secretname)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of organization |
| `secretname` | `str` | Template, Required | name of the secret |

## Response Type

**204**: delete one secret of the organization

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

secretname = 'secretname4'

result = organization_api.delete_org_secret(
    org,
    secretname
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


# Get Org Variables List

Get an org-level variables list

```python
def get_org_variables_list(self,
                          org,
                          page=None,
                          limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: VariableList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[ActionVariable]`](../../doc/models/action-variable.md).

## Example Usage

```python
org = 'org6'

result = organization_api.get_org_variables_list(org)

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


# Get Org Variable

Get an org-level variable

```python
def get_org_variable(self,
                    org,
                    variablename)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `variablename` | `str` | Template, Required | name of the variable |

## Response Type

**200**: ActionVariable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionVariable`](../../doc/models/action-variable.md).

## Example Usage

```python
org = 'org6'

variablename = 'variablename4'

result = organization_api.get_org_variable(
    org,
    variablename
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


# Update Org Variable

Update an org-level variable

```python
def update_org_variable(self,
                       org,
                       variablename,
                       body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `variablename` | `str` | Template, Required | name of the variable |
| `body` | [`UpdateVariableOption`](../../doc/models/update-variable-option.md) | Body, Optional | - |

## Response Type

**204**: response when updating an org-level variable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

variablename = 'variablename4'

result = organization_api.update_org_variable(
    org,
    variablename
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


# Create Org Variable

Create an org-level variable

```python
def create_org_variable(self,
                       org,
                       variablename,
                       body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `variablename` | `str` | Template, Required | name of the variable |
| `body` | [`CreateVariableOption`](../../doc/models/create-variable-option.md) | Body, Optional | - |

## Response Type

**201**: successfully created the org-level variable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

variablename = 'variablename4'

result = organization_api.create_org_variable(
    org,
    variablename
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
| 409 | variable name already exists. | `ApiException` |
| 500 | APIError is error format response | `ApiException` |


# Delete Org Variable

Delete an org-level variable

```python
def delete_org_variable(self,
                       org,
                       variablename)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `variablename` | `str` | Template, Required | name of the variable |

## Response Type

**200**: ActionVariable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`ActionVariable`](../../doc/models/action-variable.md).

## Example Usage

```python
org = 'org6'

variablename = 'variablename4'

result = organization_api.delete_org_variable(
    org,
    variablename
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


# Org List Activity Feeds

List an organization's activity feeds

```python
def org_list_activity_feeds(self,
                           org,
                           date=None,
                           page=None,
                           limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the org |
| `date` | `date` | Query, Optional | the date of the activities to be found |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: ActivityFeedsList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Activity]`](../../doc/models/activity.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_activity_feeds(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Update Avatar

Update Avatar

```python
def org_update_avatar(self,
                     org,
                     body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `body` | [`UpdateUserAvatarOption`](../../doc/models/update-user-avatar-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

result = organization_api.org_update_avatar(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Delete Avatar

Delete Avatar

```python
def org_delete_avatar(self,
                     org)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

result = organization_api.org_delete_avatar(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Organization List Blocks

List users blocked by the organization

```python
def organization_list_blocks(self,
                            org,
                            page=None,
                            limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
org = 'org6'

result = organization_api.organization_list_blocks(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Organization Check User Block

Check if a user is blocked by the organization

```python
def organization_check_user_block(self,
                                 org,
                                 username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user to check |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.organization_check_user_block(
    org,
    username
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


# Organization Block User

Block a user

```python
def organization_block_user(self,
                           org,
                           username,
                           note=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user to block |
| `note` | `str` | Query, Optional | optional note for the block |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.organization_block_user(
    org,
    username
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Organization Unblock User

Unblock a user

```python
def organization_unblock_user(self,
                             org,
                             username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user to unblock |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.organization_unblock_user(
    org,
    username
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Org List Hooks

List an organization's webhooks

```python
def org_list_hooks(self,
                  org,
                  page=None,
                  limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: HookList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Hook]`](../../doc/models/hook.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_hooks(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Create Hook

Create a hook

```python
def org_create_hook(self,
                   org,
                   body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `body` | [`CreateHookOption`](../../doc/models/create-hook-option.md) | Body, Required | - |

## Response Type

**201**: Hook

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Hook`](../../doc/models/hook.md).

## Example Usage

```python
org = 'org6'

body = CreateHookOption(
    config={
        'key0': 'config0'
    },
    mtype=Type.MSTEAMS,
    active=False
)

result = organization_api.org_create_hook(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Get Hook

Get a hook

```python
def org_get_hook(self,
                org,
                id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `id` | `int` | Template, Required | id of the hook to get |

## Response Type

**200**: Hook

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Hook`](../../doc/models/hook.md).

## Example Usage

```python
org = 'org6'

id = 112

result = organization_api.org_get_hook(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Delete Hook

Delete a hook

```python
def org_delete_hook(self,
                   org,
                   id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `id` | `int` | Template, Required | id of the hook to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

id = 112

result = organization_api.org_delete_hook(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Edit Hook

Update a hook

```python
def org_edit_hook(self,
                 org,
                 id,
                 body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `id` | `int` | Template, Required | id of the hook to update |
| `body` | [`EditHookOption`](../../doc/models/edit-hook-option.md) | Body, Optional | - |

## Response Type

**200**: Hook

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Hook`](../../doc/models/hook.md).

## Example Usage

```python
org = 'org6'

id = 112

result = organization_api.org_edit_hook(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org List Labels

List an organization's labels

```python
def org_list_labels(self,
                   org,
                   page=None,
                   limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: LabelList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Label]`](../../doc/models/label.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_labels(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Create Label

Create a label for an organization

```python
def org_create_label(self,
                    org,
                    body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `body` | [`CreateLabelOption`](../../doc/models/create-label-option.md) | Body, Optional | - |

## Response Type

**201**: Label

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Label`](../../doc/models/label.md).

## Example Usage

```python
org = 'org6'

body = CreateLabelOption(
    color='#00aabb',
    name='name6',
    exclusive=False,
    is_archived=False
)

result = organization_api.org_create_label(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Org Get Label

Get a single label

```python
def org_get_label(self,
                 org,
                 id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `id` | `int` | Template, Required | id of the label to get |

## Response Type

**200**: Label

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Label`](../../doc/models/label.md).

## Example Usage

```python
org = 'org6'

id = 112

result = organization_api.org_get_label(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Delete Label

Delete a label

```python
def org_delete_label(self,
                    org,
                    id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `id` | `int` | Template, Required | id of the label to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

id = 112

result = organization_api.org_delete_label(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Edit Label

Update a label

```python
def org_edit_label(self,
                  org,
                  id,
                  body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `id` | `int` | Template, Required | id of the label to edit |
| `body` | [`EditLabelOption`](../../doc/models/edit-label-option.md) | Body, Optional | - |

## Response Type

**200**: Label

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Label`](../../doc/models/label.md).

## Example Usage

```python
org = 'org6'

id = 112

body = EditLabelOption(
    color='#00aabb',
    exclusive=False,
    is_archived=False
)

result = organization_api.org_edit_label(
    org,
    id,
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
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Org List Members

List an organization's members

```python
def org_list_members(self,
                    org,
                    page=None,
                    limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_members(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Is Member

Check if a user is a member of an organization

```python
def org_is_member(self,
                 org,
                 username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user to check for an organization membership |

## Response Type

**204**: user is a member

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.org_is_member(
    org,
    username
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | user is not a member | `ApiException` |


# Org Delete Member

Remove a member from an organization

```python
def org_delete_member(self,
                     org,
                     username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user to remove from the organization |

## Response Type

**204**: member removed

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.org_delete_member(
    org,
    username
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


# Org List Public Members

List an organization's public members

```python
def org_list_public_members(self,
                           org,
                           page=None,
                           limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_public_members(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Is Public Member

Check if a user is a public member of an organization

```python
def org_is_public_member(self,
                        org,
                        username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user to check for a public organization membership |

## Response Type

**204**: user is a public member

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.org_is_public_member(
    org,
    username
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | user is not a public member | `ApiException` |


# Org Publicize Member

Publicize a user's membership

```python
def org_publicize_member(self,
                        org,
                        username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user whose membership is to be publicized |

## Response Type

**204**: membership publicized

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.org_publicize_member(
    org,
    username
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


# Org Conceal Member

Conceal a user's membership

```python
def org_conceal_member(self,
                      org,
                      username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `username` | `str` | Template, Required | username of the user whose membership is to be concealed |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

username = 'username0'

result = organization_api.org_conceal_member(
    org,
    username
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


# Rename Org

Rename an organization

```python
def rename_org(self,
              org,
              body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | existing org name |
| `body` | [`RenameOrgOption`](../../doc/models/rename-org-option.md) | Body, Required | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

body = RenameOrgOption(
    new_name='new_name2'
)

result = organization_api.rename_org(
    org,
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


# Org List Repos

List an organization's repos

```python
def org_list_repos(self,
                  org,
                  page=None,
                  limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_repos(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Create Org Repo

Create a repository in an organization

```python
def create_org_repo(self,
                   org,
                   body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of organization |
| `body` | [`CreateRepoOption`](../../doc/models/create-repo-option.md) | Body, Optional | - |

## Response Type

**201**: Repository

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Repository`](../../doc/models/repository.md).

## Example Usage

```python
org = 'org6'

result = organization_api.create_org_repo(org)

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


# Org Delete Repos

Delete all repositories in an organization

```python
def org_delete_repos(self,
                    org)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
org = 'org6'

result = organization_api.org_delete_repos(org)

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


# Org List Teams

List an organization's teams

```python
def org_list_teams(self,
                  org,
                  page=None,
                  limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: TeamList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Team]`](../../doc/models/team.md).

## Example Usage

```python
org = 'org6'

result = organization_api.org_list_teams(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Create Team

Create a team

```python
def org_create_team(self,
                   org,
                   body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `body` | [`CreateTeamOption`](../../doc/models/create-team-option.md) | Body, Optional | - |

## Response Type

**201**: Team

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Team`](../../doc/models/team.md).

## Example Usage

```python
org = 'org6'

body = CreateTeamOption(
    name='name6',
    units=[
        'repo.actions',
        'repo.code',
        'repo.issues',
        'repo.ext_issues',
        'repo.wiki',
        'repo.ext_wiki',
        'repo.pulls',
        'repo.releases',
        'repo.projects',
        'repo.ext_wiki'
    ]
)

result = organization_api.org_create_team(
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Team Search

Search for teams within an organization

```python
def team_search(self,
               org,
               q=None,
               include_desc=None,
               page=None,
               limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `org` | `str` | Template, Required | name of the organization |
| `q` | `str` | Query, Optional | keywords to search |
| `include_desc` | `bool` | Query, Optional | include search within team description (defaults to true) |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: SearchResults of a successful search

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`TeamSearchResponse`](../../doc/models/team-search-response.md).

## Example Usage

```python
org = 'org6'

result = organization_api.team_search(org)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Get Team

Get a team

```python
def org_get_team(self,
                id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team to get |

## Response Type

**200**: Team

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Team`](../../doc/models/team.md).

## Example Usage

```python
id = 112

result = organization_api.org_get_team(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Delete Team

Delete a team

```python
def org_delete_team(self,
                   id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team to delete |

## Response Type

**204**: team deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

result = organization_api.org_delete_team(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Edit Team

Edit a team

```python
def org_edit_team(self,
                 id,
                 body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team to edit |
| `body` | [`EditTeamOption`](../../doc/models/edit-team-option.md) | Body, Optional | - |

## Response Type

**200**: Team

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Team`](../../doc/models/team.md).

## Example Usage

```python
id = 112

body = EditTeamOption(
    name='name6',
    units=[
        'repo.code',
        'repo.issues',
        'repo.ext_issues',
        'repo.wiki',
        'repo.pulls',
        'repo.releases',
        'repo.projects',
        'repo.ext_wiki'
    ],
    units_map={
        'repo.code': 'read',
        'repo.ext_issues': 'none',
        'repo.ext_wiki': 'none',
        'repo.issues': 'write',
        'repo.projects': 'none',
        'repo.pulls': 'owner',
        'repo.releases': 'none',
        'repo.wiki': 'admin'
    }
)

result = organization_api.org_edit_team(
    id,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org List Team Activity Feeds

List a team's activity feeds

```python
def org_list_team_activity_feeds(self,
                                id,
                                date=None,
                                page=None,
                                limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `date` | `date` | Query, Optional | the date of the activities to be found |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: ActivityFeedsList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Activity]`](../../doc/models/activity.md).

## Example Usage

```python
id = 112

result = organization_api.org_list_team_activity_feeds(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org List Team Members

List a team's members

```python
def org_list_team_members(self,
                         id,
                         page=None,
                         limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
id = 112

result = organization_api.org_list_team_members(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org List Team Member

List a particular member of team

```python
def org_list_team_member(self,
                        id,
                        username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `username` | `str` | Template, Required | username of the user whose data is to be listed |

## Response Type

**200**: User

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`User`](../../doc/models/user.md).

## Example Usage

```python
id = 112

username = 'username0'

result = organization_api.org_list_team_member(
    id,
    username
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


# Org Add Team Member

Add a team member

```python
def org_add_team_member(self,
                       id,
                       username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `username` | `str` | Template, Required | username of the user to add to a team |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

username = 'username0'

result = organization_api.org_add_team_member(
    id,
    username
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


# Org Remove Team Member

Remove a team member

```python
def org_remove_team_member(self,
                          id,
                          username)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `username` | `str` | Template, Required | username of the user to remove from a team |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

username = 'username0'

result = organization_api.org_remove_team_member(
    id,
    username
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


# Org List Team Repos

List a team's repos

```python
def org_list_team_repos(self,
                       id,
                       page=None,
                       limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: RepositoryList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Repository]`](../../doc/models/repository.md).

## Example Usage

```python
id = 112

result = organization_api.org_list_team_repos(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org List Team Repo

List a particular repo of team

```python
def org_list_team_repo(self,
                      id,
                      org,
                      repo)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `org` | `str` | Template, Required | organization that owns the repo to list |
| `repo` | `str` | Template, Required | name of the repo to list |

## Response Type

**200**: Repository

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Repository`](../../doc/models/repository.md).

## Example Usage

```python
id = 112

org = 'org6'

repo = 'repo4'

result = organization_api.org_list_team_repo(
    id,
    org,
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Add Team Repository

Add a repository to a team

```python
def org_add_team_repository(self,
                           id,
                           org,
                           repo)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `org` | `str` | Template, Required | organization that owns the repo to add |
| `repo` | `str` | Template, Required | name of the repo to add |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

org = 'org6'

repo = 'repo4'

result = organization_api.org_add_team_repository(
    id,
    org,
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


# Org Remove Team Repository

This does not delete the repository, it only removes the repository from the team.

```python
def org_remove_team_repository(self,
                              id,
                              org,
                              repo)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | id of the team |
| `org` | `str` | Template, Required | organization that owns the repo to remove |
| `repo` | `str` | Template, Required | name of the repo to remove |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 112

org = 'org6'

repo = 'repo4'

result = organization_api.org_remove_team_repository(
    id,
    org,
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


# Org List Current User Orgs

List the current user's organizations

```python
def org_list_current_user_orgs(self,
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
result = organization_api.org_list_current_user_orgs()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org List User Orgs

List a user's organizations

```python
def org_list_user_orgs(self,
                      username,
                      page=None,
                      limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose organizations are to be listed |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: OrganizationList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Organization]`](../../doc/models/organization.md).

## Example Usage

```python
username = 'username0'

result = organization_api.org_list_user_orgs(username)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Org Get User Permissions

Get user permissions in organization

```python
def org_get_user_permissions(self,
                            username,
                            org)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `str` | Template, Required | username of the user whose permissions are to be obtained |
| `org` | `str` | Template, Required | name of the organization |

## Response Type

**200**: OrganizationPermissions

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`OrganizationPermissions`](../../doc/models/organization-permissions.md).

## Example Usage

```python
username = 'username0'

org = 'org6'

result = organization_api.org_get_user_permissions(
    username,
    org
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

