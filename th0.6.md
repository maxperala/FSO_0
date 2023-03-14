sequenceDiagram
    participant browser
    participant server
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa {content}
    activate server
    server-->>browser: JSON Response {message: 'note created'} code 201 (React re-renders the component)
    deactivate server
    