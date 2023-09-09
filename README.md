# Developing a Simple Webserver
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:
```
Name: E. Varsha Sharon
Register Number: 212222100058

from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1 align="center">Top 5 <b>Revenue</b> Generating Companies</h1>
<hr>
<h3 align="center">Here's the list of the leading Revenue Companies in the world</h3>
<ul>
<li><b><u>Amazon</u></b></li>
<p>Amazon.com, Inc. is an American multinational technology company focusing on e-commerce, cloud computing, online advertising, digital streaming, and artificial intelligence. </p>
<br>
<li><b><u>Walmart</u></b></li>
<p>Walmart Inc. is an American multinational retail corporation that operates a chain of hypermarkets, discount department stores, and grocery stores. </p>
<br>
<li><b><u>Tesla</u></b></li>
<p>Tesla designs and manufactures electric vehicles, stationary battery energy storage devices from home to grid-scale, solar panels and solar shingles, and related products and services.</p>
<br>
<li><b><u>Toyota</u></b></li>
<p>Toyota Motor Corporation is a Japanese multinational automotive manufacturer headquartered in Toyota City, Aichi, Japan. </p>
<br>
<li><b><u>Shell</u></b></li>
<p>Shell is a public limited company with a primary listing on the London Stock Exchange and secondary listings on Euronext Amsterdam and the New York Stock Exchange. </p>

</ul>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## OUTPUT:
![simple webserver](https://github.com/varshasharon/simplewebserver/assets/98278161/f6303905-fb80-477a-9cdd-0592dc8e76a5)
![webrun](https://github.com/varshasharon/simplewebserver/assets/98278161/bb6c7989-08cf-41b1-bc9f-7dbed47a5e18)



## RESULT:
The program for implementing simple webserver is executed successfully.
