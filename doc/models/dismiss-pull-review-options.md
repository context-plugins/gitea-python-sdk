
# Dismiss Pull Review Options

DismissPullReviewOptions are options to dismiss a pull request review

*This model accepts additional fields of type Any.*

## Structure

`DismissPullReviewOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | - |
| `priors` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.dismiss_pull_review_options import DismissPullReviewOptions

dismiss_pull_review_options = DismissPullReviewOptions(
    message='message8',
    priors=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

