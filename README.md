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

### PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler
content='''
 <!doctype html>
 <html>
 <head>
 <title> My Web Server</title>
 </head>
 <body>
 <h1>Top Five Web Application Development Frameworks</h1>
 <h2>1.Django</h2>
 <h2>2. MEAN Stack</h2>
 <h2>3. React </h2>
 <h2>4. String </h2>
 <h2>5. MERN Stack</h2>
 </body>
 </html>
 '''
class MyServer(BaseHTTPRequestHandler):
def do_GET(self):
print("Get request received...")
self.send_response(200) 
self.send_header("content-type", "text/html") 
self.end_headers()
self.wfile.write(content.encode())
print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
![serveroutput](serveroutput.png)
![serveroutput](clientoutput.png)
class MyServer(BaseHTTPRequestHandler):
def do_GET(self):
print("Get request received...")
self.send_response(200) 
self.send_header("content-type", "text/html") 
self.end_headers()
self.wfile.write(content.encode())
print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
## OUTPUT:
<h3>Server Output:</h3>

![output1](https://github.com/Narendran-sec/webserver/assets/147473131/40ec8e02-dcb7-4c41-bac3-8a8cc5633c84)


<h3>Client Output:</h3>

![output2](https://github.com/Narendran-sec/webserver/assets/147473131/3054f4d8-e6c2-4d85-8458-ce1fd09bfa93)


## RESULT:
The program is executed succesfully
