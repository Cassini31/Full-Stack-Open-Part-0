``` Mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Writes a new note on text field then clicks the save button.

    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Server-->>Browser: JSON File

    Browser->>User: Renders new note submitted by User.