
#  👨‍💻 SHODAN-DORKS  #
⚡ **This Dorks lets users search for various types of servers connected to the internet using a variety of filters.**


# DATABASE #

Mongo DB Dork |
------------------ | 
To find MongoDB database servers which have open authentication over the public internet within Shodan, the following search query can be used:
```
"MongoDB Server Information" port:27017 -authentication
```

Mongo DB Dork |
------------------ | 
MongoDB also has a web management application similar to phpMyAdmin called Mongo Express Web GUI, which we can find with the following query:
```
"Set-Cookie: mongo-express=" "200 OK"
```
MySQL Dork |
------------------ | 
Similarly, to find MySQL-powered databases:
```
mysql port:"3306"
```

ElasticSearch Dork |
------------------ | 
To lookup popular ElasticSearch-powered instances:
```
port:"9200" all:"elastic indices"
```

PostgreSQL Dork |
------------------ | 
To look up for  PostgreSQL databases:
```
port:5432 PostgreSQL
```

# EXPOSED PORTS #

FTP Dork |
------------------ | 
For FTP, querying for proftpd, a popular FTP server:
```
proftpd port:21
```

FTP server Dork |
------------------ | 
To look for FTP servers that allow anonymous logins:
```
"220" "230 Login successful." port:21
```

OpenSSH Dork |
------------------ | 
To query for OpenSSH, a popular SSH server:
```
openssh port:22
```

Telnet Dork |
------------------ | 
For Telnet, querying for port 23:
```
port:"23"
```

EXIM-powered mail servers Dork |
------------------ | 
To look up EXIM-powered mail servers on port 25:
```
port:"25" product:"exim"
```
Memcached Dork |
------------------ | 
commonly seen on port 11211, has been a major source of UDP amplification attacks leading to huge DDoS attacks. Services running Memcached available on the public internet are often exploited for these attacks:
```
port:"11211" product:"Memcached"
```

Jenkins Dork |
------------------ | 
Jenkins is a popular automated build, deploy and test tool, often the starting point of any software being built for release. It can be found via the following query:
```
"X-Jenkins" "Set-Cookie: JSESSIONID" http.title:"Dashboard"
```




