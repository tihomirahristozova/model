# Table Gen_Product_Types

Categorization of the products by their nature. Entity: Gen_Product_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Type_Id|`Guid`|`PK`, Readonly||
|Product_Type_Code|`String`||The unique code of the ProductType. `Required` `Filter(eq)` |
|Is_Default|`Boolean`||When checked specifies that this type is set by default for new products unless another type is specified in the product groups. `Required` `Default(false)` `Filter(eq)` |
|Is_Fixed_Asset|`Boolean`||True when assets are acquired or retired when products from this type are purchased or sold. `Required` `Default(false)` `Filter(eq)` |
|Is_Service_Activity_Service|`Boolean`||True when the product corresponds to service used in service documents (like service activities). `Required` `Default(false)` `Filter(eq)` |
|Is_Serviced|`Boolean`||True when the products of this type create service agreements and can be serviced. `Required` `Default(false)` `Filter(eq)` |
|Is_Shipped|`Boolean`||True when the products from this type are being shipped after sales. `Required` `Default(false)` `Filter(eq)` |
|Is_Stocked|`Boolean`||True=The products of this type are stocked in a warehouse; false=otherwise (services). `Required` `Default(true)` `Filter(eq)` |
|Lot_Auto_Creation|`Boolean`||If checked specifies that lots are automatically created by the receiving orders with which the products are received. `Required` `Default(false)` |
|Product_Type_Name|`MultilanguageString`||The name of this ProductType. `Required` `Filter(eq;like)` `ORD` |
