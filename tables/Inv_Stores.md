# Table Inv_Stores

Represents the physical warehouses. Entity: Inv_Stores

# Inheritance

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Store_Code|`String`||The unique code of the Store. `Required` `Filter(eq;like)` `ORD` |
|Creation_Time|`DateTime?`|Readonly|Date and time when the Store was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Store. `Filter(like)` `ReadOnly` |
|Default_Supply_Store_Id|`Guid?`||The store from which goods are usually supplied to this store. `Filter(multi eq)` |
|GLN|`String`|||
|Is_Active|`Boolean`|||
|Store_Name|`MultilanguageString`||Name of the store. `Required` `Filter(like)` |
|Number_Of_Dimensions|`Int32`||Number of dimensions in the coordinate system of the storage bins. 0 means single-bin store. Currently, this is only stored for information and is not used for automatical generation of store bins, as it was intended. `Required` `Default(0)` `Filter(eq)` |
|Party_Code|`String`|Readonly||
|Creation_Time|`DateTime?`|Readonly||
|Creation_User|`String`|Readonly||
|Party_Name|`MultilanguageString`|||
|Notes|`String`|||
|Party_Type|`PartyType`|Allowed: `C`, `L`, `P`, `S`, `V`||
|Party_Unique_Number|`String`|Readonly||
|Update_Time|`DateTime?`|Readonly||
|Update_User|`String`|Readonly||
|Schema_XML|`String`||Obsolete. Not used. |
|Unmanaged|`Boolean`||If false the system will expect the user to process the store transactions. If true the system will auto-generate them. `Required` `Default(true)` |
|Update_Time|`DateTime?`|Readonly|Date and time when the Store was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Store. `Filter(like)` `ReadOnly` |
