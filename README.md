# CVE-2019-19368

#Title: Cross Site Scripting - Reflected
#Vendor: MAXUM Development (https://maxum.com)
#Affected Product: Rumpus FTP Web File Manager
#Affected Version: 8.2.9.1

Description:
A Reflected Cross Site Scripting was discovered in the main authentication page of Rumpus FTP Web File Manager. An attacker can exploit it by sending a crafted link to end users and can execute arbitrary JavaScripts

PoC: 

Payload: ?!'><sVg/OnLoAD=alert`1`//

URL: http://localhost/Login?!%27%3E%3CsVg/OnLoAD=alert`1`//

Solution:
Upgrade to the latest version.
