
# File Delete Response

FileDeleteResponse contains information about a repo's file that was deleted

*This model accepts additional fields of type Any.*

## Structure

`FileDeleteResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commit` | [`FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile`](../../doc/models/file-commit-response-contains-information-generated-from-a-git-commit-for-a-repo-s-file.md) | Optional | - |
| `content` | `Any` | Optional | Content is always null for delete operations |
| `verification` | [`PayloadCommitVerification`](../../doc/models/payload-commit-verification.md) | Optional | PayloadCommitVerification represents the GPG verification of a commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from giteaapi.models.file_commit_response_contains_information_generated_from_a_git_commit_for_a_repo_s_file import FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile
from giteaapi.models.file_delete_response import FileDeleteResponse
from giteaapi.models.payload_commit_verification import PayloadCommitVerification
from giteaapi.models.payload_user import PayloadUser

file_delete_response = FileDeleteResponse(
    commit=FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile(
        author=CommitUserContainsInformationOfAUserInTheContextOfACommit(
            date='date6',
            email='email6',
            name='name0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        committer=CommitUserContainsInformationOfAUserInTheContextOfACommit(
            date='date0',
            email='email2',
            name='name4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        html_url='html_url2',
        message='message2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    content=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    verification=PayloadCommitVerification(
        payload='payload0',
        reason='reason0',
        signature='signature2',
        signer=PayloadUser(
            email='email6',
            name='name0',
            username='username0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        verified=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

