
# Commit Contains Information Generated from a Git Commit

*This model accepts additional fields of type Any.*

## Structure

`CommitContainsInformationGeneratedFromAGitCommit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `author` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `commit` | [`RepoCommitContainsInformationOfACommitInTheContextOfARepository`](../../doc/models/repo-commit-contains-information-of-a-commit-in-the-context-of-a-repository.md) | Optional | - |
| `committer` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `created` | `datetime` | Optional | - |
| `files` | [`List[CommitAffectedFiles]`](../../doc/models/commit-affected-files.md) | Optional | Files contains information about files affected by the commit |
| `html_url` | `str` | Optional | HTMLURL is the web URL for viewing the commit |
| `parents` | [`List[CommitMetaContainsMetaInformationOfACommitInTermsOfApi]`](../../doc/models/commit-meta-contains-meta-information-of-a-commit-in-terms-of-api.md) | Optional | Parents contains the parent commit information |
| `sha` | `str` | Optional | SHA is the commit SHA hash |
| `stats` | [`CommitStats`](../../doc/models/commit-stats.md) | Optional | CommitStats is statistics for a RepoCommit |
| `url` | `str` | Optional | URL is the API URL for the commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.commit_affected_files import CommitAffectedFiles
from giteaapi.models.commit_contains_information_generated_from_a_git_commit import CommitContainsInformationGeneratedFromAGitCommit
from giteaapi.models.commit_meta_contains_meta_information_of_a_commit_in_terms_of_api import CommitMetaContainsMetaInformationOfACommitInTermsOfApi
from giteaapi.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from giteaapi.models.repo_commit_contains_information_of_a_commit_in_the_context_of_a_repository import RepoCommitContainsInformationOfACommitInTheContextOfARepository
from giteaapi.models.user import User

commit_contains_information_generated_from_a_git_commit = CommitContainsInformationGeneratedFromAGitCommit(
    author=User(
        active=False,
        avatar_url='avatar_url6',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description0',
        email='email6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    commit=RepoCommitContainsInformationOfACommitInTheContextOfARepository(
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
        message='message2',
        tree=CommitMetaContainsMetaInformationOfACommitInTermsOfApi(
            created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            sha='sha4',
            url='url2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        url='url2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    committer=User(
        active=False,
        avatar_url='avatar_url0',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description4',
        email='email2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    files=[
        CommitAffectedFiles(
            filename='filename6',
            status='status6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

