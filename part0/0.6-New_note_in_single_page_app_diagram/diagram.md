```mermaid
note over browser:
the user enters a note into the text field
the browser executes the event handler
to submit the form
end note

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa

note over browser:
browser update the notes
array, and render on page
end note

server-->browser: HTTP 201 Created
```