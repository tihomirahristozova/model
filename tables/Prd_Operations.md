# Table Prd_Operations

The different steps performed to create products. Entity: Prd_Operations

# Aggregate Hierarchy

* [Prd_Operation_Groups](Prd_Operation_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this Operation. |
|Minimum_Concurrent_Start_Time_Minutes|`Int32?`||How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting. |
|Move_Time_Minutes|`Int32`||The time required for the product to move to the next operation. During this time no resource is allocated. `Required` `Default(0)` |
|Operation_Name|`String`||The name of this Operation. `Required` `Filter(like)` |
|Run_Time_Minutes|`Int32`||The time required to process one product lot. The run time is calculated for each produced lot. `Required` `Default(0)` |
|Scrap_Rate|`Decimal?`||The percentage (0..1) of scrap usually occurring during the production operation. null means that the scrap rate cannot be generally calculated. |
|Setup_Time_Minutes|`Int32`||The time required to setup the operation. The setup is incurred only once, regardless of the produced quntity. `Required` `Default(0)` |
|Standard_Price_Per_Hour|`Decimal`||Standard price for 1 hour work for this operation. `Required` `Default(0)` |
|Tooling|`String`||Short description of the needed instruments for the operation. |
|Wait_Time_Minutes|`Int32`||The time required to wait after completing the operation. During this time, the resource is still allocated to the operation. `Required` `Default(0)` |
