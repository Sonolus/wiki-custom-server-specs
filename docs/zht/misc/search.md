# `Search`

`Search`提供了搜尋的設定，並會被Sonolus程式用於填充搜索界面。

## 語法

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

用於識別搜索選項的查詢參數的名稱。

## 例子

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

當用戶提交搜尋時，將發送以下查詢參數：

```url
?keywords=expert&minRating=75
```

## 備註

雖然可以在請求之間更改搜尋，但建議保持一致。
