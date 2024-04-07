# `ServerOptionsSection`

`ServerOptionsSection` provides a section of options, and is used by Sonolus app to populate various interfaces such as search.

## Syntax

```ts
type ServerOptionsSection = {
    type: string
    title: Text | (string & {})
    icon?: Icon
    options: ServerOption[]
}

type ServerOption =
    | ServerTextOption
    | ServerSliderOption
    | ServerToggleOption
    | ServerSelectOption
    | ServerMultiOption

type ServerTextOption = {
    query: string
    name: Text | (string & {})
    type: 'text'
    placeholder: Text | (string & {})
}

type ServerSliderOption = {
    query: string
    name: Text | (string & {})
    type: 'slider'
    def: number
    min: number
    max: number
    step: number
    unit?: Text | (string & {})
}

type ServerToggleOption = {
    query: string
    name: Text | (string & {})
    type: 'toggle'
    def: 0 | 1
}

type ServerSelectOption = {
    query: string
    name: Text | (string & {})
    type: 'select'
    def: number
    values: (Text | (string & {}))[]
}

type ServerMultiOption = {
    query: string
    name: Text | (string & {})
    type: 'multi'
    defs: boolean[]
    values: (Text | (string & {}))[]
}
```

### `query`

Name of query parameter used to identify the option.

## Examples

```json
{
    "type": "advanced",
    "title": "#ADVANCED",
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
            "step": 1
        },
        {
            "query": "random",
            "name": "#RANDOM",
            "type": "toggle",
            "def": 0
        },
        {
            "query": "genre",
            "name": "#GENRE",
            "type": "select",
            "def": 0,
            "values": [
                // ...
            ]
        },
        {
            "query": "difficulty",
            "name": "#DIFFICULTY",
            "type": "multi",
            "def": [
                // ...
            ],
            "values": [
                // ...
            ]
        }
    ]
}
```

When user submits, the following query parameters will be sent:

```url
?type=advanced&keywords=expert&minRating=75&random=1&genre=3&difficulty=10011
```
