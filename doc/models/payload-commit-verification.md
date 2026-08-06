
# Payload Commit Verification

PayloadCommitVerification represents the GPG verification of a commit

*This model accepts additional fields of type Any.*

## Structure

`PayloadCommitVerification`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payload` | `str` | Optional | The signed payload content |
| `reason` | `str` | Optional | The reason for the verification status |
| `signature` | `str` | Optional | The GPG signature of the commit |
| `signer` | [`PayloadUser`](../../doc/models/payload-user.md) | Optional | PayloadUser represents the author or committer of a commit |
| `verified` | `bool` | Optional | Whether the commit signature is verified |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.payload_commit_verification import PayloadCommitVerification
from gitea.models.payload_user import PayloadUser

payload_commit_verification = PayloadCommitVerification(
    payload='payload4',
    reason='reason6',
    signature='signature6',
    signer=PayloadUser(
        email='email6',
        name='name0',
        username='username0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    verified=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

