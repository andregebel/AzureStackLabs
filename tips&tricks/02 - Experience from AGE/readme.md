Recently I learned, that [Microsoft Documentation](https://learn.microsoft.com/en-us/azure-stack/hci/concepts/firewall-requirements) is/was missing some Informations


## Management NIC - Deployment
Make sure there is only one management NIC with IP address (setup is complaining about multiple gateways)

## Network Adapters
Same network adapters in one intent (speed and type)

## RDMA
RDMA off for Compute_Management Intent in the settings. Almost no switch can do RDMA!

## Custom Loation
Custom Loation only underscore, numbers and letters

## The created switch must be used for the Logical Network!
https://learn.microsoft.com/de-de/azure/aks/hybrid/aks-networks?tabs=azureportal
