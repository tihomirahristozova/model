# Table Log_Shipment_Lines

Represents detail lines of shipments. Each line contains the shipment of one product. Entity: Log_Shipment_Lines

# Aggregate Hierarchy

* [Log_Shipments](Log_Shipments.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Shipment_Line_Id|`Guid`|`PK`, Readonly||
|Box_Count|`Int32?`||The count of boxes in which the goods are packaged. null means unknown. |
|Finished|`Boolean`|Readonly|True if this shipment should prohibit further shipments for the sales order line. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Gross_Weight_kg|`Decimal?`||The gross weight of the whole line in kilogramms. null means unknown. |
|Guarantee_Period_Days|`Int32?`||Guarantee period in days for the offered product. null for non-serviced products. |
|Height_m|`Decimal?`||The height of the package in meters. null means unknown. |
|Length_m|`Decimal?`||The length of the package in meters. null means unknown. |
|Line_No|`Int32`||Line number, unique for the shipment. `Required` |
|Line_Required_Delivery_Date|`DateTime?`||Required delivery date for this lines. Depending on the shipment route travel time, the shipment should be released accordingly. |
|Net_Weight_kg|`Decimal?`||The net weight of the entire batch of goods in kilograms. null means unknown. |
|Notes|`String`||Specific notes for this line. |
|Pallet_No|`Int32?`||The number of the pallet in which the goods are packaged. null means unknown. |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. `Filter(multi eq)` |
|Volume_l|`Decimal?`||The volume in litres of the whole batch. null means unknown. |
|Width_m|`Decimal?`||The width of the package in meters. null means unknown. |
