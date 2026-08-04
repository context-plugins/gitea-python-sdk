
# Tag

Tag represents a repository tag

*This model accepts additional fields of type Any.*

## Structure

`Tag`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commit` | [`CommitMetaContainsMetaInformationOfACommitInTermsOfApi`](../../doc/models/commit-meta-contains-meta-information-of-a-commit-in-terms-of-api.md) | Optional | - |
| `id` | `str` | Optional | The ID (SHA) of the tag |
| `message` | `str` | Optional | The message associated with the tag |
| `name` | `str` | Optional | The name of the tag |
| `tarball_url` | `str` | Optional | The URL to download the tarball archive |
| `zipball_url` | `str` | Optional | The URL to download the zipball archive |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.commit_meta_contains_meta_information_of_a_commit_in_terms_of_api import CommitMetaContainsMetaInformationOfACommitInTermsOfApi
from giteaapi.models.tag import Tag

tag = Tag(
    commit=CommitMetaContainsMetaInformationOfACommitInTermsOfApi(
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        sha='sha4',
        url='url2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    id='id6',
    message='message6',
    name='name6',
    tarball_url='tarball_url2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

