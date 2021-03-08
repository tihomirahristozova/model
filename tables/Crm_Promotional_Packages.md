# Table Crm_Promotional_Packages

Promotional packages are packages of products, which are sold together at a special pricing and discount conditions. Entity: Crm_Promotional_Packages

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Promotional_Package_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||Package status: true = the offer is available for new documents; false = otherwise. `Required` `Default(true)` `Filter(eq)` |
|Promotional_Package_Code|`String`||Unique code of the promotional package. `Required` `Filter(eq;like)` `ORD` |
|Promotional_Package_Name|`String`||The name of this PromotionalPackage. `Required` `Filter(eq;like)` `ORD` |
|Valid_For_Customer_Filter_XML|`DataAccessFilter`||When not null, the package is valid only for the customers, that match the filter. |
|Valid_For_Distribution_Channel_Filter_XML|`DataAccessFilter`||When not null, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria. |
|Valid_For_Ship_To_Customer_Filter_XML|`DataAccessFilter`||When not null, specifies validity condition for the Ship To Customer of the sales document. |
|Valid_From_Date|`DateTime?`||When not null specifies the first date when the package is valid for offering. The date is compared against the document date. `Filter(eq;ge;le)` |
|Valid_To_Date|`DateTime?`||When not null specifies the last date (inclusive) when the package is valid. The date is compared against the document date. `Filter(eq;ge;le)` |
