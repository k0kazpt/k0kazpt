# Azure Documentation
- [Azure Documentation](#azure-documentation)
  - [Architecture](#architecture)
    - [Considerations](#considerations)
## Architecture
### Considerations
- VMs:
  - No NSG's shall be attached directly to NIC's. All NSG's shall be controlled on the subnet level;
  - When created VM NIC's shall be attached to an Application Security Group, for use in NSG rules.
- Network:
  - Subnet depend on NSG's and routing tables (_in terraform: add them as submodule to subnet module?_);
  - NSG rules should be primarily based on Application Security Groups and not on IP's of VMs (_in terraform: submodule to vm module?_)


References:
- https://docs.microsoft.com/pt-pt/azure/virtual-network/network-security-groups-overview
- https://docs.microsoft.com/pt-pt/azure/virtual-network/application-security-groups