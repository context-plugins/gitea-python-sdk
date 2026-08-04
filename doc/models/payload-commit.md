
# Payload Commit

PayloadCommit represents a commit

*This model accepts additional fields of type Any.*

## Structure

`PayloadCommit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added` | `List[str]` | Optional | List of files added in this commit |
| `author` | [`PayloadUser`](../../doc/models/payload-user.md) | Optional | PayloadUser represents the author or committer of a commit |
| `committer` | [`PayloadUser`](../../doc/models/payload-user.md) | Optional | PayloadUser represents the author or committer of a commit |
| `id` | `str` | Optional | sha1 hash of the commit |
| `message` | `str` | Optional | The commit message |
| `modified` | `List[str]` | Optional | List of files modified in this commit |
| `removed` | `List[str]` | Optional | List of files removed in this commit |
| `timestamp` | `datetime` | Optional | - |
| `url` | `str` | Optional | The URL to view this commit |
| `verification` | [`PayloadCommitVerification`](../../doc/models/payload-commit-verification.md) | Optional | PayloadCommitVerification represents the GPG verification of a commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.payload_commit import PayloadCommit
from giteaapi.models.payload_user import PayloadUser

payload_commit = PayloadCommit(
    added=[
        'added0',
        'added1'
    ],
    author=PayloadUser(
        email='email6',
        name='name0',
        username='username0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    committer=PayloadUser(
        email='email2',
        name='name4',
        username='username6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    id='id2',
    message='message2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

