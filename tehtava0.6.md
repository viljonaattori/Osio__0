```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: Käyttäjä kirjoittaa muistiinpanon tekstikenttään ja painaa "Save"

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: HTTP 201 Created
    deactivate server

    Note right of browser:Selain päivittää käyttöliittymän lisäämällä uuden muistiinpanon ilman sivun uudelleenlatausta

    Note over browser: Uusi muistiinpano lisätään muistiinpanolistaan JavaScriptin avulla
```
