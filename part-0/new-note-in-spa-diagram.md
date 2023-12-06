::: mermaid
    sequenceDiagram
    participant browser
    participant server

    Note right of browser: On save, the event handler creates a new note, adds it to the notes list with the command notes.push(note), rerenders the note list on the page
    browser->>server:  HTTP POST request and the data type is to be JSON
    server-->>browser: HTTP status code 201 created
:::