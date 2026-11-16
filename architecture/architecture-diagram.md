
# Azure Enterprise Architecture

## Planned Infrastructure Architecture

This diagram represents the proposed Azure infrastructure
for Northstar Professional Services Inc.

```mermaid
flowchart TB
    Internet((Internet))

    subgraph Azure["Microsoft Azure - Canada Central"]
        subgraph VNet["vnet-northstar-prod - 10.10.0.0/16"]

            subgraph Management["Management Subnet - 10.10.1.0/24"]
                Admin["Management VM"]
            end

            subgraph Servers["Servers Subnet - 10.10.2.0/24"]
                DC["Windows Server - AD DS / DNS"]
            end

            subgraph Applications["Applications Subnet - 10.10.3.0/24"]
                APP["Application Workload"]
            end
        end

        Identity["Microsoft Entra ID"]
        Monitor["Azure Monitor / Log Analytics"]
        Backup["Azure Backup"]
        Security["Network Security Groups"]
    end

    Internet --> VNet
    Admin --> DC
    DC --> APP
    Identity -.-> Admin
    Identity -.-> DC
    Security -.-> VNet
    Admin --> Monitor
    DC --> Monitor
    APP --> Monitor
    DC --> Backup
    APP --> Backup
```

## Architecture Components

| Component | Purpose |
|---|---|
| Virtual Network | Private cloud networking |
| Management Subnet | Administrative workloads |
| Servers Subnet | Windows Server infrastructure |
| Applications Subnet | Application workloads |
| Entra ID | Identity management |
| NSGs | Network traffic filtering |
| Azure Monitor | Monitoring and logging |
| Azure Backup | Data protection |

**Status:** Proposed architecture - not yet deployed.
