# Table Gen_Document_Fulfillments

Fulfillment ledger for documents. Entity: Gen_Document_Fulfillments (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Fulfillment_Id|`Guid`|`PK`, Readonly||
|Creation_Time_Utc|`DateTime`||The exact time in UTC, when the fulfillment was created in the system. `Required` `Default(NowUtc)` `Filter(multi eq;ge;le)` |
|Document_Line_Id|`Guid`||The Id of the fulfilled line within the document. The attribute contains the Id and is not a reference, because it references different entities depending on document entity type and line type. `Required` `Filter(multi eq)` |
|Fulfillment_Type|`FulfillmentType`|Allowed: `P`, `C`|Type of fulfillment: P=Planned; C=Completed. `Required` `Filter(multi eq)` `Introduced in version 21.1.1.26` |
|Is_Final|`Boolean`||Specifies whether this fulfillment finalizes the line, regardless of any remaining quantities. `Required` `Filter(eq)` |
|Line_No|`Int32?`||Line number. Used for human-readability of the fulfillment. null if the lines do not support line numbers or the line number is unknown. `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.26` |
|Line_Type|`String`||Detail (line) type, for example materials, services, etc. L=Line. Other values are defined by the document entity type. `Required` `Default("L")` `Filter(multi eq)` `Introduced in version 21.1.1.26` |
|Quantity_Base|`Decimal`||Fulfilled quantity in the base measurement unit of the product. `Required` `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.33` |
