# Table Crm_Campaigns

Marketing campaigns. Used to treat target groups with marketing messages, plan budgets and marketing activities. Entity: Crm_Campaigns

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Campaign_Id|`Guid`|`PK`, Readonly||
|Description|`String`||Campaign description. |
|End_Date|`DateTime?`||End date of the campaign. null means that the end date is still unknown. |
|Forecasted_Cost|`Decimal`||Forecasted total cost of the campaign. `Required` `Default(0)` |
|Campaign_Name|`String`||Short name of the campaign. `Required` `Filter(like)` `ORD` |
|Start_Date|`DateTime`||Starting date of the campaign. `Required` `Default(Today)` |
