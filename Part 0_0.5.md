SequenceDiagram 
     participant B as Browser 
     participant S as Server 
     Browser->>:HTTP GET https://studies.cs.helsinki./f/exampleapp/spa activate server 
     Server-->> Browser:HTML document deactivate server --> Browser : HTML document deactivate server 
     Note right of Browser : Browser starts executing the HTML then request CSS and JavaScript files
     Browser ->> Server : HTTP GET https://studies.cs.helsinki.fi activate server 
     Server --> Browser :Main.CSS deactivate server 
     Browser ->> Server : GET https://studies.cs.helsinki.fi/exampleapp/spa.js activate server 
     Server -->>Browser:JavaScript file deactivate server 
     Note right of Browser : Browser execute spa.js
     Browser ->> Server : HTTP GET https://studies.cs.helsinki.fi activate server 
     Server -->> Browser : data.json(the notes) deactivate server 
     Note right of Browser : Browser renders notes dynamically on the page 