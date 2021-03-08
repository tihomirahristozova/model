# Table Inv_Cost_Corrections_Options

Options per document type for the cost corrections. Entity: Inv_Cost_Corrections_Options

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Corrections_Option_Id|`Guid`|`PK`, Readonly||
|Reset_Transactions_State_On_Releasing|`Boolean`||When true, the stock transactions state are re-set when the cost correction is released. The idea is to notify these documents, so that they have chance to re-generate their sub-documents. `Required` `Default(false)` `Filter(eq)` |
|Schedule_Document_Events|`Boolean`||Indicates wheather the document events caused by the cost correction should be scheduled for later procession. `Required` `Default(false)` |
