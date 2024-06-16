# `ServerForm`

`ServerForm` provides a form, and is used by Sonolus app to populate various interfaces such as search.

## Syntax

```ts
type ServerForm = {
    type: string
    title: Text | (string & {})
    icon?: Icon | (string & {})
    options: ServerOption[]
}

type ServerOption =
    | ServerTextOption
    | ServerTextAreaOption
    | ServerSliderOption
    | ServerToggleOption
    | ServerSelectOption
    | ServerMultiOption
    | ServerServerItemOption
    | ServerCollectionItemOption
    | ServerFileOption

type ServerTextOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
    type: 'text'
    placeholder: Text | (string & {})
    limit?: number
}

type ServerTextAreaOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
    type: 'textArea'
    placeholder: Text | (string & {})
    limit?: number
}

type ServerSliderOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
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
    description?: string
    required?: boolean
    type: 'toggle'
    def: 0 | 1
}

type ServerSelectOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
    type: 'select'
    def: number
    values: (Text | (string & {}))[]
}

type ServerMultiOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
    type: 'multi'
    defs: boolean[]
    values: (Text | (string & {}))[]
}

type ServerServerItemOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
    type: 'serverItem'
    itemType: ItemType
}

type ServerCollectionItemOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
    type: 'collectionItem'
    itemType: ItemType
}

type ServerFileOption = {
    query: string
    name: Text | (string & {})
    description?: string
    required?: boolean
    type: 'file'
}
```

### `query`

Name of query parameter used to identify the option.

### `required`

If `true`, player is required to modify the value.

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
