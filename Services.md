# Services # 

Android Root Bridge Dork |
------------------ | 
Find android root bridges with port 5555.
```
"Android Debug Bridge" "Device" port:5555
```

Misconfigured Wordpress Sites Dork |
------------------ | 
he wp-config.php if accessed can give out the database credentials.
```
http.html:"* The wp-config.php creation script uses this file"
```

PEM Certificates Dork |
------------------ | 
Find Exposed Certificates 
```
http.title:"Index of /" http.html:".pem"
```

API Keys  Dork |
------------------ | 
Search for secret API keys publicly exposed on websites :
ex : Searching for slack API token on all the scanned websites 
```
http.html:"xoxb-"
```
