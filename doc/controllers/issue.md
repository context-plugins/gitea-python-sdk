# Issue

```python
issue_api = client.issue
```

## Class Name

`IssueApi`

## Methods

* [Issue Search Issues](../../doc/controllers/issue.md#issue-search-issues)
* [Issue List Issues](../../doc/controllers/issue.md#issue-list-issues)
* [Issue Create Issue](../../doc/controllers/issue.md#issue-create-issue)
* [Issue Get Repo Comments](../../doc/controllers/issue.md#issue-get-repo-comments)
* [Issue Get Comment](../../doc/controllers/issue.md#issue-get-comment)
* [Issue Delete Comment](../../doc/controllers/issue.md#issue-delete-comment)
* [Issue Edit Comment](../../doc/controllers/issue.md#issue-edit-comment)
* [Issue List Issue Comment Attachments](../../doc/controllers/issue.md#issue-list-issue-comment-attachments)
* [Issue Create Issue Comment Attachment](../../doc/controllers/issue.md#issue-create-issue-comment-attachment)
* [Issue Get Issue Comment Attachment](../../doc/controllers/issue.md#issue-get-issue-comment-attachment)
* [Issue Delete Issue Comment Attachment](../../doc/controllers/issue.md#issue-delete-issue-comment-attachment)
* [Issue Edit Issue Comment Attachment](../../doc/controllers/issue.md#issue-edit-issue-comment-attachment)
* [Issue Get Comment Reactions](../../doc/controllers/issue.md#issue-get-comment-reactions)
* [Issue Post Comment Reaction](../../doc/controllers/issue.md#issue-post-comment-reaction)
* [Issue Delete Comment Reaction](../../doc/controllers/issue.md#issue-delete-comment-reaction)
* [Issue Get Issue](../../doc/controllers/issue.md#issue-get-issue)
* [Issue Delete](../../doc/controllers/issue.md#issue-delete)
* [Issue Edit Issue](../../doc/controllers/issue.md#issue-edit-issue)
* [Issue List Issue Attachments](../../doc/controllers/issue.md#issue-list-issue-attachments)
* [Issue Create Issue Attachment](../../doc/controllers/issue.md#issue-create-issue-attachment)
* [Issue Get Issue Attachment](../../doc/controllers/issue.md#issue-get-issue-attachment)
* [Issue Delete Issue Attachment](../../doc/controllers/issue.md#issue-delete-issue-attachment)
* [Issue Edit Issue Attachment](../../doc/controllers/issue.md#issue-edit-issue-attachment)
* [Issue Add Assignees](../../doc/controllers/issue.md#issue-add-assignees)
* [Issue Remove Assignees](../../doc/controllers/issue.md#issue-remove-assignees)
* [Issue Check Assignee](../../doc/controllers/issue.md#issue-check-assignee)
* [Issue List Blocks](../../doc/controllers/issue.md#issue-list-blocks)
* [Issue Create Issue Blocking](../../doc/controllers/issue.md#issue-create-issue-blocking)
* [Issue Remove Issue Blocking](../../doc/controllers/issue.md#issue-remove-issue-blocking)
* [Issue Get Comments](../../doc/controllers/issue.md#issue-get-comments)
* [Issue Create Comment](../../doc/controllers/issue.md#issue-create-comment)
* [Issue Delete Comment Deprecated](../../doc/controllers/issue.md#issue-delete-comment-deprecated)
* [Issue Edit Comment Deprecated](../../doc/controllers/issue.md#issue-edit-comment-deprecated)
* [Issue Edit Issue Deadline](../../doc/controllers/issue.md#issue-edit-issue-deadline)
* [Issue List Issue Dependencies](../../doc/controllers/issue.md#issue-list-issue-dependencies)
* [Issue Create Issue Dependencies](../../doc/controllers/issue.md#issue-create-issue-dependencies)
* [Issue Remove Issue Dependencies](../../doc/controllers/issue.md#issue-remove-issue-dependencies)
* [Issue Get Labels](../../doc/controllers/issue.md#issue-get-labels)
* [Issue Replace Labels](../../doc/controllers/issue.md#issue-replace-labels)
* [Issue Add Label](../../doc/controllers/issue.md#issue-add-label)
* [Issue Clear Labels](../../doc/controllers/issue.md#issue-clear-labels)
* [Issue Remove Label](../../doc/controllers/issue.md#issue-remove-label)
* [Issue Lock Issue](../../doc/controllers/issue.md#issue-lock-issue)
* [Issue Unlock Issue](../../doc/controllers/issue.md#issue-unlock-issue)
* [Pin Issue](../../doc/controllers/issue.md#pin-issue)
* [Unpin Issue](../../doc/controllers/issue.md#unpin-issue)
* [Move Issue Pin](../../doc/controllers/issue.md#move-issue-pin)
* [Issue Get Issue Reactions](../../doc/controllers/issue.md#issue-get-issue-reactions)
* [Issue Post Issue Reaction](../../doc/controllers/issue.md#issue-post-issue-reaction)
* [Issue Delete Issue Reaction](../../doc/controllers/issue.md#issue-delete-issue-reaction)
* [Issue Delete Stop Watch](../../doc/controllers/issue.md#issue-delete-stop-watch)
* [Issue Start Stop Watch](../../doc/controllers/issue.md#issue-start-stop-watch)
* [Issue Stop Stop Watch](../../doc/controllers/issue.md#issue-stop-stop-watch)
* [Issue Subscriptions](../../doc/controllers/issue.md#issue-subscriptions)
* [Issue Check Subscription](../../doc/controllers/issue.md#issue-check-subscription)
* [Issue Add Subscription](../../doc/controllers/issue.md#issue-add-subscription)
* [Issue Delete Subscription](../../doc/controllers/issue.md#issue-delete-subscription)
* [Issue Get Comments and Timeline](../../doc/controllers/issue.md#issue-get-comments-and-timeline)
* [Issue Tracked Times](../../doc/controllers/issue.md#issue-tracked-times)
* [Issue Add Time](../../doc/controllers/issue.md#issue-add-time)
* [Issue Reset Time](../../doc/controllers/issue.md#issue-reset-time)
* [Issue Delete Time](../../doc/controllers/issue.md#issue-delete-time)
* [Issue List Labels](../../doc/controllers/issue.md#issue-list-labels)
* [Issue Create Label](../../doc/controllers/issue.md#issue-create-label)
* [Issue Get Label](../../doc/controllers/issue.md#issue-get-label)
* [Issue Delete Label](../../doc/controllers/issue.md#issue-delete-label)
* [Issue Edit Label](../../doc/controllers/issue.md#issue-edit-label)
* [Issue Get Milestones List](../../doc/controllers/issue.md#issue-get-milestones-list)
* [Issue Create Milestone](../../doc/controllers/issue.md#issue-create-milestone)
* [Issue Get Milestone](../../doc/controllers/issue.md#issue-get-milestone)
* [Issue Delete Milestone](../../doc/controllers/issue.md#issue-delete-milestone)
* [Issue Edit Milestone](../../doc/controllers/issue.md#issue-edit-milestone)


# Issue Search Issues

Search for issues across the repositories that the user has access to

```python
def issue_search_issues(self,
                       state="open",
                       labels=None,
                       milestones=None,
                       q=None,
                       mtype=None,
                       since=None,
                       before=None,
                       assigned=False,
                       created=False,
                       mentioned=False,
                       review_requested=False,
                       reviewed=False,
                       owner=None,
                       created_by=None,
                       team=None,
                       page=1,
                       limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`State9`](../../doc/models/state-9.md) | Query, Optional | State of the issue<br><br>**Default**: `"open"` |
| `labels` | `str` | Query, Optional | Comma-separated list of label names. Fetch only issues that have any of these labels. Non existent labels are discarded. |
| `milestones` | `str` | Query, Optional | Comma-separated list of milestone names. Fetch only issues that have any of these milestones. Non existent milestones are discarded. |
| `q` | `str` | Query, Optional | Search string |
| `mtype` | [`Type5`](../../doc/models/type-5.md) | Query, Optional | Filter by issue type |
| `since` | `datetime` | Query, Optional | Only show issues updated after the given time (RFC 3339 format) |
| `before` | `datetime` | Query, Optional | Only show issues updated before the given time (RFC 3339 format) |
| `assigned` | `bool` | Query, Optional | Filter issues or pulls assigned to the authenticated user<br><br>**Default**: `False` |
| `created` | `bool` | Query, Optional | Filter issues or pulls created by the authenticated user<br><br>**Default**: `False` |
| `mentioned` | `bool` | Query, Optional | Filter issues or pulls mentioning the authenticated user<br><br>**Default**: `False` |
| `review_requested` | `bool` | Query, Optional | Filter pull requests where the authenticated user's review was requested<br><br>**Default**: `False` |
| `reviewed` | `bool` | Query, Optional | Filter pull requests reviewed by the authenticated user<br><br>**Default**: `False` |
| `owner` | `str` | Query, Optional | Filter by repository owner |
| `created_by` | `str` | Query, Optional | Only show items which were created by the given user |
| `team` | `str` | Query, Optional | Filter by team (requires organization owner parameter) |
| `page` | `int` | Query, Optional | Page number of results to return (1-based)<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `limit` | `int` | Query, Optional | Number of items per page<br><br>**Constraints**: `>= 0` |

## Response Type

**200**: IssueList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Issue]`](../../doc/models/issue.md).

## Example Usage

```python
state = State9.OPEN

assigned = False

created = False

mentioned = False

review_requested = False

reviewed = False

page = 1

result = issue_api.issue_search_issues(
    state=state,
    assigned=assigned,
    created=created,
    mentioned=mentioned,
    review_requested=review_requested,
    reviewed=reviewed,
    page=page
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Issue List Issues

List a repository's issues

```python
def issue_list_issues(self,
                     owner,
                     repo,
                     state=None,
                     labels=None,
                     q=None,
                     mtype=None,
                     milestones=None,
                     since=None,
                     before=None,
                     created_by=None,
                     assigned_by=None,
                     mentioned_by=None,
                     page=None,
                     limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `state` | [`State9`](../../doc/models/state-9.md) | Query, Optional | whether issue is open or closed |
| `labels` | `str` | Query, Optional | comma separated list of label names. Fetch only issues that have any of this label names. Non existent labels are discarded. |
| `q` | `str` | Query, Optional | search string |
| `mtype` | [`Type5`](../../doc/models/type-5.md) | Query, Optional | filter by type (issues / pulls) if set |
| `milestones` | `str` | Query, Optional | comma separated list of milestone names or ids. It uses names and fall back to ids. Fetch only issues that have any of this milestones. Non existent milestones are discarded |
| `since` | `datetime` | Query, Optional | Only show items updated after the given time. This is a timestamp in RFC 3339 format |
| `before` | `datetime` | Query, Optional | Only show items updated before the given time. This is a timestamp in RFC 3339 format |
| `created_by` | `str` | Query, Optional | Only show items which were created by the given user |
| `assigned_by` | `str` | Query, Optional | Only show items for which the given user is assigned |
| `mentioned_by` | `str` | Query, Optional | Only show items in which the given user was mentioned |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: IssueList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Issue]`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = issue_api.issue_list_issues(
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Issue Create Issue

Create an issue. If using deadline only the date will be taken into account, and time of day ignored.

```python
def issue_create_issue(self,
                      owner,
                      repo,
                      body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `body` | [`CreateIssueOption`](../../doc/models/create-issue-option.md) | Body, Optional | - |

## Response Type

**201**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = issue_api.issue_create_issue(
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
| 412 | APIError is error format response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Get Repo Comments

List all comments in a repository

```python
def issue_get_repo_comments(self,
                           owner,
                           repo,
                           since=None,
                           before=None,
                           page=None,
                           limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `since` | `datetime` | Query, Optional | if provided, only comments updated since the provided time are returned. |
| `before` | `datetime` | Query, Optional | if provided, only comments updated before the provided time are returned. |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: CommentList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Comment]`](../../doc/models/comment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = issue_api.issue_get_repo_comments(
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Issue Get Comment

Get a comment

```python
def issue_get_comment(self,
                     owner,
                     repo,
                     id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment |

## Response Type

**200**: Comment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Comment`](../../doc/models/comment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_get_comment(
    owner,
    repo,
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


# Issue Delete Comment

Delete a comment

```python
def issue_delete_comment(self,
                        owner,
                        repo,
                        id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of comment to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_delete_comment(
    owner,
    repo,
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


# Issue Edit Comment

Edit a comment

```python
def issue_edit_comment(self,
                      owner,
                      repo,
                      id,
                      body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment to edit |
| `body` | [`EditIssueCommentOption`](../../doc/models/edit-issue-comment-option.md) | Body, Optional | - |

## Response Type

**200**: Comment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Comment`](../../doc/models/comment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_edit_comment(
    owner,
    repo,
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
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue List Issue Comment Attachments

List comment's attachments

```python
def issue_list_issue_comment_attachments(self,
                                        owner,
                                        repo,
                                        id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment |

## Response Type

**200**: AttachmentList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Attachment]`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_list_issue_comment_attachments(
    owner,
    repo,
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
| 404 | APIError is error format response | `ApiException` |


# Issue Create Issue Comment Attachment

Create a comment attachment

```python
def issue_create_issue_comment_attachment(self,
                                         owner,
                                         repo,
                                         id,
                                         attachment,
                                         name=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment |
| `attachment` | `typing.BinaryIO` | Form, Required | attachment to upload |
| `name` | `str` | Query, Optional | name of the attachment |

## Response Type

**201**: Attachment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Attachment`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

attachment = FileWrapper(Path('dummy_file').open('rb'), 'optional-content-type')

result = issue_api.issue_create_issue_comment_attachment(
    owner,
    repo,
    id,
    attachment
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
| 404 | APIError is error format response | `ApiException` |
| 413 | APIError is error format response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Get Issue Comment Attachment

Get a comment attachment

```python
def issue_get_issue_comment_attachment(self,
                                      owner,
                                      repo,
                                      id,
                                      attachment_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment |
| `attachment_id` | `int` | Template, Required | id of the attachment to get |

## Response Type

**200**: Attachment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Attachment`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

attachment_id = 242

result = issue_api.issue_get_issue_comment_attachment(
    owner,
    repo,
    id,
    attachment_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APIError is error format response | `ApiException` |


# Issue Delete Issue Comment Attachment

Delete a comment attachment

```python
def issue_delete_issue_comment_attachment(self,
                                         owner,
                                         repo,
                                         id,
                                         attachment_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment |
| `attachment_id` | `int` | Template, Required | id of the attachment to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

attachment_id = 242

result = issue_api.issue_delete_issue_comment_attachment(
    owner,
    repo,
    id,
    attachment_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APIError is error format response | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Edit Issue Comment Attachment

Edit a comment attachment

```python
def issue_edit_issue_comment_attachment(self,
                                       owner,
                                       repo,
                                       id,
                                       attachment_id,
                                       body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment |
| `attachment_id` | `int` | Template, Required | id of the attachment to edit |
| `body` | [`EditAttachmentOptions`](../../doc/models/edit-attachment-options.md) | Body, Optional | - |

## Response Type

**201**: Attachment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Attachment`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

attachment_id = 242

result = issue_api.issue_edit_issue_comment_attachment(
    owner,
    repo,
    id,
    attachment_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APIError is error format response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Get Comment Reactions

Get a list of reactions from a comment of an issue

```python
def issue_get_comment_reactions(self,
                               owner,
                               repo,
                               id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment to edit |

## Response Type

**200**: ReactionList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Reaction]`](../../doc/models/reaction.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_get_comment_reactions(
    owner,
    repo,
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


# Issue Post Comment Reaction

Add a reaction to a comment of an issue

```python
def issue_post_comment_reaction(self,
                               owner,
                               repo,
                               id,
                               content=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment to edit |
| `content` | [`EditReactionOption`](../../doc/models/edit-reaction-option.md) | Body, Optional | - |

## Response Type

**200**: Reaction

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Reaction`](../../doc/models/reaction.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_post_comment_reaction(
    owner,
    repo,
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


# Issue Delete Comment Reaction

Remove a reaction from a comment of an issue

```python
def issue_delete_comment_reaction(self,
                                 owner,
                                 repo,
                                 id,
                                 content=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the comment to edit |
| `content` | [`EditReactionOption`](../../doc/models/edit-reaction-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_delete_comment_reaction(
    owner,
    repo,
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


# Issue Get Issue

Get an issue

```python
def issue_get_issue(self,
                   owner,
                   repo,
                   index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue to get |

## Response Type

**200**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_get_issue(
    owner,
    repo,
    index
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


# Issue Delete

Delete an issue

```python
def issue_delete(self,
                owner,
                repo,
                index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of issue to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_delete(
    owner,
    repo,
    index
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


# Issue Edit Issue

Pass `content_version` to enable optimistic locking on body edits.
If the version doesn't match the current value, the request fails with 409 Conflict.

```python
def issue_edit_issue(self,
                    owner,
                    repo,
                    index,
                    body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue to edit |
| `body` | [`EditIssueOption`](../../doc/models/edit-issue-option.md) | Body, Optional | - |

## Response Type

**201**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_edit_issue(
    owner,
    repo,
    index
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
| 412 | APIError is error format response | `ApiException` |


# Issue List Issue Attachments

List issue's attachments

```python
def issue_list_issue_attachments(self,
                                owner,
                                repo,
                                index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |

## Response Type

**200**: AttachmentList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Attachment]`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_list_issue_attachments(
    owner,
    repo,
    index
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APIError is error format response | `ApiException` |


# Issue Create Issue Attachment

Create an issue attachment

```python
def issue_create_issue_attachment(self,
                                 owner,
                                 repo,
                                 index,
                                 attachment,
                                 name=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `attachment` | `typing.BinaryIO` | Form, Required | attachment to upload |
| `name` | `str` | Query, Optional | name of the attachment |

## Response Type

**201**: Attachment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Attachment`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

attachment = FileWrapper(Path('dummy_file').open('rb'), 'optional-content-type')

result = issue_api.issue_create_issue_attachment(
    owner,
    repo,
    index,
    attachment
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
| 404 | APIError is error format response | `ApiException` |
| 413 | APIError is error format response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Get Issue Attachment

Get an issue attachment

```python
def issue_get_issue_attachment(self,
                              owner,
                              repo,
                              index,
                              attachment_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `attachment_id` | `int` | Template, Required | id of the attachment to get |

## Response Type

**200**: Attachment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Attachment`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

attachment_id = 242

result = issue_api.issue_get_issue_attachment(
    owner,
    repo,
    index,
    attachment_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APIError is error format response | `ApiException` |


# Issue Delete Issue Attachment

Delete an issue attachment

```python
def issue_delete_issue_attachment(self,
                                 owner,
                                 repo,
                                 index,
                                 attachment_id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `attachment_id` | `int` | Template, Required | id of the attachment to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

attachment_id = 242

result = issue_api.issue_delete_issue_attachment(
    owner,
    repo,
    index,
    attachment_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APIError is error format response | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Edit Issue Attachment

Edit an issue attachment

```python
def issue_edit_issue_attachment(self,
                               owner,
                               repo,
                               index,
                               attachment_id,
                               body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `attachment_id` | `int` | Template, Required | id of the attachment to edit |
| `body` | [`EditAttachmentOptions`](../../doc/models/edit-attachment-options.md) | Body, Optional | - |

## Response Type

**201**: Attachment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Attachment`](../../doc/models/attachment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

attachment_id = 242

result = issue_api.issue_edit_issue_attachment(
    owner,
    repo,
    index,
    attachment_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | APIError is error format response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Add Assignees

Add assignees to an issue

```python
def issue_add_assignees(self,
                       owner,
                       repo,
                       index,
                       body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `body` | [`IssueAssigneesOption`](../../doc/models/issue-assignees-option.md) | Body, Required | - |

## Response Type

**201**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

body = IssueAssigneesOption()

result = issue_api.issue_add_assignees(
    owner,
    repo,
    index,
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
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Issue Remove Assignees

Remove assignees from an issue

```python
def issue_remove_assignees(self,
                          owner,
                          repo,
                          index,
                          body)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `body` | [`IssueAssigneesOption`](../../doc/models/issue-assignees-option.md) | Body, Required | - |

## Response Type

**200**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

body = IssueAssigneesOption()

result = issue_api.issue_remove_assignees(
    owner,
    repo,
    index,
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
| 404 | APINotFound is a not found empty response | `ApiException` |
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Issue Check Assignee

Check if a user can be assigned to an issue

```python
def issue_check_assignee(self,
                        owner,
                        repo,
                        index,
                        assignee)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `assignee` | `str` | Template, Required | username of the user to check for being an assignee |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

assignee = 'assignee8'

result = issue_api.issue_check_assignee(
    owner,
    repo,
    index,
    assignee
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


# Issue List Blocks

List issues that are blocked by this issue

```python
def issue_list_blocks(self,
                     owner,
                     repo,
                     index,
                     page=None,
                     limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `str` | Template, Required | index of the issue |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: IssueList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Issue]`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 'index4'

result = issue_api.issue_list_blocks(
    owner,
    repo,
    index
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


# Issue Create Issue Blocking

Block the issue given in the body by the issue in path

```python
def issue_create_issue_blocking(self,
                               owner,
                               repo,
                               index,
                               body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `str` | Template, Required | index of the issue |
| `body` | [`IssueMeta`](../../doc/models/issue-meta.md) | Body, Optional | - |

## Response Type

**201**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 'index4'

result = issue_api.issue_create_issue_blocking(
    owner,
    repo,
    index
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | the issue does not exist | `ApiException` |


# Issue Remove Issue Blocking

Unblock the issue given in the body by the issue in path

```python
def issue_remove_issue_blocking(self,
                               owner,
                               repo,
                               index,
                               body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `str` | Template, Required | index of the issue |
| `body` | [`IssueMeta`](../../doc/models/issue-meta.md) | Body, Optional | - |

## Response Type

**200**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 'index4'

result = issue_api.issue_remove_issue_blocking(
    owner,
    repo,
    index
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


# Issue Get Comments

List all comments on an issue

```python
def issue_get_comments(self,
                      owner,
                      repo,
                      index,
                      since=None,
                      before=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `since` | `datetime` | Query, Optional | if provided, only comments updated since the specified time are returned. |
| `before` | `datetime` | Query, Optional | if provided, only comments updated before the provided time are returned. |

## Response Type

**200**: CommentList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Comment]`](../../doc/models/comment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_get_comments(
    owner,
    repo,
    index
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


# Issue Create Comment

Add a comment to an issue

```python
def issue_create_comment(self,
                        owner,
                        repo,
                        index,
                        body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `body` | [`CreateIssueCommentOption`](../../doc/models/create-issue-comment-option.md) | Body, Optional | - |

## Response Type

**201**: Comment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Comment`](../../doc/models/comment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_create_comment(
    owner,
    repo,
    index
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
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Delete Comment Deprecated

**This endpoint is deprecated.**

Delete a comment

```python
def issue_delete_comment_deprecated(self,
                                   owner,
                                   repo,
                                   index,
                                   id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | this parameter is ignored |
| `id` | `int` | Template, Required | id of comment to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

id = 112

result = issue_api.issue_delete_comment_deprecated(
    owner,
    repo,
    index,
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


# Issue Edit Comment Deprecated

**This endpoint is deprecated.**

Edit a comment

```python
def issue_edit_comment_deprecated(self,
                                 owner,
                                 repo,
                                 index,
                                 id,
                                 body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | this parameter is ignored |
| `id` | `int` | Template, Required | id of the comment to edit |
| `body` | [`EditIssueCommentOption`](../../doc/models/edit-issue-comment-option.md) | Body, Optional | - |

## Response Type

**200**: Comment

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Comment`](../../doc/models/comment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

id = 112

result = issue_api.issue_edit_comment_deprecated(
    owner,
    repo,
    index,
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


# Issue Edit Issue Deadline

Set an issue deadline. If set to null, the deadline is deleted. If using deadline only the date will be taken into account, and time of day ignored.

```python
def issue_edit_issue_deadline(self,
                             owner,
                             repo,
                             index,
                             body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue to create or update a deadline on |
| `body` | [`EditDeadlineOption`](../../doc/models/edit-deadline-option.md) | Body, Optional | - |

## Response Type

**201**: IssueDeadline

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`IssueDeadline`](../../doc/models/issue-deadline.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_edit_issue_deadline(
    owner,
    repo,
    index
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


# Issue List Issue Dependencies

List an issue's dependencies, i.e all issues that block this issue.

```python
def issue_list_issue_dependencies(self,
                                 owner,
                                 repo,
                                 index,
                                 page=None,
                                 limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `str` | Template, Required | index of the issue |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: IssueList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Issue]`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 'index4'

result = issue_api.issue_list_issue_dependencies(
    owner,
    repo,
    index
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


# Issue Create Issue Dependencies

Make the issue in the url depend on the issue in the form.

```python
def issue_create_issue_dependencies(self,
                                   owner,
                                   repo,
                                   index,
                                   body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `str` | Template, Required | index of the issue |
| `body` | [`IssueMeta`](../../doc/models/issue-meta.md) | Body, Optional | - |

## Response Type

**201**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 'index4'

result = issue_api.issue_create_issue_dependencies(
    owner,
    repo,
    index
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | the issue does not exist | `ApiException` |
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Remove Issue Dependencies

Remove an issue dependency

```python
def issue_remove_issue_dependencies(self,
                                   owner,
                                   repo,
                                   index,
                                   body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `str` | Template, Required | index of the issue |
| `body` | [`IssueMeta`](../../doc/models/issue-meta.md) | Body, Optional | - |

## Response Type

**200**: Issue

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Issue`](../../doc/models/issue.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 'index4'

result = issue_api.issue_remove_issue_dependencies(
    owner,
    repo,
    index
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
| 423 | APIRepoArchivedError is an error that is raised when an archived repo should be modified | `ApiException` |


# Issue Get Labels

Get an issue's labels

```python
def issue_get_labels(self,
                    owner,
                    repo,
                    index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |

## Response Type

**200**: LabelList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Label]`](../../doc/models/label.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_get_labels(
    owner,
    repo,
    index
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


# Issue Replace Labels

Replace an issue's labels

```python
def issue_replace_labels(self,
                        owner,
                        repo,
                        index,
                        body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `body` | [`IssueLabelsOption`](../../doc/models/issue-labels-option.md) | Body, Optional | - |

## Response Type

**200**: LabelList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Label]`](../../doc/models/label.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_replace_labels(
    owner,
    repo,
    index
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


# Issue Add Label

Add a label to an issue

```python
def issue_add_label(self,
                   owner,
                   repo,
                   index,
                   body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `body` | [`IssueLabelsOption`](../../doc/models/issue-labels-option.md) | Body, Optional | - |

## Response Type

**200**: LabelList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Label]`](../../doc/models/label.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_add_label(
    owner,
    repo,
    index
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


# Issue Clear Labels

Remove all labels from an issue

```python
def issue_clear_labels(self,
                      owner,
                      repo,
                      index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_clear_labels(
    owner,
    repo,
    index
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


# Issue Remove Label

Remove a label from an issue

```python
def issue_remove_label(self,
                      owner,
                      repo,
                      index,
                      id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `id` | `int` | Template, Required | id of the label to remove |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

id = 112

result = issue_api.issue_remove_label(
    owner,
    repo,
    index,
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
| 422 | APIValidationError is error format response related to input validation | `ApiException` |


# Issue Lock Issue

Lock an issue

```python
def issue_lock_issue(self,
                    owner,
                    repo,
                    index,
                    body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `body` | [`LockIssueOption`](../../doc/models/lock-issue-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_lock_issue(
    owner,
    repo,
    index
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


# Issue Unlock Issue

Unlock an issue

```python
def issue_unlock_issue(self,
                      owner,
                      repo,
                      index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_unlock_issue(
    owner,
    repo,
    index
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


# Pin Issue

Pin an Issue

```python
def pin_issue(self,
             owner,
             repo,
             index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of issue to pin |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.pin_issue(
    owner,
    repo,
    index
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


# Unpin Issue

Unpin an Issue

```python
def unpin_issue(self,
               owner,
               repo,
               index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of issue to unpin |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.unpin_issue(
    owner,
    repo,
    index
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


# Move Issue Pin

Moves the Pin to the given Position

```python
def move_issue_pin(self,
                  owner,
                  repo,
                  index,
                  position)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of issue |
| `position` | `int` | Template, Required | the new position |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

position = 142

result = issue_api.move_issue_pin(
    owner,
    repo,
    index,
    position
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


# Issue Get Issue Reactions

Get a list reactions of an issue

```python
def issue_get_issue_reactions(self,
                             owner,
                             repo,
                             index,
                             page=None,
                             limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: ReactionList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Reaction]`](../../doc/models/reaction.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_get_issue_reactions(
    owner,
    repo,
    index
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


# Issue Post Issue Reaction

Add a reaction to an issue

```python
def issue_post_issue_reaction(self,
                             owner,
                             repo,
                             index,
                             content=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `content` | [`EditReactionOption`](../../doc/models/edit-reaction-option.md) | Body, Optional | - |

## Response Type

**200**: Reaction

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Reaction`](../../doc/models/reaction.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_post_issue_reaction(
    owner,
    repo,
    index
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


# Issue Delete Issue Reaction

Remove a reaction from an issue

```python
def issue_delete_issue_reaction(self,
                               owner,
                               repo,
                               index,
                               content=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `content` | [`EditReactionOption`](../../doc/models/edit-reaction-option.md) | Body, Optional | - |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_delete_issue_reaction(
    owner,
    repo,
    index
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


# Issue Delete Stop Watch

Delete an issue's existing stopwatch.

```python
def issue_delete_stop_watch(self,
                           owner,
                           repo,
                           index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue to stop the stopwatch on |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_delete_stop_watch(
    owner,
    repo,
    index
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | Not repo writer, user does not have rights to toggle stopwatch | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 409 | Cannot cancel a non-existent stopwatch | `ApiException` |


# Issue Start Stop Watch

Start stopwatch on an issue.

```python
def issue_start_stop_watch(self,
                          owner,
                          repo,
                          index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue to create the stopwatch on |

## Response Type

**201**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_start_stop_watch(
    owner,
    repo,
    index
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | Not repo writer, user does not have rights to toggle stopwatch | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 409 | Cannot start a stopwatch again if it already exists | `ApiException` |


# Issue Stop Stop Watch

Stop an issue's existing stopwatch.

```python
def issue_stop_stop_watch(self,
                         owner,
                         repo,
                         index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue to stop the stopwatch on |

## Response Type

**201**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_stop_stop_watch(
    owner,
    repo,
    index
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 403 | Not repo writer, user does not have rights to toggle stopwatch | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |
| 409 | Cannot stop a non-existent stopwatch | `ApiException` |


# Issue Subscriptions

Get users who subscribed on an issue.

```python
def issue_subscriptions(self,
                       owner,
                       repo,
                       index,
                       page=None,
                       limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: UserList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[User]`](../../doc/models/user.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_subscriptions(
    owner,
    repo,
    index
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


# Issue Check Subscription

Check if user is subscribed to an issue

```python
def issue_check_subscription(self,
                            owner,
                            repo,
                            index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |

## Response Type

**200**: WatchInfo

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`WatchInfo`](../../doc/models/watch-info.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_check_subscription(
    owner,
    repo,
    index
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


# Issue Add Subscription

Subscribe user to issue

```python
def issue_add_subscription(self,
                          owner,
                          repo,
                          index,
                          user)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `user` | `str` | Template, Required | username of the user to subscribe the issue to |

## Response Type

**200**: Already subscribed

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

user = 'user0'

result = issue_api.issue_add_subscription(
    owner,
    repo,
    index,
    user
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


# Issue Delete Subscription

Unsubscribe user from issue

```python
def issue_delete_subscription(self,
                             owner,
                             repo,
                             index,
                             user)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `user` | `str` | Template, Required | username of the user to unsubscribe from an issue |

## Response Type

**200**: Already unsubscribed

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

user = 'user0'

result = issue_api.issue_delete_subscription(
    owner,
    repo,
    index,
    user
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


# Issue Get Comments and Timeline

List all comments and events on an issue

```python
def issue_get_comments_and_timeline(self,
                                   owner,
                                   repo,
                                   index,
                                   since=None,
                                   page=None,
                                   limit=None,
                                   before=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `since` | `datetime` | Query, Optional | if provided, only comments updated since the specified time are returned. |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |
| `before` | `datetime` | Query, Optional | if provided, only comments updated before the provided time are returned. |

## Response Type

**200**: TimelineList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[TimelineComment]`](../../doc/models/timeline-comment.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_get_comments_and_timeline(
    owner,
    repo,
    index
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


# Issue Tracked Times

List an issue's tracked times

```python
def issue_tracked_times(self,
                       owner,
                       repo,
                       index,
                       user=None,
                       since=None,
                       before=None,
                       page=None,
                       limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `user` | `str` | Query, Optional | optional filter by user (available for issue managers) |
| `since` | `datetime` | Query, Optional | Only show times updated after the given time. This is a timestamp in RFC 3339 format |
| `before` | `datetime` | Query, Optional | Only show times updated before the given time. This is a timestamp in RFC 3339 format |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: TrackedTimeList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[TrackedTime]`](../../doc/models/tracked-time.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_tracked_times(
    owner,
    repo,
    index
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


# Issue Add Time

Add tracked time to a issue

```python
def issue_add_time(self,
                  owner,
                  repo,
                  index,
                  body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `body` | [`AddTimeOption`](../../doc/models/add-time-option.md) | Body, Optional | - |

## Response Type

**200**: TrackedTime

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`TrackedTime`](../../doc/models/tracked-time.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_add_time(
    owner,
    repo,
    index
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


# Issue Reset Time

Reset a tracked time of an issue

```python
def issue_reset_time(self,
                    owner,
                    repo,
                    index)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue to add tracked time to |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

result = issue_api.issue_reset_time(
    owner,
    repo,
    index
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


# Issue Delete Time

Delete specific tracked time

```python
def issue_delete_time(self,
                     owner,
                     repo,
                     index,
                     id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `index` | `int` | Template, Required | index of the issue |
| `id` | `int` | Template, Required | id of time to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

index = 44

id = 112

result = issue_api.issue_delete_time(
    owner,
    repo,
    index,
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
| 400 | APIError is error format response | `ApiException` |
| 403 | APIForbiddenError is a forbidden error response | `ApiException` |
| 404 | APINotFound is a not found empty response | `ApiException` |


# Issue List Labels

Get all of a repository's labels

```python
def issue_list_labels(self,
                     owner,
                     repo,
                     page=None,
                     limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: LabelList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Label]`](../../doc/models/label.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = issue_api.issue_list_labels(
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Issue Create Label

Create a label

```python
def issue_create_label(self,
                      owner,
                      repo,
                      body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `body` | [`CreateLabelOption`](../../doc/models/create-label-option.md) | Body, Optional | - |

## Response Type

**201**: Label

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Label`](../../doc/models/label.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

body = CreateLabelOption(
    color='#00aabb',
    name='name6',
    exclusive=False,
    is_archived=False
)

result = issue_api.issue_create_label(
    owner,
    repo,
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


# Issue Get Label

Get a single label

```python
def issue_get_label(self,
                   owner,
                   repo,
                   id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the label to get |

## Response Type

**200**: Label

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Label`](../../doc/models/label.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_get_label(
    owner,
    repo,
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


# Issue Delete Label

Delete a label

```python
def issue_delete_label(self,
                      owner,
                      repo,
                      id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the label to delete |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

result = issue_api.issue_delete_label(
    owner,
    repo,
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


# Issue Edit Label

Update a label

```python
def issue_edit_label(self,
                    owner,
                    repo,
                    id,
                    body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `int` | Template, Required | id of the label to edit |
| `body` | [`EditLabelOption`](../../doc/models/edit-label-option.md) | Body, Optional | - |

## Response Type

**200**: Label

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Label`](../../doc/models/label.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 112

body = EditLabelOption(
    color='#00aabb',
    exclusive=False,
    is_archived=False
)

result = issue_api.issue_edit_label(
    owner,
    repo,
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


# Issue Get Milestones List

Get all of a repository's opened milestones

```python
def issue_get_milestones_list(self,
                             owner,
                             repo,
                             state=None,
                             name=None,
                             page=None,
                             limit=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `state` | `str` | Query, Optional | Milestone state, Recognized values are open, closed and all. Defaults to "open" |
| `name` | `str` | Query, Optional | filter by milestone name |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: MilestoneList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[Milestone]`](../../doc/models/milestone.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = issue_api.issue_get_milestones_list(
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Issue Create Milestone

Create a milestone

```python
def issue_create_milestone(self,
                          owner,
                          repo,
                          body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `body` | [`CreateMilestoneOption`](../../doc/models/create-milestone-option.md) | Body, Optional | - |

## Response Type

**201**: Milestone

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Milestone`](../../doc/models/milestone.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = issue_api.issue_create_milestone(
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
| 404 | APINotFound is a not found empty response | `ApiException` |


# Issue Get Milestone

Get a milestone

```python
def issue_get_milestone(self,
                       owner,
                       repo,
                       id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `str` | Template, Required | the milestone to get, identified by ID and if not available by name |

## Response Type

**200**: Milestone

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Milestone`](../../doc/models/milestone.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 'id0'

result = issue_api.issue_get_milestone(
    owner,
    repo,
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


# Issue Delete Milestone

Delete a milestone

```python
def issue_delete_milestone(self,
                          owner,
                          repo,
                          id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `str` | Template, Required | the milestone to delete, identified by ID and if not available by name |

## Response Type

**204**: APIEmpty is an empty response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 'id0'

result = issue_api.issue_delete_milestone(
    owner,
    repo,
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


# Issue Edit Milestone

Update a milestone

```python
def issue_edit_milestone(self,
                        owner,
                        repo,
                        id,
                        body=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `id` | `str` | Template, Required | the milestone to edit, identified by ID and if not available by name |
| `body` | [`EditMilestoneOption`](../../doc/models/edit-milestone-option.md) | Body, Optional | - |

## Response Type

**200**: Milestone

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`Milestone`](../../doc/models/milestone.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

id = 'id0'

result = issue_api.issue_edit_milestone(
    owner,
    repo,
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

