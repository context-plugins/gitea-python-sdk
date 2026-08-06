
# Pull Request Minimal

PullRequestMinimal is the minimal information about a pull request, as
returned in the `pull_requests` field of a workflow run.

*This model accepts additional fields of type Any.*

## Structure

`PullRequestMinimal`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `base` | [`PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest`](../../doc/models/pull-request-minimal-head-is-a-minimal-description-of-one-side-of-a-pull-request.md) | Optional | - |
| `head` | [`PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest`](../../doc/models/pull-request-minimal-head-is-a-minimal-description-of-one-side-of-a-pull-request.md) | Optional | - |
| `id` | `int` | Optional | - |
| `number` | `int` | Optional | - |
| `url` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.pull_request_minimal import PullRequestMinimal
from gitea.models.pull_request_minimal_head_is_a_minimal_description_of_one_side_of_a_pull_request import PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest
from gitea.models.pull_request_minimal_head_repo_is_a_minimal_description_of_the_repository_on_one_side_of_a_pull_request import PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest

pull_request_minimal = PullRequestMinimal(
    base=PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest(
        ref='ref6',
        repo=PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest(
            id=94,
            name='name4',
            url='url8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        sha='sha2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    head=PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest(
        ref='ref8',
        repo=PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest(
            id=94,
            name='name4',
            url='url8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        sha='sha4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    id=76,
    number=62,
    url='url4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

