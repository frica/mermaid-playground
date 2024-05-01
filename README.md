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


## Git graph

### Tags

```mermaid
gitGraph
       commit
       commit id: "Normal" tag: "RC 1"
       commit
       commit id: "Reverse" type: REVERSE tag: "RC_2"
       commit
       commit id: "Highlight" type: HIGHLIGHT tag: "v1.0.0"
       commit
```

### No branch label, no commit labels

```mermaid
%%{init: { 'logLevel': 'debug', 'theme': 'forest', 'gitGraph': {'showBranches': false, 'showCommitLabel': false}} }%%
gitGraph
       commit
       commit id: "Normal" tag: "RC 1"
       commit
       commit id: "Reverse" type: REVERSE tag: "RC_2"
       commit
       commit id: "Highlight" type: HIGHLIGHT tag: "v1.0.0"
       commit
```

### Merges

```mermaid
gitGraph
    commit
    commit
    branch develop
    commit
    branch feature
    checkout feature
    commit
    commit
    commit
    checkout develop
    merge feature
    checkout main
    commit
    merge develop tag: "RC 1"
    commit
```

### Top to bottom

```mermaid
gitGraph TB:
    commit
    commit
    branch develop
    commit
    branch feature
    checkout feature
    commit
    commit
    commit
    checkout develop
    merge feature tag: "RC 1"
    checkout main
    commit
    merge develop tag: "Beta 1"
    commit
```