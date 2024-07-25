Recently I learned, that [Microsoft Documentation](https://learn.microsoft.com/en-us/azure-stack/hci/concepts/firewall-requirements) is/was missing some Informations


## Management NIC - Deployment
Make sure there is only one management NIC with IP address (setup is complaining about multiple gateways)


## Network Adapters
Same network adapters in one intent (speed and type)


## RDMA
RDMA off for Compute_Management Intent in the settings. Almost no switch can do RDMA!


## Custom Loation
Custom Loation only underscore, numbers and letters


## Bitlocker
Export yout Bitlocker keys!!!!
on one of the Nodes from the Cluster open a Powershell an execute
```PowerShell
Get-AsRecoveryKeyInfo | ft ComputerName, PasswordID, RecoveryKey
```
Example Output:
```PowerShell
 PS C:\Users\ashciuser> Get-AsRecoveryKeyInfo | ft ComputerName, PasswordID, RecoveryKey

 ComputerName    PasswordId    RecoveryKey
 -------         ----------    -----------
 ASB88RR1OU19    {Password1}   Key1
 ASB88RR1OU20    {Password2}   Key2
 ASB88RR1OU21    {Password3}   Key3
 ASB88RR1OU22    {Password4}   Key4
```

https://learn.microsoft.com/en-us/azure-stack/hci/manage/manage-bitlocker


## The created switch must be used for the Logical Network!
https://learn.microsoft.com/de-de/azure/aks/hybrid/aks-networks?tabs=azureportal
