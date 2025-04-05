# AKS-Cluster-terraform
This is repository is to bring AKS cluster in Azure with terraform code.

Link: https://learn.microsoft.com/en-us/azure/aks/learn/quick-kubernetes-deploy-terraform?pivots=development-environment-azure-cli

How to Install Azure CLI on Windows:
     on powershell: winget install --id Microsoft.AzureCLI

Provide access to tenant and subscription of Azure via Azure cli:
    az login --scope https://graph.microsoft.com/.default

   Output: Select the account you want to log in with. For more information on login with Azure CLI, see https://go.microsoft.com/fwlink/?linkid=2271136

Retrieving tenants and subscriptions for the selection...

[Tenant and subscription selection]

No     Subscription name     Subscription ID                       Tenant
-----  --------------------  ------------------------------------  -----------------
[1] *  Azure subscription 1  9a881c5b-xxxx-4141-b050-XXXXXX  Default Directory

The default is marked with an *; the default tenant is 'Default Directory' and subscription is 'Azure subscription 1' (9a881c5b-ce93-4141-b050-4a6e4226ac1c).

Select a subscription and tenant (Type a number or Enter for no changes):     Click Enter
OutPut:
Tenant: Default Directory
Subscription: Azure subscription 1 (9a881c5b-xxxx-4141-b050-xxxxxx)

[Announcements]
With the new Azure CLI login experience, you can select the subscription you want to use more easily. Learn more about it and its configuration at https://go.microsoft.com/fwlink/?linkid=2271236

If you encounter any problem, please open an issue at https://aka.ms/azclibug

[Warning] The login output has been updated. Please be aware that it no longer displays the full list of available subscriptions by default.

==========================================================================

PS C:\WINDOWS\system32> az vm list-usage --location eastus --output table

Name                                      CurrentValue    Limit
----------------------------------------  --------------  -------
Availability Sets                         0               2500
Total Regional vCPUs                      0               4
Virtual Machines                          0               25000
Virtual Machine Scale Sets                0               2500
Dedicated vCPUs                           0               0
Cloud Services                            0               2500
Total Regional Low-priority vCPUs         0               3
Basic A Family vCPUs                      0               4
Standard A0-A7 Family vCPUs               0               4
Standard A8-A11 Family vCPUs              0               4

Azure CLI commands: 
    PS C:\WINDOWS\system32> az vm list-sizes --location southindia --output table

This command has been deprecated and will be removed in a future release. Use 'az vm list-skus' instead.

MaxDataDiskCount    MemoryInMB    Name                    NumberOfCores    OsDiskSizeInMB    ResourceDiskSizeInMB
------------------  ------------  ----------------------  ---------------  ----------------  ----------------------
4                   8192          Standard_D2a_v4         2                1047552           51200
8                   16384         Standard_D4a_v4         4                1047552           102400
16                  32768         Standard_D8a_v4         8                1047552           204800
32                  65536         Standard_D16a_v4        16               1047552           409600
32                  131072        Standard_D32a_v4        32               1047552           819200
32                  196608        Standard_D48a_v4        48               1047552           1228800
32                  262144        Standard_D64a_v4        64               1047552           1638400
32                  393216        Standard_D96a_v4        96               1047552           2457600
4                   8192          Standard_D2as_v4        2                1047552           16384
8                   16384         Standard_D4as_v4        4                1047552           32768
16                  32768         Standard_D8as_v4        8                1047552           65536
32                  65536         Standard_D16as_v4       16               1047552           131072
32                  131072        Standard_D32as_v4       32               1047552           262144
32                  196608        Standard_D48as_v4       48               1047552           393216

