# Table Crm_Customer_Types

User defined customer type. Primarily used for customer definition security, because it has record level security, which is also applied to the individual customer definitions. Entity: Crm_Customer_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Customer_Type_Id|`Guid`|`PK`, Readonly||
|Customer_Type_Name|`MultilanguageString`||The name of this CustomerType. `Required` `Filter(eq;like)` |
