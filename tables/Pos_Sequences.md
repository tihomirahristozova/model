# Table Pos_Sequences

Stores the last issued fiscal sales number for each POS device. Entity: Pos_Sequences (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pos_Sequence_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Indicates whether this sequence is active. `Required` `Default(true)` `Filter(multi eq)` |
|Max_No|`String`||Specifies the maximum number allowed in the sequence. null means that the sequence will grow unlimited. `Filter(multi eq;ge;le)` |
|Next_No|`String`||The next consecutive number which will be assigned on the next request. `Required` `Filter(multi eq;ge;le)` |
