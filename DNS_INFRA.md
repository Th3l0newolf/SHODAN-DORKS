# DNS SERVERS # 

DNS Dork |
------------------ | 
DNS servers with recursion enabled can be a huge source of network threats. To find these servers, one can use the query:

```
"port: 53" Recursion: Enabled
```

Network Infrastructure Dork |
------------------ | 
To find devices running a specific version of a RouterOS operating system that powers routers, switches and other networking equipment from the company MikroTik, we use the following search query, This allows us to find those switches, routers and other networking gear running an older and possibly vulnerable version of the RouterOS operating system which runs on port number 8291, used for the web management UI.



```
port:8291 os:"MikroTik RouterOS 6.45.9"
```

Web servers Dork |
------------------ | 
we’ll use this to find IPs that host a specific version of the popular web server Apache:
```
product:"Apache httpd" port:"80"
```

Microsoft IIS Dork |
------------------ | 
Similarly, to look up Microsoft IIS-powered websites and web servers:
```
product:"Microsoft IIS httpd"
```

Nginx servers Dork |
------------------ | 
To look up Nginx-powered websites and web servers:

The below product query can be combined with the “port” option too. For example, if you wish to lookup Nginx-powered web servers on port 8080:
```
product:"nginx"

"port: 8080" product:"nginx"
```

Operating systems Dork |
------------------ | 
we’ll use this to find IPs that host a specific version of the popular web server Apache:
```
os:"windows 7

os:"Windows 10 Home 19041"

os:"Linux"
```
