
# Wiki Commit List

WikiCommitList commit/revision list

*This model accepts additional fields of type Any.*

## Structure

`WikiCommitList`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commits` | [`List[WikiCommit]`](../../doc/models/wiki-commit.md) | Optional | The list of wiki commits |
| `count` | `int` | Optional | The total count of commits |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from gitea.models.wiki_commit import WikiCommit
from gitea.models.wiki_commit_list import WikiCommitList

wiki_commit_list = WikiCommitList(
    commits=[
        WikiCommit(
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
            sha='sha0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        WikiCommit(
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
            sha='sha0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        WikiCommit(
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
            sha='sha0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    count=204,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

