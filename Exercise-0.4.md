``` Mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Writes a new note on text field then clicks the save button.
    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    Server-->>Browser: HTML Document

    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server-->>Browser: HTML Document

    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server-->>Browser: CSS File

    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server-->>Browser: JavaScript File

    Note right of Browser: Browser executes the JavaScript File 

    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server-->>Browser: JSON File

    Browser->>User: Renders new note submitted by User.
```