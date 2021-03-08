# Table Inv_Lots

Warehouse lots. They contain one row for each specific product, status, production batch and other specific warehousing conditions. Lot status can block certain operations. Entity: Inv_Lots

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Lot_Id|`Guid`|`PK`, Readonly||
|Description|`MultilanguageString`||The description of this Lot. |
|Expiry_Date|`DateTime?`||Expiry date for this lot. |
|License_No|`String`||The license number for this lot. Null when license number is N/A or unknown. |
|Lot_Number|`String`||The unique number of the Lot. May contain characters, if required. `Required` `Filter(eq;like)` |
|Production_Batch_Id|`Guid?`||Non-null if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods. `Filter(multi eq)` |
|Purchase_Lot_Number|`String`||Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order. `Filter(like)` |
|Receipt_Date|`DateTime?`|Readonly|The date of the first receipt of products in this lot. `ReadOnly` |
|Status|`Status`|Allowed: `0`, `-3`, `-2`, `-1`|Status of the warehouse lot. Minus statuses describe blocked conditions. -3 blocked for document (sales or service order) -2 blocked for party -1 blocked for inspection 0 free to use. `Required` `Default(0)` `Filter(multi eq)` |
