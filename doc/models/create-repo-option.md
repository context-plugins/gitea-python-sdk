
# Create Repo Option

CreateRepoOption options when creating repository

*This model accepts additional fields of type Any.*

## Structure

`CreateRepoOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_init` | `bool` | Optional | Whether the repository should be auto-initialized? |
| `default_branch` | `str` | Optional | DefaultBranch of the repository (used when initializes and in template) |
| `description` | `str` | Optional | Description of the repository to create |
| `gitignores` | `str` | Optional | Gitignores to use |
| `issue_labels` | `str` | Optional | Label-Set to use |
| `license` | `str` | Optional | License to use |
| `name` | `str` | Required | Name of the repository to create |
| `object_format_name` | [`ObjectFormatName1`](../../doc/models/object-format-name-1.md) | Optional | ObjectFormatName of the underlying git repository, empty string for default (sha1)<br>sha1 ObjectFormatSHA1<br>sha256 ObjectFormatSHA256 |
| `private` | `bool` | Optional | Whether the repository is private |
| `readme` | `str` | Optional | Readme of the repository to create |
| `template` | `bool` | Optional | Whether the repository is template |
| `trust_model` | [`TrustModel`](../../doc/models/trust-model.md) | Optional | TrustModel of the repository |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_repo_option import CreateRepoOption

create_repo_option = CreateRepoOption(
    name='name4',
    auto_init=False,
    default_branch='default_branch2',
    description='description6',
    gitignores='gitignores0',
    issue_labels='issue_labels2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

