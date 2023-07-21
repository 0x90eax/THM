10.10.93.135:RA:Windows:

nmap::
```
53/tcp   open  domain              Simple DNS Plus
80/tcp   open  http                Microsoft IIS httpd 10.0
|_http-server-header: Microsoft-IIS/10.0
| http-methods: 
|_  Potentially risky methods: TRACE
|_http-title: Windcorp.
88/tcp   open  kerberos-sec        Microsoft Windows Kerberos (server time: 2023-07-18 02:06:43Z)
135/tcp  open  msrpc               Microsoft Windows RPC
139/tcp  open  netbios-ssn         Microsoft Windows netbios-ssn
443/tcp  open  ssl/http            Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
| http-ntlm-info: 
|   Target_Name: WINDCORP
|   NetBIOS_Domain_Name: WINDCORP
|   NetBIOS_Computer_Name: FIRE
|   DNS_Domain_Name: windcorp.thm
|   DNS_Computer_Name: Fire.windcorp.thm
|   DNS_Tree_Name: windcorp.thm
|_  Product_Version: 10.0.17763
| tls-alpn: 
|_  http/1.1
|_http-server-header: Microsoft-HTTPAPI/2.0
| http-auth: 
| HTTP/1.1 401 Unauthorized\x0D
|   Negotiate
|_  NTLM
| ssl-cert: Subject: commonName=Windows Admin Center
| Subject Alternative Name: DNS:WIN-2FAA40QQ70B
| Not valid before: 2020-04-30T14:41:03
|_Not valid after:  2020-06-30T14:41:02
|_ssl-date: 2023-07-18T02:08:30+00:00; +7m58s from scanner time.
|_http-title: Site doesn't have a title.
445/tcp  open  microsoft-ds?
464/tcp  open  kpasswd5?
593/tcp  open  ncacn_http          Microsoft Windows RPC over HTTP 1.0
2179/tcp open  vmrdp?
3268/tcp open  ldap                Microsoft Windows Active Directory LDAP (Domain: windcorp.thm0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped
3389/tcp open  ms-wbt-server       Microsoft Terminal Services
|_ssl-date: 2023-07-18T02:08:30+00:00; +7m58s from scanner time.
| ssl-cert: Subject: commonName=Fire.windcorp.thm
| Not valid before: 2023-07-17T01:58:17
|_Not valid after:  2024-01-16T01:58:17
| rdp-ntlm-info: 
|   Target_Name: WINDCORP
|   NetBIOS_Domain_Name: WINDCORP
|   NetBIOS_Computer_Name: FIRE
|   DNS_Domain_Name: windcorp.thm
|   DNS_Computer_Name: Fire.windcorp.thm
|   DNS_Tree_Name: windcorp.thm
|   Product_Version: 10.0.17763
|_  System_Time: 2023-07-18T02:07:45+00:00
5269/tcp open  xmpp                Wildfire XMPP Client
| xmpp-info: 
|   STARTTLS Failed
|   info: 
|     xmpp: 
|     unknown: 
|     features: 
|     errors: 
|       (timeout)
|     capabilities: 
|     auth_mechanisms: 
|_    compression_methods: 
7070/tcp open  http                Jetty 9.4.18.v20190429
|_http-title: Openfire HTTP Binding Service
|_http-server-header: Jetty(9.4.18.v20190429)
7443/tcp open  ssl/http            Jetty 9.4.18.v20190429
|_http-server-header: Jetty(9.4.18.v20190429)
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:*.fire.windcorp.thm
| Not valid before: 2020-05-01T08:39:00
|_Not valid after:  2025-04-30T08:39:00
|_http-title: Openfire HTTP Binding Service
7777/tcp open  socks5              (No authentication; connection not allowed by ruleset)
| socks-auth-info: 
|_  No authentication
9090/tcp open  zeus-admin?
| fingerprint-strings: 
|   GetRequest: 
|     HTTP/1.1 200 OK
|     Date: Tue, 18 Jul 2023 02:06:42 GMT
|     Last-Modified: Fri, 31 Jan 2020 17:54:10 GMT
|     Content-Type: text/html
|     Accept-Ranges: bytes
|     Content-Length: 115
|     <html>
|     <head><title></title>
|     <meta http-equiv="refresh" content="0;URL=index.jsp">
|     </head>
|     <body>
|     </body>
|     </html>
|   HTTPOptions: 
|     HTTP/1.1 200 OK
|     Date: Tue, 18 Jul 2023 02:06:52 GMT
|     Allow: GET,HEAD,POST,OPTIONS
|   JavaRMI, drda, ibm-db2-das, informix: 
|     HTTP/1.1 400 Illegal character CNTL=0x0
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 69
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x0</pre>
|   SqueezeCenter_CLI: 
|     HTTP/1.1 400 No URI
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 49
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: No URI</pre>
|   WMSRequest: 
|     HTTP/1.1 400 Illegal character CNTL=0x1
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 69
|     Connection: close
|_    <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x1</pre>
9091/tcp open  ssl/xmltec-xmlmail?
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:*.fire.windcorp.thm
| Not valid before: 2020-05-01T08:39:00
|_Not valid after:  2025-04-30T08:39:00
| fingerprint-strings: 
|   DNSStatusRequestTCP, DNSVersionBindReqTCP: 
|     HTTP/1.1 400 Illegal character CNTL=0x0
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 69
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x0</pre>
|   GetRequest: 
|     HTTP/1.1 200 OK
|     Date: Tue, 18 Jul 2023 02:07:06 GMT
|     Last-Modified: Fri, 31 Jan 2020 17:54:10 GMT
|     Content-Type: text/html
|     Accept-Ranges: bytes
|     Content-Length: 115
|     <html>
|     <head><title></title>
|     <meta http-equiv="refresh" content="0;URL=index.jsp">
|     </head>
|     <body>
|     </body>
|     </html>
|   HTTPOptions: 
|     HTTP/1.1 200 OK
|     Date: Tue, 18 Jul 2023 02:07:07 GMT
|     Allow: GET,HEAD,POST,OPTIONS
|   Help: 
|     HTTP/1.1 400 No URI
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 49
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: No URI</pre>
|   RPCCheck: 
|     HTTP/1.1 400 Illegal character OTEXT=0x80
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 71
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character OTEXT=0x80</pre>
|   RTSPRequest: 
|     HTTP/1.1 400 Unknown Version
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 58
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Unknown Version</pre>
|   SSLSessionReq: 
|     HTTP/1.1 400 Illegal character CNTL=0x16
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 70
|     Connection: close
|_    <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x16</pre>
2 services unrecognized despite returning data. If you know the service/version, please submit the following fingerprints at https://nmap.org/cgi-bin/submit.cgi?new-service :

Host script results:
|_clock-skew: mean: 7m57s, deviation: 0s, median: 7m57s
| smb2-time: 
|   date: 2023-07-18T02:07:47
|_  start_date: N/A
| smb2-security-mode: 
|   311: 
|_    Message signing enabled and required

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 17 19:00:39 2023 -- 1 IP address (1 host up) scanned in 141.85 seconds
er CNTL=0x1</pre>
9091/tcp open  ssl/xmltec-xmlmail?
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:*.fire.windcorp.thm
| Not valid before: 2020-05-01T08:39:00
|_Not valid after:  2025-04-30T08:39:00
| fingerprint-strings: 
|   DNSStatusRequestTCP, DNSVersionBindReqTCP: 
|     HTTP/1.1 400 Illegal character CNTL=0x0
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 69
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x0</pre>
|   GetRequest: 
|     HTTP/1.1 200 OK
|     Date: Tue, 18 Jul 2023 02:07:06 GMT
|     Last-Modified: Fri, 31 Jan 2020 17:54:10 GMT
|     Content-Type: text/html
|     Accept-Ranges: bytes
|     Content-Length: 115
|     <html>
|     <head><title></title>
|     <meta http-equiv="refresh" content="0;URL=index.jsp">
|     </head>
|     <body>
|     </body>
|     </html>
|   HTTPOptions: 
|     HTTP/1.1 200 OK
|     Date: Tue, 18 Jul 2023 02:07:07 GMT
|     Allow: GET,HEAD,POST,OPTIONS
|   Help: 
|     HTTP/1.1 400 No URI
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 49
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: No URI</pre>
|   RPCCheck: 
|     HTTP/1.1 400 Illegal character OTEXT=0x80
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 71
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character OTEXT=0x80</pre>
|   RTSPRequest: 
|     HTTP/1.1 400 Unknown Version
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 58
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Unknown Version</pre>
|   SSLSessionReq: 
|     HTTP/1.1 400 Illegal character CNTL=0x16
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 70
|     Connection: close
|_    <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x16</pre>
2 services unrecognized despite returning data. If you know the service/version, please submit the following fingerprints at https://nmap.org/cgi-bin/submit.cgi?new-service :
Host script results:
|_clock-skew: mean: 7m57s, deviation: 0s, median: 7m57s
| smb2-time: 
|   date: 2023-07-18T02:07:47
|_  start_date: N/A
| smb2-security-mode: 
|   311: 
|_    Message signing enabled and required

-sU:
123/udp open  ntp
389/udp open  lda
```

