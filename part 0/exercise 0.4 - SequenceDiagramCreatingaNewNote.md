# Sequence Diagram: Creating a New Note

```mermaid
sequenceDiagram
    participant User
    participant WebPage as Web Page (Client)
    participant Server

    User->>WebPage: Enter text into text field
    User->>WebPage: Click "Save" button
    WebPage->>Server: POST /notes with note data
    Server-->>WebPage: 200 OK (or error) response
    WebPage->>User: Display updated note list
