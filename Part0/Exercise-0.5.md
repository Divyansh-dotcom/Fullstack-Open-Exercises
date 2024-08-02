```mermaid

sequenceDiagram
    participant Browser
    participant Server
    
    
    Browser->>Server: HTTP GET /exampleapp/spa
    activate server
    Server-->>Browser: HTML for single-page app
    decativate server


    Browser->>Server: HTTP GET /exampleapp/spa.js
    activate server
    Server-->>Browser: spa.js
    deactivate server


    Browser->>Server: HTTP GET /exampleapp/main.css
activate server
    Server-->>Browser: main.css
deactivate server

    Browser->>Server: HTTP GET /exampleapp/data.json
activate server
    Server-->>Browser: data.json (notes data)
deactivate server
