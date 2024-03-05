```mermaid

sequenceDiagram
    participant browser
    participant server

    Note right of browser: The user creates a new note

    browser-->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note left of server: The new note is saves and the browser render the notes to display
    server-->>browser: [{ "content": "New note", "date": "2024-03-03" }, ... ]
    deactivate server
    