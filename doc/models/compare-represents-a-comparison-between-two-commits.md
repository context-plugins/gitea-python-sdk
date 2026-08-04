
# Compare Represents a Comparison between Two Commits

*This model accepts additional fields of type Any.*

## Structure

`CompareRepresentsAComparisonBetweenTwoCommits`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commits` | [`List[CommitContainsInformationGeneratedFromAGitCommit]`](../../doc/models/commit-contains-information-generated-from-a-git-commit.md) | Optional | - |
| `total_commits` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.commit_affected_files import CommitAffectedFiles
from giteaapi.models.commit_contains_information_generated_from_a_git_commit import CommitContainsInformationGeneratedFromAGitCommit
from giteaapi.models.commit_meta_contains_meta_information_of_a_commit_in_terms_of_api import CommitMetaContainsMetaInformationOfACommitInTermsOfApi
from giteaapi.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from giteaapi.models.compare_represents_a_comparison_between_two_commits import CompareRepresentsAComparisonBetweenTwoCommits
from giteaapi.models.repo_commit_contains_information_of_a_commit_in_the_context_of_a_repository import RepoCommitContainsInformationOfACommitInTheContextOfARepository
from giteaapi.models.user import User

compare_represents_a_comparison_between_two_commits = CompareRepresentsAComparisonBetweenTwoCommits(
    commits=[
        CommitContainsInformationGeneratedFromAGitCommit(
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
                ),
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
    ],
    total_commits=186,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

