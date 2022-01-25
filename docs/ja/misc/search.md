# `Search`

`Search`は検索の構成を提供し、Sonolusアプリが検索インターフェースのフォームを構成するために利用されます。

## 構文

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

検索オプションを識別するために使用されるクエリパラメータの名前。

## 例

```json
{
    "search": {
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
}
```

ユーザーが検索フォームをSubmitすると、次のようなクエリパラメータが送信されます。

```url
?keywords=expert&minRating=75
```

## 備考

エンドポイント毎に検索フォームを変更することは可能ですが、一貫性を保つことをお勧めします。
