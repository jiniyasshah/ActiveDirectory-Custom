# 01 - Install Domain Controller

1. Use 'Sconfig' to:
   - Change the hostname.
   - Change the IP Address to static
   - Change DNS Server to our own IP Address (192.168.48.155)

2. Install the Active Directory Windows Feature

-----------------------------------------------------------------------
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
-----------------------------------------------------------------------


-----------------------------------------------------------------------
Get-NetIPAddress
Set-DnsClientServerAddress -InterfaceIndex 7 -ServerAddress 192.168.48.155
Get-DNSClientServerAddress
-----------------------------------------------------------------------


3. Joining the Workstation to the domain
-----------------------------------------------------------------------
Add-Computer -DomainName zero.com -Credential zero\Administrator -Force -Restart
-----------------------------------------------------------------------
