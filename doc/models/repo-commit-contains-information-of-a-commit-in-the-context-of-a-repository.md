
# Repo Commit Contains Information of a Commit in the Context of a Repository

*This model accepts additional fields of type Any.*

## Structure

`RepoCommitContainsInformationOfACommitInTheContextOfARepository`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `author` | [`CommitUserContainsInformationOfAUserInTheContextOfACommit`](../../doc/models/commit-user-contains-information-of-a-user-in-the-context-of-a-commit.md) | Optional | - |
| `committer` | [`CommitUserContainsInformationOfAUserInTheContextOfACommit`](../../doc/models/commit-user-contains-information-of-a-user-in-the-context-of-a-commit.md) | Optional | - |
| `message` | `str` | Optional | Message is the commit message |
| `tree` | [`CommitMetaContainsMetaInformationOfACommitInTermsOfApi`](../../doc/models/commit-meta-contains-meta-information-of-a-commit-in-terms-of-api.md) | Optional | - |
| `url` | `str` | Optional | URL is the API URL for the commit |
| `verification` | [`PayloadCommitVerification`](../../doc/models/payload-commit-verification.md) | Optional | PayloadCommitVerification represents the GPG verification of a commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.commit_meta_contains_meta_information_of_a_commit_in_terms_of_api import CommitMetaContainsMetaInformationOfACommitInTermsOfApi
from giteaapi.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from giteaapi.models.repo_commit_contains_information_of_a_commit_in_the_context_of_a_repository import RepoCommitContainsInformationOfACommitInTheContextOfARepository

repo_commit_contains_information_of_a_commit_in_the_context_of_a_repository = RepoCommitContainsInformationOfACommitInTheContextOfARepository(
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
    message='message4',
    tree=CommitMetaContainsMetaInformationOfACommitInTermsOfApi(
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        sha='sha4',
        url='url2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    url='url0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

