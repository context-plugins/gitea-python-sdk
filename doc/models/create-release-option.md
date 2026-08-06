
# Create Release Option

CreateReleaseOption options when creating a release

*This model accepts additional fields of type Any.*

## Structure

`CreateReleaseOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | The release notes or description |
| `draft` | `bool` | Optional | Whether to create the release as a draft |
| `name` | `str` | Optional | The display title of the release |
| `prerelease` | `bool` | Optional | Whether to mark the release as a prerelease |
| `tag_message` | `str` | Optional | The message for the git tag |
| `tag_name` | `str` | Required | - |
| `target_commitish` | `str` | Optional | The target commitish for the release |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_release_option import CreateReleaseOption

create_release_option = CreateReleaseOption(
    tag_name='tag_name2',
    body='body4',
    draft=False,
    name='name8',
    prerelease=False,
    tag_message='tag_message0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

