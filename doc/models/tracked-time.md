
# Tracked Time

TrackedTime worked time for an issue / pr

*This model accepts additional fields of type Any.*

## Structure

`TrackedTime`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `datetime` | Optional | - |
| `id` | `int` | Optional | ID is the unique identifier for the tracked time entry |
| `issue` | [`Issue`](../../doc/models/issue.md) | Optional | Issue represents an issue in a repository |
| `issue_id` | `int` | Optional | deprecated (only for backwards compatibility) |
| `time` | `int` | Optional | Time in seconds |
| `user_id` | `int` | Optional | deprecated (only for backwards compatibility) |
| `user_name` | `str` | Optional | username of the user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.attachment import Attachment
from giteaapi.models.issue import Issue
from giteaapi.models.tracked_time import TrackedTime
from giteaapi.models.user import User

tracked_time = TrackedTime(
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id=210,
    issue=Issue(
        assets=[
            Attachment(
                browser_download_url='browser_download_url6',
                created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                download_count=224,
                id=12,
                name='name8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Attachment(
                browser_download_url='browser_download_url6',
                created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                download_count=224,
                id=12,
                name='name8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        assignee=User(
            active=False,
            avatar_url='avatar_url4',
            created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            description='description2',
            email='email8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        assignees=[
            User(
                active=False,
                avatar_url='avatar_url0',
                created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                description='description6',
                email='email2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            User(
                active=False,
                avatar_url='avatar_url0',
                created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                description='description6',
                email='email2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        body='body0',
        closed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    issue_id=134,
    time=144,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

