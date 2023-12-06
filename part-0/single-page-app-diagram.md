::: mermaid
    sequenceDiagram
    participant browser
    participant server

    browser->>server: GET main.html (one HTML page fetched from the server, the contents of which are manipulated with JavaScript that executes in the browser)
:::