# Table Rent_Transaction_Templates

Specifies additional options for document routes, generating Rental Transactions. Entity: Rent_Transaction_Templates

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Rent_Transaction_Template_Id|`Guid`|`PK`, Readonly||
|Transaction_Type|`TransactionType`|Allowed: `D`, `R`, `W`, `S`|Transaction type for the rent transaction that is to be created. `Required` |
