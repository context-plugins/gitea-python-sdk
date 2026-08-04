
# Wiki Commit

WikiCommit page commit/revision

*This model accepts additional fields of type Any.*

## Structure

`WikiCommit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `author` | [`CommitUserContainsInformationOfAUserInTheContextOfACommit`](../../doc/models/commit-user-contains-information-of-a-user-in-the-context-of-a-commit.md) | Optional | - |
| `commiter` | [`CommitUserContainsInformationOfAUserInTheContextOfACommit`](../../doc/models/commit-user-contains-information-of-a-user-in-the-context-of-a-commit.md) | Optional | - |
| `message` | `str` | Optional | The commit message |
| `sha` | `str` | Optional | The commit SHA hash |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from giteaapi.models.wiki_commit import WikiCommit

wiki_commit = WikiCommit(
    author=CommitUserContainsInformationOfAUserInTheContextOfACommit(
        date='date6',
        email='email6',
        name='name0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    commiter=CommitUserContainsInformationOfAUserInTheContextOfACommit(
        date='date2',
        email='email4',
        name='name2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    message='message6',
    sha='sha2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

