# Table Crm_Sales_Person_Groups

Hierarchical sales person grouping. Entity: Crm_Sales_Person_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Person_Group_Id|`Guid`|`PK`, Readonly||
|Sales_Person_Group_Code|`String`||The unique code of the SalesPersonGroup. `Required` `Filter(eq;like)` `ORD` |
|Full_Path|`String`|Readonly|Full path to this item in the form /root/child1/../leaf/. `Filter(eq;like)` `ReadOnly` |
|Sales_Person_Group_Name|`String`||The name of this SalesPersonGroup. `Required` `Filter(eq;like)` |
