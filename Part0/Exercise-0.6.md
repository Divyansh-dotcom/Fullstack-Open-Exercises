```mermaid

sequenceDiagram
    participant User
    participant Browser
    participant Server
    
    User->>Browser: Fill out and submit new note form
    Browser->>Server: HTTP POST /new_note_spa (note data)
    Server-->>Browser: Response (confirmation of new note creation)
    Browser->>Server: HTTP GET /exampleapp/data.json
    Server-->>Browser: data.json (updated notes data)
    Browser->>User: displays updated notes
