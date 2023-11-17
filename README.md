* Active Directory Setup

Rename PC
* Rename-Computer WS03

Setting up DNS Server
* Set-DnsClientServerAddress -InterfaceIndex 7 -ServerAddress 192.***.**.155

Add To DC
* $username = "Administrator"
* $password = ConvertTo-SecureString "Pass****" -AsPlainText -Force
* $credentials = New-Object System.Management.Automation.PSCredential -ArgumentList $username, $password
* Add-Computer -DomainName zero.com -Credential $credentials -Force

Add DC To Trusted Hosts
* Start-Service WinRM
* Set-Item wsman:\localhost\client\trustedhosts -value dc-1.zero.com -Force

Enable DC To execute commands on Workstation
* Enable-PSRemoting

