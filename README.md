# Current Dataflow (Email-rendering)

```mermaid
    Braze->>+Newsletters API: Get Newsletter HTML
    Newsletters API->>+CAPI: Fetch Article Content
    CAPI-->>-Newsletters API: Article Content
    Newsletters API-->>-Braze: Newsletter HTML!
```
