# WebPi
Utilzing a Raspberry Pi to run a web server

Config
------
sudo apt update
sudo apt install lighttpg -y
sudo systemctl status lighttpg
sudo nano /var/www/html/index.html

<!DOCTYPE html>
<html>
<head>
    <title>My Raspberry Pi Web Server</title>
    <meta charset="UTF-8">
    <style>
        body { font-family: Arial; background: #f2f2f2; padding: 40px; text-align: center; }
        h1 { color: #333; }
    </style>
</head>
<body>
    <h1>Hello from Raspberry Pi!</h1>
    <p>This is a web page served by Lighttpd.</p>
</body>
</html>
>Goto browser
>Enter <http://192.168.1.12>
>See result in webpitest.png

