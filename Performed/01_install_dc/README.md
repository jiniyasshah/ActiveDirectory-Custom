# 01 - Install Domain Controller

1. Use 'Sconfig' to:
   - Change the hostname.
   - Change the IP Address to static
   - Change DNS Server to our own IP Address (192.168.48.155)

2. Install the Active Directory Windows Feature
   - Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
   
3. Setting up DNS Server
   - Get-NetIPAddress
   - Set-DnsClientServerAddress -InterfaceIndex 7 -ServerAddress 192.168.48.155
   - Get-DNSClientServerAddress

4. Setting up ADDSForest
   - Import-Module ADDSDeployment
   - Install-ADDSForest 


# 02 - Install WorkStation

1. Setup the DNS Server
   - Set-DnsClientServerAddress -InterfaceIndex 7 -ServerAddress 192.168.48.155
   - Get-DNSClientServerAddress

2. Add the workstation to Domain Controller
   - Add-Computer -DomainName zero.com -Credential zero\Administrator -Force -Restart
   



