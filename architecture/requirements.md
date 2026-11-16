
# Enterprise Architecture Requirements

## Organization
Northstar Professional Services Inc.

## Business Profile
- Country: Canada
- Headquarters: Toronto, Ontario
- Employees: 50
- IT Administrators: 3
- Infrastructure: Microsoft Azure

## Business Requirements

1. Centralized identity management.
2. Secure cloud networking.
3. Windows Server infrastructure.
4. Segmented network architecture.
5. Role-based access management.
6. Secure application and data access.
7. Infrastructure monitoring.
8. Backup and disaster recovery.
9. Administrative automation.
10. Cost governance.

## Network Design

Azure Region: Canada Central

Virtual Network: vnet-northstar-prod

Address Space: 10.10.0.0/16

Subnets:

| Subnet | Address Range |
|---|---|
| Management | 10.10.1.0/24 |
| Servers | 10.10.2.0/24 |
| Applications | 10.10.3.0/24 |

## Security Requirements

- Least privilege access.
- Network Security Groups.
- Restricted administrative access.
- Secure storage.
- Centralized monitoring.
- Backup and recovery validation.

## Deployment Principles

- Deploy resources from scratch.
- Use consistent naming conventions.
- Apply cost controls.
- Document implementation decisions.
- Validate every deployment.
