
# File Commit Response Contains Information Generated from a Git Commit for a Repo S File

*This model accepts additional fields of type Any.*

## Structure

`FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `author` | [`CommitUserContainsInformationOfAUserInTheContextOfACommit`](../../doc/models/commit-user-contains-information-of-a-user-in-the-context-of-a-commit.md) | Optional | - |
| `committer` | [`CommitUserContainsInformationOfAUserInTheContextOfACommit`](../../doc/models/commit-user-contains-information-of-a-user-in-the-context-of-a-commit.md) | Optional | - |
| `created` | `datetime` | Optional | - |
| `html_url` | `str` | Optional | HTMLURL is the web URL for viewing this commit |
| `message` | `str` | Optional | Message is the commit message |
| `parents` | [`List[CommitMetaContainsMetaInformationOfACommitInTermsOfApi]`](../../doc/models/commit-meta-contains-meta-information-of-a-commit-in-terms-of-api.md) | Optional | Parents contains parent commit metadata |
| `sha` | `str` | Optional | SHA is the commit SHA hash |
| `tree` | [`CommitMetaContainsMetaInformationOfACommitInTermsOfApi`](../../doc/models/commit-meta-contains-meta-information-of-a-commit-in-terms-of-api.md) | Optional | - |
| `url` | `str` | Optional | URL is the API URL for the commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from gitea.models.file_commit_response_contains_information_generated_from_a_git_commit_for_a_repo_s_file import FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile

file_commit_response_contains_information_generated_from_a_git_commit_for_a_repo_s_file = FileCommitResponseContainsInformationGeneratedFromAGitCommitForARepoSFile(
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
)
```

