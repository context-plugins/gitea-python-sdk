
# Update File Options

UpdateFileOptions options for updating or creating a file
Note: `author` and `committer` are optional (if only one is given, it will be used for the other, otherwise the authenticated user will be used)

*This model accepts additional fields of type Any.*

## Structure

`UpdateFileOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `author` | [`Identity`](../../doc/models/identity.md) | Optional | Identity for a person's identity like an author or committer |
| `branch` | `str` | Optional | branch (optional) is the base branch for the changes. If not supplied, the default branch is used |
| `committer` | [`Identity`](../../doc/models/identity.md) | Optional | Identity for a person's identity like an author or committer |
| `content` | `str` | Required | content must be base64 encoded |
| `dates` | [`CommitDateOptions`](../../doc/models/commit-date-options.md) | Optional | CommitDateOptions store dates for GIT_AUTHOR_DATE and GIT_COMMITTER_DATE |
| `force_push` | `bool` | Optional | force_push (optional) will do a force-push if the new branch already exists |
| `from_path` | `str` | Optional | from_path (optional) is the path of the original file which will be moved/renamed to the path in the URL |
| `message` | `str` | Optional | message (optional) is the commit message of the changes. If not supplied, a default message will be used |
| `new_branch` | `str` | Optional | new_branch (optional) will make a new branch from base branch for the changes. If not supplied, the changes will be committed to the base branch |
| `sha` | `str` | Optional | the blob ID (SHA) for the file that already exists to update, or leave it empty to create a new file |
| `signoff` | `bool` | Optional | Add a Signed-off-by trailer by the committer at the end of the commit log message. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.commit_date_options import CommitDateOptions
from gitea.models.identity import Identity
from gitea.models.update_file_options import UpdateFileOptions

update_file_options = UpdateFileOptions(
    content='content2',
    author=Identity(
        email='email6',
        name='name0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    branch='branch4',
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

