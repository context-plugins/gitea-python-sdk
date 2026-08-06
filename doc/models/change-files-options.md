
# Change Files Options

ChangeFilesOptions options for creating, updating or deleting multiple files
Note: `author` and `committer` are optional (if only one is given, it will be used for the other, otherwise the authenticated user will be used)

*This model accepts additional fields of type Any.*

## Structure

`ChangeFilesOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `author` | [`Identity`](../../doc/models/identity.md) | Optional | Identity for a person's identity like an author or committer |
| `branch` | `str` | Optional | branch (optional) is the base branch for the changes. If not supplied, the default branch is used |
| `committer` | [`Identity`](../../doc/models/identity.md) | Optional | Identity for a person's identity like an author or committer |
| `dates` | [`CommitDateOptions`](../../doc/models/commit-date-options.md) | Optional | CommitDateOptions store dates for GIT_AUTHOR_DATE and GIT_COMMITTER_DATE |
| `files` | [`List[ChangeFileOperation]`](../../doc/models/change-file-operation.md) | Required | list of file operations |
| `force_push` | `bool` | Optional | force_push (optional) will do a force-push if the new branch already exists |
| `message` | `str` | Optional | message (optional) is the commit message of the changes. If not supplied, a default message will be used |
| `new_branch` | `str` | Optional | new_branch (optional) will make a new branch from base branch for the changes. If not supplied, the changes will be committed to the base branch |
| `signoff` | `bool` | Optional | Add a Signed-off-by trailer by the committer at the end of the commit log message. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.change_file_operation import ChangeFileOperation
from gitea.models.change_files_options import ChangeFilesOptions
from gitea.models.commit_date_options import CommitDateOptions
from gitea.models.identity import Identity
from gitea.models.operation import Operation

change_files_options = ChangeFilesOptions(
    files=[
        ChangeFileOperation(
            operation=Operation.RENAME,
            path='path8',
            content='content8',
            from_path='from_path8',
            sha='sha0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    author=Identity(
        email='email6',
        name='name0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    branch='branch2',
    committer=Identity(
        email='email2',
        name='name4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    dates=CommitDateOptions(
        author=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        committer=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    force_push=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

