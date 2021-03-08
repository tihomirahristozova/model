# Table Scm_Requisition_Lines

Detail lines of Requistions. Entity: Scm_Requisition_Lines

# Aggregate Hierarchy

* [Scm_Requisitions](Scm_Requisitions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Requisition_Line_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Line number, unique within the Requisition. Usually is increasing number like 10, 20, 30, ... when initially entering the Requisition (in order to allow insertions with adjustment documents). `Required` |
|Notes|`String`||Notes for this RequisitionLine. |
|Product_Description|`MultilanguageString`||The description of the required product. When Product is set, this is copied initially from the product name. When Product is null, this contains the manually entered description of the desired product. |
|Required_Delivery_Date|`DateTime`||The desired delivery date. Initially set to the required delivery date in the requisition header or if it is empty - to the document date plus the products lead time. `Required` `Filter(ge;le)` |
