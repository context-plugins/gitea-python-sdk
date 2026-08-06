
# Pull Request Minimal Head Is a Minimal Description of One Side of a Pull Request

*This model accepts additional fields of type Any.*

## Structure

`PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ref` | `str` | Optional | - |
| `repo` | [`PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest`](../../doc/models/pull-request-minimal-head-repo-is-a-minimal-description-of-the-repository-on-one-side-of-a-pull-request.md) | Optional | - |
| `sha` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.pull_request_minimal_head_is_a_minimal_description_of_one_side_of_a_pull_request import PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest
from gitea.models.pull_request_minimal_head_repo_is_a_minimal_description_of_the_repository_on_one_side_of_a_pull_request import PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest

pull_request_minimal_head_is_a_minimal_description_of_one_side_of_a_pull_request = PullRequestMinimalHeadIsAMinimalDescriptionOfOneSideOfAPullRequest(
    ref='ref0',
    repo=PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest(
        id=94,
        name='name4',
        url='url8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    sha='sha6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

