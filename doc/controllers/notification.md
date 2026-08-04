# Notification

```python
notification_api = client.notification
```

## Class Name

`NotificationApi`

## Methods

* [Notify Get List](../../doc/controllers/notification.md#notify-get-list)
* [Notify Read List](../../doc/controllers/notification.md#notify-read-list)
* [Notify New Available](../../doc/controllers/notification.md#notify-new-available)
* [Notify Get Thread](../../doc/controllers/notification.md#notify-get-thread)
* [Notify Read Thread](../../doc/controllers/notification.md#notify-read-thread)
* [Notify Get Repo List](../../doc/controllers/notification.md#notify-get-repo-list)
* [Notify Read Repo List](../../doc/controllers/notification.md#notify-read-repo-list)


# Notify Get List

List users's notification threads

```python
def notify_get_list(self,
                   all=None,
                   status_types=None,
                   subject_type=None,
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
| `all` | `bool` | Query, Optional | If true, show notifications marked as read. Default value is false |
| `status_types` | `List[str]` | Query, Optional | Show notifications with the provided status types. Options are: unread, read and/or pinned. Defaults to unread & pinned. |
| `subject_type` | [`List[SubjectType]`](../../doc/models/subject-type.md) | Query, Optional | filter notifications by subject type |
| `since` | `datetime` | Query, Optional | Only show notifications updated after the given time. This is a timestamp in RFC 3339 format |
| `before` | `datetime` | Query, Optional | Only show notifications updated before the given time. This is a timestamp in RFC 3339 format |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: NotificationThreadList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[NotificationThread]`](../../doc/models/notification-thread.md).

## Example Usage

```python
result = notification_api.notify_get_list()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Notify Read List

Mark notification threads as read, pinned or unread

```python
def notify_read_list(self,
                    last_read_at=None,
                    all=None,
                    status_types=None,
                    to_status=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last_read_at` | `datetime` | Query, Optional | Describes the last point that notifications were checked. Anything updated since this time will not be updated. |
| `all` | `str` | Query, Optional | If true, mark all notifications on this repo. Default value is false |
| `status_types` | `List[str]` | Query, Optional | Mark notifications with the provided status types. Options are: unread, read and/or pinned. Defaults to unread. |
| `to_status` | `str` | Query, Optional | Status to mark notifications as, Defaults to read. |

## Response Type

**205**: NotificationThreadList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[NotificationThread]`](../../doc/models/notification-thread.md).

## Example Usage

```python
result = notification_api.notify_read_list()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Notify New Available

Check if unread notifications exist

```python
def notify_new_available(self)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Response Type

**200**: Number of unread notifications

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`NotificationCount`](../../doc/models/notification-count.md).

## Example Usage

```python
result = notification_api.notify_new_available()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Notify Get Thread

Get notification thread by ID

```python
def notify_get_thread(self,
                     id)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Template, Required | id of notification thread |

## Response Type

**200**: NotificationThread

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`NotificationThread`](../../doc/models/notification-thread.md).

## Example Usage

```python
id = 'id0'

result = notification_api.notify_get_thread(id)

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


# Notify Read Thread

Mark notification thread as read by ID

```python
def notify_read_thread(self,
                      id,
                      to_status="read")
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Template, Required | id of notification thread |
| `to_status` | `str` | Query, Optional | Status to mark notifications as<br><br>**Default**: `"read"` |

## Response Type

**205**: NotificationThread

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`NotificationThread`](../../doc/models/notification-thread.md).

## Example Usage

```python
id = 'id0'

to_status = 'read'

result = notification_api.notify_read_thread(
    id,
    to_status=to_status
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


# Notify Get Repo List

List users's notification threads on a specific repo

```python
def notify_get_repo_list(self,
                        owner,
                        repo,
                        all=None,
                        status_types=None,
                        subject_type=None,
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
| `all` | `bool` | Query, Optional | If true, show notifications marked as read. Default value is false |
| `status_types` | `List[str]` | Query, Optional | Show notifications with the provided status types. Options are: unread, read and/or pinned. Defaults to unread & pinned |
| `subject_type` | [`List[SubjectType]`](../../doc/models/subject-type.md) | Query, Optional | filter notifications by subject type |
| `since` | `datetime` | Query, Optional | Only show notifications updated after the given time. This is a timestamp in RFC 3339 format |
| `before` | `datetime` | Query, Optional | Only show notifications updated before the given time. This is a timestamp in RFC 3339 format |
| `page` | `int` | Query, Optional | page number of results to return (1-based) |
| `limit` | `int` | Query, Optional | page size of results |

## Response Type

**200**: NotificationThreadList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[NotificationThread]`](../../doc/models/notification-thread.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = notification_api.notify_get_repo_list(
    owner,
    repo
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Notify Read Repo List

Mark notification threads as read, pinned or unread on a specific repo

```python
def notify_read_repo_list(self,
                         owner,
                         repo,
                         all=None,
                         status_types=None,
                         to_status=None,
                         last_read_at=None)
```

## Authentication

This endpoint requires [BasicAuth](../../doc/auth/basic-authentication.md) **OR** [Token](../../doc/auth/custom-query-parameter-2.md) **OR** [AccessToken](../../doc/auth/custom-query-parameter.md) **OR** [AuthorizationHeaderToken](../../doc/auth/custom-header-signature.md) **OR** [SudoParam](../../doc/auth/custom-query-parameter-1.md) **OR** [SudoHeader](../../doc/auth/custom-header-signature-1.md) **OR** [TOTPHeader](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `owner` | `str` | Template, Required | owner of the repo |
| `repo` | `str` | Template, Required | name of the repo |
| `all` | `str` | Query, Optional | If true, mark all notifications on this repo. Default value is false |
| `status_types` | `List[str]` | Query, Optional | Mark notifications with the provided status types. Options are: unread, read and/or pinned. Defaults to unread. |
| `to_status` | `str` | Query, Optional | Status to mark notifications as. Defaults to read. |
| `last_read_at` | `datetime` | Query, Optional | Describes the last point that notifications were checked. Anything updated since this time will not be updated. |

## Response Type

**205**: NotificationThreadList

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`List[NotificationThread]`](../../doc/models/notification-thread.md).

## Example Usage

```python
owner = 'owner4'

repo = 'repo4'

result = notification_api.notify_read_repo_list(
    owner,
    repo
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

