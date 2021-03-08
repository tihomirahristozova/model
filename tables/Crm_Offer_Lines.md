# Table Crm_Offer_Lines

Detail records (lines) of Offers. Entity: Crm_Offer_Lines

# Aggregate Hierarchy

* [Crm_Offers](Crm_Offers.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Offer_Line_Id|`Guid`|`PK`, Readonly||
|Choice_Group_Name|`String`||Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group. |
|Delivery_Term_Days|`Int32`||Delivery term in days. When Required Delivery Date is specified (not null), it takes precedence and this is ignored. `Required` `Default(0)` |
|Guarantee_Period_Days|`Int32?`||Guarantee period in days for the offered product. null for non-serviced products. |
|Is_Selected|`Boolean`||True when the line is selected for further processing (ordering), false otherwise. `Required` `Default(true)` |
|Line_Custom_Discount_Percent|`Decimal`||Operator defined discount percentage, specified for this line. `Required` `Default(0)` |
|Line_No|`Int32`||Line number, unique within the Offer. Usually is increasing number like 10, 20, 30, ... when initially entering the Offer (in order to allow insertions with adjustment documents). `Required` |
|Line_Standard_Discount_Percent|`Decimal`||The discount percentage, applied through the standard discount policy. `Required` `Default(0)` |
|Notes|`String`||Notes for this OfferLine. |
|Product_Description|`MultilanguageString`||The description of the offered product. Initially copied from the name of the offered product. `Required` `Filter(like)` |
|Required_Delivery_Date|`DateTime?`||Date, when the delivery is required. Alternative to Delivery Term Days. When null, Delivery Term Days is used. |
|Variant|`String`||Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together. |
