# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
'''
from http.server import HTTPServer,BaseHTTPRequestHandler

content ="""
<html>
<body>
<h1>Welcome to the webserver </h1>
</body>
</html>
"""

class WebHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
    
server_address=('',8000)
httpd=HTTPServer(server_address,WebHandler)
print("Web server running...")
httpd.serve_forever()    
'''

## OUTPUT:
### Server side output
![Server side output](./images/serversideoutput.png)
### Client side output
![Server side output](./images/clientsideoutput.png)

## RESULT:
The program is executed succesfully
