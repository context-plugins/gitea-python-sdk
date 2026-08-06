
# Wiki Page Meta Data

WikiPageMetaData wiki page meta information

*This model accepts additional fields of type Any.*

## Structure

`WikiPageMetaData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `html_url` | `str` | Optional | The HTML URL to view the wiki page |
| `last_commit` | [`WikiCommit`](../../doc/models/wiki-commit.md) | Optional | WikiCommit page commit/revision |
| `sub_url` | `str` | Optional | The sub URL path for the wiki page |
| `title` | `str` | Optional | The title of the wiki page |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from gitea.models.wiki_commit import WikiCommit
from gitea.models.wiki_page_meta_data import WikiPageMetaData

wiki_page_meta_data = WikiPageMetaData(
    html_url='html_url8',
    last_commit=WikiCommit(
        author=CommitUserContainsInformationOfAUserInTheContextOfACommit(
            date='date6',
            email='email6',
            name='name0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        commiter=CommitUserContainsInformationOfAUserInTheContextOfACommit(
            date='date2',
            email='email4',
            name='name2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        message='message8',
        sha='sha4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    sub_url='sub_url0',
    title='title2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

