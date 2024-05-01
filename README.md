# mermaid-playground
Mermaid playground

## Flowchart

```mermaid
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
```

## Pie chart

### showdata and style outer stroke

```mermaid
%%{init: {"pie": {"textPosition": 0.5}, "themeVariables": {"pieOuterStrokeWidth": "3px"}} }%%
pie showData
    title Work items overview
    "New" : 1
    "Ongoing" : 10
    "Code review" : 5
    "Resolved" :  6
    "Closed" : 6
```

### dark theme

```mermaid
%%{init: {'theme':'dark'}}%%
pie
    title Status
    "New" : 1
    "Ongoing" : 10
    "Code review" : 5
    "Resolved" :  6
    "Closed" : 6
```

### Custom colors

```mermaid
%%{init: {
    'theme': 'base',
    'themeVariables': {
      'primaryColor': '#64518a',
      'primaryTextColor': '#0c0d0e',
      'primaryBorderColor': '#7C0000',
      'lineColor': '#F8B229',
      'secondaryColor': '#e98a2e',
      'tertiaryColor': '#20a5de'
    }
  }
}%%
pie
    title Status
    "New" : 1
    "Ongoing" : 10
    "Code review" : 5
    "Resolved" :  6
    "Closed" : 6
```