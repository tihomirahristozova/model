# Table Ast_Assets

The fixed assets. Entity: Ast_Assets

# Aggregate Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Asset_Id|`Guid`|`PK`, Readonly||
|Asset_Code|`String`||The unique code of the Asset. `Required` `Filter(eq;like)` `ORD` |
|Deployment_Date|`DateTime?`||Date, when the asset is first deployed. Null if the asset is not deployed yet. |
|Is_Active|`Boolean`||Checked if the assets is active and can be used in documents. The inactive assets can be used only for reports. `Required` `Default(true)` `Filter(eq)` |
|Asset_Name|`MultilanguageString`||The name of this Asset. `Required` `Filter(like)` |
|Notes|`String`||Notes for this Asset. |
|Purchase_Date|`DateTime`||Original purchase date of the asset. `Required` |
|Serial_Number|`String`||Serial number of the asset. `Filter(eq)` |
