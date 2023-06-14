# Current Dataflow (Email-rendering)

```mermaid
sequenceDiagram
    participant Braze
    participant Newsletters API
    participant CAPI
    Braze->>Newsletters API: Get Newsletter HTML
    Newsletters API->>CAPI: Fetch Article Content
    CAPI-->>Newsletters API: Article Content
    Newsletters API-->>Braze: Newsletter HTML!
```
