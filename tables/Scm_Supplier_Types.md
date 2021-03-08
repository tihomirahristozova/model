# Table Scm_Supplier_Types

Supplier types are primarily used to differentiate the security level access to the different supplier groups. Entity: Scm_Supplier_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Supplier_Type_Id|`Guid`|`PK`, Readonly||
|Supplier_Type_Name|`String`||The name of this SupplierType. `Required` `Filter(eq;like)` |
