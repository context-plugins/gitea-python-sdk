
# Commit Meta Contains Meta Information of a Commit in Terms of Api

*This model accepts additional fields of type Any.*

## Structure

`CommitMetaContainsMetaInformationOfACommitInTermsOfApi`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `datetime` | Optional | - |
| `sha` | `str` | Optional | SHA is the commit SHA hash |
| `url` | `str` | Optional | URL is the API URL for the commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.commit_meta_contains_meta_information_of_a_commit_in_terms_of_api import CommitMetaContainsMetaInformationOfACommitInTermsOfApi

commit_meta_contains_meta_information_of_a_commit_in_terms_of_api = CommitMetaContainsMetaInformationOfACommitInTermsOfApi(
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    sha='sha2',
    url='url0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

