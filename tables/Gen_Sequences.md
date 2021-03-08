# Table Gen_Sequences

Provides numbering sequences, applicable for use in a multi-threaded environment. Entity: Gen_Sequences

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sequence_Id|`Guid`|`PK`, Readonly||
|Sequence_Name|`String`||The name of this Sequence. `Required` `Filter(like)` |
|Simultaneous_Transactions|`Boolean`||When false, specifies that the users will wait in a queue for a single numbering sequence generator. When true, the system will allow parallel numbering, by using any of the available sequence generators. However, parallel numbering has the drawback that, if no sequence generator is free, it will immediately throw exception, instead of waiting. So before setting to true, make sure that enough sequence generators are available. `Required` `Default(false)` |
