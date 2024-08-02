```mermaid

sequenceDiagram
    participant browser
    participant server
    
    
    browser-->>server: HTTP GET /exampleapp/spa
    activate server
    server-->>browser: HTML for single-page app
    deactivate server


    browser-->>server: HTTP GET /exampleapp/spa.js
    activate server
    server-->>browser: spa.js
    deactivate server


    browser-->>server: HTTP GET /exampleapp/main.css
activate server
    server-->>browser: main.css
deactivate server

    browser-->>server: HTTP GET /exampleapp/data.json
activate server
    server-->>browser: data.json (notes data)
deactivate server
