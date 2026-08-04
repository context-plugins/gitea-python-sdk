
# File Response

FileResponse contains information about a repo's file

*This model accepts additional fields of type Any.*

## Structure

`FileResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commit` | [`FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile`](../../doc/models/file-commit-response-contains-information-generated-from-a-git-commit-for-a-repo-s-file.md) | Optional | - |
| `content` | [`ContentsResponse`](../../doc/models/contents-response.md) | Optional | ContentsResponse contains information about a repo's entry's (dir, file, symlink, submodule) metadata and content |
| `verification` | [`PayloadCommitVerification`](../../doc/models/payload-commit-verification.md) | Optional | PayloadCommitVerification represents the GPG verification of a commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from giteaapi.models.contents_response import ContentsResponse
from giteaapi.models.file_commit_response_contains_information_generated_from_a_git_commit_for_a_repo_s_file import FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile
from giteaapi.models.file_links_response import FileLinksResponse
from giteaapi.models.file_response import FileResponse
from giteaapi.models.payload_commit_verification import PayloadCommitVerification
from giteaapi.models.payload_user import PayloadUser

file_response = FileResponse(
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
    content=ContentsResponse(
        links=FileLinksResponse(
            git='git6',
            html='html6',
            mself='self4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        content='content8',
        download_url='download_url6',
        encoding='encoding4',
        git_url='git_url4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
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

