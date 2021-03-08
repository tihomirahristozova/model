# Table Ast_Valuation_Models

Valuation models stand for the different valuations an asset can have. For example Accounting, Tax, External Financial Reports, etc. All asset transactions are posted for specific valuation model, but are usually automatically copied to other models. Entity: Ast_Valuation_Models

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Valuation_Model_Id|`Guid`|`PK`, Readonly||
|Is_System|`Boolean`|Readonly|Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Valuation_Model_Name|`MultilanguageString`||The name of this ValuationModel. `Required` `Filter(like)` |
