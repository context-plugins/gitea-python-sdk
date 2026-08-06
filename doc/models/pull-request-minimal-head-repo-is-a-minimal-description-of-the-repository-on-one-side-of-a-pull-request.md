
# Pull Request Minimal Head Repo Is a Minimal Description of the Repository on One Side of a Pull Request

*This model accepts additional fields of type Any.*

## Structure

`PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Optional | - |
| `name` | `str` | Optional | - |
| `url` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.pull_request_minimal_head_repo_is_a_minimal_description_of_the_repository_on_one_side_of_a_pull_request import PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest

pull_request_minimal_head_repo_is_a_minimal_description_of_the_repository_on_one_side_of_a_pull_request = PullRequestMinimalHeadRepoIsAMinimalDescriptionOfTheRepositoryOnOneSideOfAPullRequest(
    id=230,
    name='name8',
    url='url2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