Exploiting LDAP Server NULL Bind – n00py Blog
[](https://github.com/0x90eax/THM/assets/137312046/87a0ea46-6c08-42b3-b287-6a310aa9dbf7)
```
200      GET        5l       53w     1890c http://10.10.93.135/css/landing-page.min.css
200      GET       11l       68w     3738c http://10.10.93.135/img/button-openfire-88x30.gif
200      GET      778l     1216w    12958c http://10.10.93.135/vendor/simple-line-icons/css/simple-line-icons.css
200      GET        5l       83w    56517c http://10.10.93.135/vendor/fontawesome-free/css/all.min.css
200      GET        7l      989w    78635c http://10.10.93.135/vendor/bootstrap/js/bootstrap.bundle.min.js
200      GET     1196l     7265w   546885c http://10.10.93.135/img/bg-showcase-1.jpg
200      GET        2l     1276w    88145c http://10.10.93.135/vendor/jquery/jquery.min.js
200      GET        7l     1966w   155758c http://10.10.93.135/vendor/bootstrap/css/bootstrap.min.css
200      GET        0l        0w   197349c http://10.10.93.135/img/bg-showcase-2.jpg
200      GET        0l        0w   193507c http://10.10.93.135/img/kirkug.jpg
200      GET        0l        0w   136643c http://10.10.93.135/img/Emilieje.jpg
200      GET        0l        0w   314857c http://10.10.93.135/img/bg-showcase-3.jpg
200      GET        0l        0w   181211c http://10.10.93.135/img/lilyleAndSparky.jpg
```

http://10.10.93.135:7070/
  openfire http binding service

http://10.10.93.135:9090/login.jsp?url=%2Findex.jsp
  amdin login page

python3
```
>>> import ldap3
>>> server = ldap3.Server('10.10.93.135', get_info = ldap3.ALL, port=3268)
>>> connection = ldap3.Connection(server)
>>> connection.bind()
True
>>> server.info
DSA info (from DSE):
  Supported LDAP versions: 3, 2
  Naming contexts: 
    DC=windcorp,DC=thm
    CN=Configuration,DC=windcorp,DC=thm
    CN=Schema,CN=Configuration,DC=windcorp,DC=thm
    DC=ForestDnsZones,DC=windcorp,DC=thm
    DC=DomainDnsZones,DC=windcorp,DC=thm
  Supported controls: 
    1.2.840.113556.1.4.1338 - Verify name - Control - MICROSOFT
    1.2.840.113556.1.4.1339 - Domain scope - Control - MICROSOFT
    1.2.840.113556.1.4.1340 - Search options - Control - MICROSOFT
    1.2.840.113556.1.4.1341 - RODC DCPROMO - Control - MICROSOFT
    1.2.840.113556.1.4.1413 - Permissive modify - Control - MICROSOFT
    1.2.840.113556.1.4.1504 - Attribute scoped query - Control - MICROSOFT
    1.2.840.113556.1.4.1852 - User quota - Control - MICROSOFT
    1.2.840.113556.1.4.1907 - Server shutdown notify - Control - MICROSOFT
    1.2.840.113556.1.4.1948 - Range retrieval no error - Control - MICROSOFT
    1.2.840.113556.1.4.1974 - Server force update - Control - MICROSOFT
    1.2.840.113556.1.4.2026 - Input DN - Control - MICROSOFT
    1.2.840.113556.1.4.2064 - Show recycled - Control - MICROSOFT
    1.2.840.113556.1.4.2065 - Show deactivated link - Control - MICROSOFT
    1.2.840.113556.1.4.2066 - Policy hints [DEPRECATED] - Control - MICROSOFT
    1.2.840.113556.1.4.2090 - DirSync EX - Control - MICROSOFT
    1.2.840.113556.1.4.2204 - Tree deleted EX - Control - MICROSOFT
    1.2.840.113556.1.4.2205 - Updates stats - Control - MICROSOFT
    1.2.840.113556.1.4.2206 - Search hints - Control - MICROSOFT
    1.2.840.113556.1.4.2211 - Expected entry count - Control - MICROSOFT
    1.2.840.113556.1.4.2239 - Policy hints - Control - MICROSOFT
    1.2.840.113556.1.4.2255 - Set owner - Control - MICROSOFT
    1.2.840.113556.1.4.2256 - Bypass quota - Control - MICROSOFT
    1.2.840.113556.1.4.2309
    1.2.840.113556.1.4.2330
    1.2.840.113556.1.4.2354
    1.2.840.113556.1.4.319 - LDAP Simple Paged Results - Control - RFC2696
    1.2.840.113556.1.4.417 - LDAP server show deleted objects - Control - MICROSOFT
    1.2.840.113556.1.4.473 - Sort Request - Control - RFC2891
    1.2.840.113556.1.4.474 - Sort Response - Control - RFC2891
    1.2.840.113556.1.4.521 - Cross-domain move - Control - MICROSOFT
    1.2.840.113556.1.4.528 - Server search notification - Control - MICROSOFT
    1.2.840.113556.1.4.529 - Extended DN - Control - MICROSOFT
    1.2.840.113556.1.4.619 - Lazy commit - Control - MICROSOFT
    1.2.840.113556.1.4.801 - Security descriptor flags - Control - MICROSOFT
    1.2.840.113556.1.4.802 - Range option - Control - MICROSOFT
    1.2.840.113556.1.4.805 - Tree delete - Control - MICROSOFT
    1.2.840.113556.1.4.841 - Directory synchronization - Control - MICROSOFT
    1.2.840.113556.1.4.970 - Get stats - Control - MICROSOFT
    2.16.840.1.113730.3.4.10 - Virtual List View Response - Control - IETF
    2.16.840.1.113730.3.4.9 - Virtual List View Request - Control - IETF
  Supported extensions: 
    1.2.840.113556.1.4.1781 - Fast concurrent bind - Extension - MICROSOFT
    1.2.840.113556.1.4.2212 - Batch request - Extension - MICROSOFT
    1.3.6.1.4.1.1466.101.119.1 - Dynamic Refresh - Extension - RFC2589
    1.3.6.1.4.1.1466.20037 - StartTLS - Extension - RFC4511-RFC4513
    1.3.6.1.4.1.4203.1.11.3 - Who am I - Extension - RFC4532
  Supported features: 
    1.2.840.113556.1.4.1670 - Active directory V51 - Feature - MICROSOFT
    1.2.840.113556.1.4.1791 - Active directory LDAP Integration - Feature - MICROSOFT
    1.2.840.113556.1.4.1935 - Active directory V60 - Feature - MICROSOFT
    1.2.840.113556.1.4.2080 - Active directory V61 R2 - Feature - MICROSOFT
    1.2.840.113556.1.4.2237 - Active directory W8 - Feature - MICROSOFT
    1.2.840.113556.1.4.800 - Active directory - Feature - MICROSOFT
  Supported SASL mechanisms: 
    GSSAPI, GSS-SPNEGO, EXTERNAL, DIGEST-MD5
  Schema entry: 
    CN=Aggregate,CN=Schema,CN=Configuration,DC=windcorp,DC=thm
Other:
  domainFunctionality: 
    7
  forestFunctionality: 
    7
  domainControllerFunctionality: 
    7
  rootDomainNamingContext: 
    DC=windcorp,DC=thm
  ldapServiceName: 
    windcorp.thm:fire$@WINDCORP.THM
  isGlobalCatalogReady: 
    TRUE
  supportedLDAPPolicies: 
    MaxPoolThreads
    MaxPercentDirSyncRequests
    MaxDatagramRecv
    MaxReceiveBuffer
    InitRecvTimeout
    MaxConnections
    MaxConnIdleTime
    MaxPageSize
    MaxBatchReturnMessages
    MaxQueryDuration
    MaxDirSyncDuration
    MaxTempTableSize
    MaxResultSetSize
    MinResultSets
    MaxResultSetsPerConn
    MaxNotificationPerConn
    MaxValRange
    MaxValRangeTransitive
    ThreadMemoryLimit
    SystemMemoryLimitPercent
  serverName: 
    CN=FIRE,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=windcorp,DC=thm
  schemaNamingContext: 
    CN=Schema,CN=Configuration,DC=windcorp,DC=thm
  isSynchronized: 
    TRUE
  highestCommittedUSN: 
    205035
  dsServiceName: 
    CN=NTDS Settings,CN=FIRE,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=windcorp,DC=thm
  dnsHostName: 
    Fire.windcorp.thm
  defaultNamingContext: 
    DC=windcorp,DC=thm
  currentTime: 
    20230718033655.0Z
  configurationNamingContext: 
    CN=Configuration,DC=windcorp,DC=thm
```




  ldapServiceName: 
    windcorp.thm:fire$@WINDCORP.THM
