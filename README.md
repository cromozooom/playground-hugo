# Sorting JSON data by date in HUGO

[link stackoverflow](https://stackoverflow.com/questions/69753662/sorting-json-data-by-date-in-hugo/69792627?noredirect=1#comment123396068_69792627)

## Solution

```
    {{ $json := getJSON "data/events.json" }}
    <ul>
        {{ range sort $json.events "date" "desc" }}
        <li>
            <b>
                {{ .name }}
            </b>
            <br>            
            {{ .date }}
        </li>
        {{ end }}
    </ul>
```

