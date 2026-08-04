
# Package File

PackageFile represents a package file

*This model accepts additional fields of type Any.*

## Structure

`PackageFile`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Optional | The unique identifier of the package file |
| `md_5` | `str` | Optional | The MD5 hash of the package file |
| `name` | `str` | Optional | The name of the package file |
| `sha_1` | `str` | Optional | The SHA1 hash of the package file |
| `sha_256` | `str` | Optional | The SHA256 hash of the package file |
| `sha_512` | `str` | Optional | The SHA512 hash of the package file |
| `size` | `int` | Optional | The size of the package file in bytes |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.package_file import PackageFile

package_file = PackageFile(
    id=124,
    md_5='md50',
    name='name0',
    sha_1='sha16',
    sha_256='sha2562',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

