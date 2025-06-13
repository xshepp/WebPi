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

sudo lighttpd-enable-mod fastcgi
sudo lighttpd-enable-mod fastcgi-php
sudo lighttpd-enable-mod rewrite
sudo service lighttpd force-reload

added web dashboard for admin logins for pi-hole, router, and switch.

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>XS Home Network Dashboard</title>
  <style>
    body {
      background-color: #0f0f0f;
      color: #ffffff;
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 50px;
    }
    h1 { margin-bottom: 40px; }
    a {
      display: block;
      margin: 20px auto;
      padding: 15px 25px;
      width: 300px;
      background-color: #1e90ff;
      color: white;
      text-decoration: none;
      border-radius: 10px;
      font-size: 18px;
    }
    a:hover {
      background-color: #4682b4;
    }
  </style>
  <body>
    <h1> XS Home Network Dashboard</h1>
    <a href="http://192.168.1.245/admin/login" target="_blank">Pi-hole Admin</a>
    <a href="https:192.168.1.1" target="_blank">Router Login</a>
    <a href="https:192.168.1.10" target="_blank">Switch Login</a>
  </body>
  </html>

Current errors: Router and switch logins cannot be reached, connects to Pi-hole fine.
----
Fixed errors, was caused due to typos in the config.
Adjusted accordingly - 
<a href="http://192.168.1.1" target="_blank">Router Login</a>
<a href="http://192.168.1.10" target="_blank">Switch Login</a>
Proceeded to add an additional button for google, and set the web interface as my homepage.
<a href="https://google.com" target="_blank">Google</a>

