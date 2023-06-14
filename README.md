# Newsletters Dataflow 

## Current Dataflow

```mermaid
sequenceDiagram
    participant Braze
    participant Email Rendering
    participant CAPI
    Braze->>Email Rendering: Get Newsletter HTML
    Email Rendering->>CAPI: Fetch Article Content
    CAPI-->>Email Rendering: Article Content
    Email Rendering-->>Braze: Newsletter HTML!
```

## New Dataflow

```mermaid
sequenceDiagram
    participant Braze
    participant Email Rendering
    participant CAPI
    participant Newsletters API
    Braze->>Email Rendering: Get Newsletter HTML
    Email Rendering->>CAPI: Fetch Article Content
    Email Rendering->>Newsletters API: Fetch Newsletter Metadata (Including Design (Theme))
    CAPI-->>Email Rendering: Article Content
    Newsletters API->>Email Rendering: Newsletter Metadata (Including Design (Theme))
    Email Rendering-->>Braze: Newsletter HTML!
```
