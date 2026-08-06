
# Annotated Tag

AnnotatedTag represents an annotated tag

*This model accepts additional fields of type Any.*

## Structure

`AnnotatedTag`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | The message associated with the annotated tag |
| `object` | [`AnnotatedTagObject`](../../doc/models/annotated-tag-object.md) | Optional | AnnotatedTagObject contains meta information of the tag object |
| `sha` | `str` | Optional | The SHA hash of the annotated tag |
| `tag` | `str` | Optional | The name of the annotated tag |
| `tagger` | [`CommitUserContainsInformationOfAUserInTheContextOfACommit`](../../doc/models/commit-user-contains-information-of-a-user-in-the-context-of-a-commit.md) | Optional | - |
| `url` | `str` | Optional | The URL to access the annotated tag |
| `verification` | [`PayloadCommitVerification`](../../doc/models/payload-commit-verification.md) | Optional | PayloadCommitVerification represents the GPG verification of a commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.annotated_tag import AnnotatedTag
from gitea.models.annotated_tag_object import AnnotatedTagObject
from gitea.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit

annotated_tag = AnnotatedTag(
    message='message4',
    object=AnnotatedTagObject(
        sha='sha8',
        mtype='type8',
        url='url6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    sha='sha0',
    tag='tag8',
    tagger=CommitUserContainsInformationOfAUserInTheContextOfACommit(
        date='date6',
        email='email6',
        name='name0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

