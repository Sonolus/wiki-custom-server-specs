# `Search`

`Search` provides search configuration, and is used by Sonolus app to populate search interface.

## Syntax

```ts
type Search = {
    options: SearchOption[]
}

type SearchOption =
    | SearchTextOption
    | SearchSliderOption
    | SearchToggleOption
    | SearchSelectOption

type SearchTextOption = {
    query: string
    name: string
    type: 'text'
    placeholder: string
}

type SearchSliderOption = {
    query: string
    name: string
    type: 'slider'
    def: number
    min: number
    max: number
    step: number
    display: 'number' | 'percentage'
}

type SearchToggleOption = {
    query: string
    name: string
    type: 'toggle'
    def: 0 | 1
}

type SearchSelectOption = {
    query: string
    name: string
    type: 'select'
    def: number
    values: string[]
}
```

### `query`

Name of query parameter used to identify the search option.

## Examples

```json
{
    "options": [
        {
            "query": "keywords",
            "name": "#KEYWORDS",
            "type": "text",
            "placeholder": "#KEYWORDS"
        },
        {
            "query": "minRating",
            "name": "#RATING_MINIMUM",
            "type": "slider",
            "def": 0,
            "min": 0,
            "max": 100,
            "step": 1,
            "display": "number"
        }
    ]
}
```

When user submits the search, the following query parameters will be sent:

```url
?keywords=expert&minRating=75
```

## Remarks

While it is possible to change search between requests, it is recommended to keep it consistent.
