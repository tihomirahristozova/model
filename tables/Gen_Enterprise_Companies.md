# Table Gen_Enterprise_Companies

The companies in the enterprise that issue documents. Entity: Gen_Enterprise_Companies

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Enterprise_Company_Id|`Guid`|`PK`, Readonly||
|BI_Start_Date|`DateTime?`||Defines the period for which BI extracts data. BI includes documents with "Document Date" greater than or equal to "BI Start Date". `Filter(eq)` `Introduced in version 18.2` |
|Default_Costing_Method|`DefaultCostingMethod`|Allowed: `AVG`, `EXP`, `BLD`|Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost. `Required` `Default("AVG")` |
|Default_Language|`DefaultLanguage?`|Allowed: `bg`, `en`|The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...). `Default("en")` |
|Edit_Period_Start_Date|`DateTime?`||Start date of the priod when the documents can be edited. |
|Is_Active|`Boolean`||Indicates whether the current Enterprise company  is active. `Required` `Default(true)` `Filter(multi eq)` `Introduced in version 20.1` |
|Print_Images_Retention_Months|`Int32`||A period of months for which the printed images of the documents will be kept. `Required` `Default(60)` `Filter(multi eq;ge;le)` `Introduced in version 20.1` |
|UI_Base_Color|`Int32?`||When not null, specifies the background color to use for visualization of the UI when the current enterprise company is selected. The color is in RGBA color format. `Introduced in version 18.2` |
