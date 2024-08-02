```mermaid
sequenceDiagram
    participant browser
    participant server

   
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: send data in form of application/json
    deactivate server


    Note right of browser: Only one file is communicated- new_note_spa
    
