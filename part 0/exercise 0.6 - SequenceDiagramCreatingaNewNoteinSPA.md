# Sequence Diagram: Creating a New Note in SPA

```mermaid
sequenceDiagram
    participant User
    participant SPA as Single-Page App
    participant Server

    User->>SPA: Enter text into text field
    User->>SPA: Click "Save" button
    SPA->>Server: POST /notes with note data
    Server-->>SPA: 200 OK (or error) response
    SPA-->>User: Update UI with new note
