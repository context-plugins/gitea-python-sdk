
# Action Workflow Run

ActionWorkflowRun represents a WorkflowRun

*This model accepts additional fields of type Any.*

## Structure

`ActionWorkflowRun`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actor` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `completed_at` | `datetime` | Optional | - |
| `conclusion` | `str` | Optional | - |
| `display_title` | `str` | Optional | - |
| `event` | `str` | Optional | - |
| `head_branch` | `str` | Optional | - |
| `head_repository` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `head_sha` | `str` | Optional | - |
| `html_url` | `str` | Optional | - |
| `id` | `int` | Optional | - |
| `path` | `str` | Optional | - |
| `previous_attempt_url` | `str` | Optional | PreviousAttemptURL is the API URL of the previous attempt of this run, e.g. ".../actions/runs/{run_id}/attempts/{attempt-1}".<br>It is set only when the current attempt is > 1 (i.e. a rerun). For the first attempt, or for legacy runs that pre-date ActionRunAttempt, it is null. |
| `pull_requests` | [`List[PullRequestMinimal]`](../../doc/models/pull-request-minimal.md) | Optional | - |
| `repository` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `repository_id` | `int` | Optional | - |
| `run_attempt` | `int` | Optional | RunAttempt is 1-based for runs created after ActionRunAttempt was introduced.<br>A value of 0 is a legacy-only sentinel for runs created before attempts existed<br>and indicates no corresponding /attempts/{n} resource is available. |
| `run_number` | `int` | Optional | - |
| `started_at` | `datetime` | Optional | - |
| `status` | `str` | Optional | - |
| `trigger_actor` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `url` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.action_workflow_run import ActionWorkflowRun
from giteaapi.models.user import User

action_workflow_run = ActionWorkflowRun(
    actor=User(
        active=False,
        avatar_url='avatar_url6',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description0',
        email='email6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    conclusion='conclusion8',
    display_title='display_title4',
    event='event4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

