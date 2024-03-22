# EX01 Developing a Simple Webserver
## Date:25-02-2024

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>TOP SOFTWARE COMPANIES IN REVENUE</title>
</head>
<body>
<center><h1> TOP SOFTWARE COMPANIES IN REVENUE</h1></centre>
<table border="10" cellspacing="10"  width="75" height="100"
            <tr align="center">
                <th bgcolor="yellow">Rank</th>
                <th bgcolor="yellow">Company</th>
                <th bgcolor="yellow">Sales</th>
                <th bgcolor="yellow">Nationality</th>
            </tr>
            <tr align="center">
                <td bgcolor="blue">1</td>
                <td bgcolor="red">Microsoft</td>
                <td bgcolor="red">57.9</td>
                <td bgcolor="red">USA</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">2</td>
                <td bgcolor="red">Oracle</td>
                <td bgcolor="red">21.0</td>
                <td bgcolor="red">USA</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">3</td>
                <td bgcolor="red">SAP</td>
                <td bgcolor="red">16.1</td>
                <td bgcolor="red">Germany</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">4</td>
                <td bgcolor="red">Computer Associates</td>
                <td bgcolor="red">4.2</td>
                <td bgcolor="red">USA</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">5</td>
                <td bgcolor="red">Adobe</td>
                <td bgcolor="red">3.4</td>
                <td bgcolor="red">USA</td>
            </tr>
 </table>       
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
![Screenshot 2024-03-15 094728](https://github.com/Aaron-0111/simplewebserver/assets/149347631/af2f75dc-d622-4ad0-9c69-dcdfb0a291fb)
![Screenshot 2024-03-15 094843](https://github.com/Aaron-0111/simplewebserver/assets/149347631/c5e0503b-f341-4a44-91ff-66f18b6e5dde)



## RESULT:
The program for implementing simple webserver is executed successfully.
