# Sequence Diagram: Accessing Single-Page Application (SPA)

```mermaid
sequenceDiagram
    participant User
    participant SPA as Single-Page App
    participant Server

    User->>SPA: Open https://studies.cs.helsinki.fi/exampleapp/spa
    SPA->>Server: GET /exampleapp/spa
    Server-->>SPA: Serve SPA HTML and assets
    SPA-->>User: Render SPA interface
