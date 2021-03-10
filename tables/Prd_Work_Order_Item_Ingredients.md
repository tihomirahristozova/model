# Table Prd_Work_Order_Item_Ingredients

The materials consumed in the production order operations. Entity: Prd_Work_Order_Item_Ingredients

## Owner Tables Hierarchy

* [Prd_Work_Orders](Prd_Work_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |The order of the line within the item.|
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item for which the materials in this line are used. If NULL means that the materials are distributed amongst all work order items in the document.|
|[Material_Id](#material_id)|`uniqueidentifier` |The Id of the consumed material (Gen_Products_Table)|
|[Used_Quantity](#used_quantity)|`decimal(18, 3)` |The quantity of the material consumed in the operation|
|[Used_Quantity_Unit_Id](#used_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity of the material consumed in the operation|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which to retrieve the material.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Id](#id)|`uniqueidentifier` `PK`|The Id of the production order operation|
|[Row_Version](#row_version)|`timestamp` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |If not NULL, specifies the serial number of the ingredient|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Selects the product thru some of the product codes.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |Lot from which to get the material. When NULL, any lot can be used.|
|[Used_Quantity_Base](#used_quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Used Quantity in the base measurement category of the material.|
|[Operation_Id](#operation_id)|`uniqueidentifier` |Specifies for which operation this ingredient is used|
|[Distribute_By](#distribute_by)|`nvarchar(2)` Allowed: `SP`, `MC`, `SC`|Distribution method in case the materials from the line are distributed amongst all work order items. Should be NOT NULL iif Work_Order_Item_Id is NULL. MC=Measurement, SP=Standard_Price|
|[Principal_Recipe_Ingredient_Id](#principal_recipe_ingredient_id)|`uniqueidentifier` |The principal recipe ingredient on which this record is based.|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin from which to take the ingredients|
|[Fixed_Scrap_Quantity](#fixed_scrap_quantity)|`decimal(18, 3)` |The quantity of the material, which will be used for setup.|
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` ||
|[Distribute_By_Measurement_Category_Id](#distribute_by_measurement_category_id)|`uniqueidentifier` |Measurement category by which the materials from the line are distributed amongst all work order items in case Distribute_By = MC. Should be NOT NULL iif Distribute_By = MC.|
|[Used_Standard_Quantity_Base](#used_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Used Quantity Base.|

## Columns

### Line_Ord


Line_Ord


The order of the line within the item.


The order of the line within the item.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|10|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Line_Ord](Prd_Work_Order_Item_Ingredients.md#line_ord)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|yes|

### Work_Order_Item_Id


Work_Order_Item_Id


The work order item for which the materials in this line are used. If NULL means that the materials are distributed amongst all work order items in the document.


The work order item for which the materials in this line are used. If NULL means that the materials are distributed amongst all work order items in the document.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Work_Order_Items](Prd_Work_Order_Items.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Work_Order_Item_Id](Prd_Work_Order_Item_Ingredients.md#work_order_item_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Material_Id


Material_Id


The Id of the consumed material (Gen_Products_Table)


The Id of the consumed material (Gen_Products_Table)

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Material_Id](Prd_Work_Order_Item_Ingredients.md#material_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Used_Quantity


Used_Quantity


The quantity of the material consumed in the operation


The quantity of the material consumed in the operation

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Used_Quantity](Prd_Work_Order_Item_Ingredients.md#used_quantity)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Used_Quantity_Unit_Id


Used_Quantity_Unit_Id


The measurement unit of the quantity of the material consumed in the operation


The measurement unit of the quantity of the material consumed in the operation

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Used_Quantity_Unit_Id](Prd_Work_Order_Item_Ingredients.md#used_quantity_unit_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Store_Id


Store_Id


The store from which to retrieve the material.


The store from which to retrieve the material.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Store_Id](Prd_Work_Order_Item_Ingredients.md#store_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Notes](Prd_Work_Order_Item_Ingredients.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|254|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Id


Id


The Id of the production order operation


The Id of the production order operation

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Id](Prd_Work_Order_Item_Ingredients.md#id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Row_Version](Prd_Work_Order_Item_Ingredients.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Serial_Number_Id


Serial_Number_Id


If not NULL, specifies the serial number of the ingredient


If not NULL, specifies the serial number of the ingredient

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Serial_Numbers](Inv_Serial_Numbers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Serial_Number_Id](Prd_Work_Order_Item_Ingredients.md#serial_number_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Product_Code_Id


Product_Code_Id


Selects the product thru some of the product codes.


Selects the product thru some of the product codes.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Codes](Gen_Product_Codes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Product_Code_Id](Prd_Work_Order_Item_Ingredients.md#product_code_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Lot_Id


Lot_Id


Lot from which to get the material. When NULL, any lot can be used.


Lot from which to get the material. When NULL, any lot can be used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Lots](Inv_Lots.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Lot_Id](Prd_Work_Order_Item_Ingredients.md#lot_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Used_Quantity_Base


Used_Quantity_Base


The equivalence of Used Quantity in the base measurement category of the material.


The equivalence of Used Quantity in the base measurement category of the material.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Used_Quantity_Base](Prd_Work_Order_Item_Ingredients.md#used_quantity_base)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Operation_Id


Operation_Id


Specifies for which operation this ingredient is used


Specifies for which operation this ingredient is used

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Operations](Prd_Operations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Operation_Id](Prd_Work_Order_Item_Ingredients.md#operation_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Distribute_By


Distribute_By


Distribution method in case the materials from the line are distributed amongst all work order items. Should be NOT NULL iif Work_Order_Item_Id is NULL. MC=Measurement, SP=Standard_Price


Distribution method in case the materials from the line are distributed amongst all work order items. Should be NOT NULL iif Work_Order_Item_Id is NULL. MC=Measurement, SP=Standard_Price

| Property | Value |
| - | - |
|Type|nvarchar(2)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`SP`, `MC`, `SC`|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Distribute_By](Prd_Work_Order_Item_Ingredients.md#distribute_by)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|2|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Principal_Recipe_Ingredient_Id


Principal_Recipe_Ingredient_Id


The principal recipe ingredient on which this record is based.


The principal recipe ingredient on which this record is based.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Principal_Recipe_Ingredient_Id](Prd_Work_Order_Item_Ingredients.md#principal_recipe_ingredient_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Store_Bin_Id


Store_Bin_Id


The store bin from which to take the ingredients


The store bin from which to take the ingredients

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Store_Bins](Inv_Store_Bins.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Store_Bin_Id](Prd_Work_Order_Item_Ingredients.md#store_bin_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Fixed_Scrap_Quantity


Fixed_Scrap_Quantity


The quantity of the material, which will be used for setup.


The quantity of the material, which will be used for setup.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Fixed_Scrap_Quantity](Prd_Work_Order_Item_Ingredients.md#fixed_scrap_quantity)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Work_Order_Id


Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Work_Orders](Prd_Work_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Work_Order_Id](Prd_Work_Order_Item_Ingredients.md#work_order_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Distribute_By_Measurement_Category_Id


Distribute_By_Measurement_Category_Id


Measurement category by which the materials from the line are distributed amongst all work order items in case Distribute_By = MC. Should be NOT NULL iif Distribute_By = MC.


Measurement category by which the materials from the line are distributed amongst all work order items in case Distribute_By = MC. Should be NOT NULL iif Distribute_By = MC.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Categories](Gen_Measurement_Categories.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Distribute_By_Measurement_Category_Id](Prd_Work_Order_Item_Ingredients.md#distribute_by_measurement_category_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Used_Standard_Quantity_Base


Used_Standard_Quantity_Base


The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Used Quantity Base.


The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Used Quantity Base.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md).[Used_Standard_Quantity_Base](Prd_Work_Order_Item_Ingredients.md#used_standard_quantity_base)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


