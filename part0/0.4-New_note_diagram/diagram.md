```mermaid
note over browser:
the user enters a note into the text field
the browser executes the event handler
to submit the form
end note

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note

server-->browser: HTTP 302 Redirect

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
server-->browser: HTML-code
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
server-->browser: main.js

note over browser:
the browser starts executing js-code
that requests JSON data from the server 
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ content: "HTML is easy", date: "2022-12-22" }, ..],

note over browser:
the browser executes the event handler
that renders notes to display
end note
```