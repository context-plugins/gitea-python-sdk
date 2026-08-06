
# Create or Update Secret Option

CreateOrUpdateSecretOption options when creating or updating secret

*This model accepts additional fields of type Any.*

## Structure

`CreateOrUpdateSecretOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `str` | Required | Data of the secret to update |
| `description` | `str` | Optional | Description of the secret to update |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_or_update_secret_option import CreateOrUpdateSecretOption

create_or_update_secret_option = CreateOrUpdateSecretOption(
    data='data4',
    description='description4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

