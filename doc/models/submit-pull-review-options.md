
# Submit Pull Review Options

SubmitPullReviewOptions are options to submit a pending pull request review

*This model accepts additional fields of type Any.*

## Structure

`SubmitPullReviewOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | - |
| `event` | [`Event`](../../doc/models/event.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.event import Event
from giteaapi.models.submit_pull_review_options import SubmitPullReviewOptions

submit_pull_review_options = SubmitPullReviewOptions(
    body='body6',
    event=Event.APPROVED,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

