
# Commit User Contains Information of a User in the Context of a Commit

*This model accepts additional fields of type Any.*

## Structure

`CommitUserContainsInformationOfAUserInTheContextOfACommit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `date` | `str` | Optional | Date is the commit date in string format |
| `email` | `str` | Optional | - |
| `name` | `str` | Optional | Name is the person's name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit

commit_user_contains_information_of_a_user_in_the_context_of_a_commit = CommitUserContainsInformationOfAUserInTheContextOfACommit(
    date='date6',
    email='email6',
    name='name0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

