# Agent Performance

The bottlenecks are in LLM and calling MCP tools.

## 1. Data Warehouse
### 1.1 SAP
```text
                      User
                       │
                       ▼
                  Tool Discovery
                       │
                "sales order history"
                       │
                       ▼
             ┌────────────────────┐
             │ Relevant MCP tools │
             ├────────────────────┤
             │ get_sales_orders   │
             │ get_order_items    │
             │ get_customer       │
             └─────────┬──────────┘
                       │
                       ▼
                      LLM
                       │
                       ▼
              get_sales_orders()
                       │
                       ▼
                  MCP Server
                       │
                       ▼
                  OData API
                       │
                       ▼
                    S/4HANA

```
Odata services are very slow.

```text

OData $metadata
       │
       ▼
Metadata parser
       │
       ├── Entity
       ├── Properties
       ├── Relationships
       └── Operations
       │
       ▼
Semantic tool registry
       │
       ▼
MCP tools(CAP)
```
OData Entity:

```text
A_SalesOrder

Properties:
    SalesOrder
    SoldToParty
    SalesOrganization
    CreationDate
    TotalNetAmount
```

### 1.2 Databricks

UC is much better.
[Link](https://learn.microsoft.com/en-us/azure/databricks/agents/custom-agents/create-custom-tool#:~:text=Databricks%20recommends%20using%20Unity%20Catalog%20functions%20as,per-user%20authentication%20support%2C%20and%20additional%20flexibility.%20Requirements.)

## 2. Database

To be tested...

