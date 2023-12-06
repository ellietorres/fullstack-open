::: mermaid
    sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes (browser will send the user input to the server)
    server-->>browser: HTTP status code 302 (after adding the new li, the server asks the browser to do a new HTTP GET request to the address defined in the header's Location)
    Note right of browser: The browser then reloads the Notes page
    browser->>server: GET - style sheet (main.css)
    browser->>server: GET - JavaScript code (main.js)
    browser->>server: GET - raw data of the notes (data.json)
:::