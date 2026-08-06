
# Generate Repo Option

GenerateRepoOption options when creating a repository using a template

*This model accepts additional fields of type Any.*

## Structure

`GenerateRepoOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `avatar` | `bool` | Optional | include avatar of the template repo |
| `default_branch` | `str` | Optional | Default branch of the new repository |
| `description` | `str` | Optional | Description of the repository to create |
| `git_content` | `bool` | Optional | include git content of default branch in template repo |
| `git_hooks` | `bool` | Optional | include git hooks in template repo |
| `labels` | `bool` | Optional | include labels in template repo |
| `name` | `str` | Required | - |
| `owner` | `str` | Required | the organization's name or individual user's name who will own the new repository |
| `private` | `bool` | Optional | Whether the repository is private |
| `protected_branch` | `bool` | Optional | include protected branches in template repo |
| `topics` | `bool` | Optional | include topics in template repo |
| `webhooks` | `bool` | Optional | include webhooks in template repo |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.generate_repo_option import GenerateRepoOption

generate_repo_option = GenerateRepoOption(
    name='name4',
    owner='owner8',
    avatar=False,
    default_branch='default_branch2',
    description='description6',
    git_content=False,
    git_hooks=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

