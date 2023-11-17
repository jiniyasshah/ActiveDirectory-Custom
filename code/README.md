# Commands:

Default:
(By default 5 Users with 1 Group and 0 LocalAdmins will be created)
* .\random_gen.ps1 out.ps1

Arguments:
* .\random_gen.ps1 out.ps1 -UserCount 10 -GroupCount 3 -LocalAdminCount 2
It will create 3 Groups with 10 Users and 2 LocalAdmin accounts


Finally, inside DomainController
* .\gen_ad.ps1 .\out.json


