# 01 - Install Domain Controller

1. Use 'Sconfig' to:
   - Change the hostname.
   - Change the IP Address to static
   - Change DNS Server to our own IP Address (192.168.48.155)

2.. Install the Active Directory Windows Feature


...Shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
...