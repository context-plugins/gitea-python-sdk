
# Edit Release Option

EditReleaseOption options when editing a release

*This model accepts additional fields of type Any.*

## Structure

`EditReleaseOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | The new release notes or description |
| `draft` | `bool` | Optional | Whether to change the draft status |
| `name` | `str` | Optional | The new display title of the release |
| `prerelease` | `bool` | Optional | Whether to change the prerelease status |
| `tag_name` | `str` | Optional | The new name of the git tag |
| `target_commitish` | `str` | Optional | The new target commitish for the release |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_release_option import EditReleaseOption

edit_release_option = EditReleaseOption(
    body='body4',
    draft=False,
    name='name8',
    prerelease=False,
    tag_name='tag_name8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

