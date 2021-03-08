# Table Log_Transportation_Execution_Lines

Contains details of executions of transportation order lines. Entity: Log_Transportation_Execution_Lines (Introduced in version 18.2)

# Aggregate Hierarchy

* [Log_Transportation_Executions](Log_Transportation_Executions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transportation_Execution_Line_Id|`Guid`|`PK`, Readonly||
|Execution_Date|`DateTime`||The date when the operation was executed. `Required` |
|Execution_Time|`TimeSpan`||The time when the operation was executed. `Required` |
|Line_No|`Int32`||Consecutive line number within this execution. `Required` |
|Notes|`String`||Notes for this TransportationExecutionLine. |
|Operation_Type|`OperationType`|Allowed: `L`, `U`, `O`|The type of operation being executed. L=Loading; U=Unloading; O=Other. `Required` |
|Pallet_Number|`String`||Pallet number, when applicable. null when unknown or not applicable. |
|Pallets_Count|`Int32?`||Number of pallets affected by this operation. null when unknown or N/A. |
|Volume_Cbm|`Int32?`||Cargo volume in cubic meters, affected by this operation. null when unknown or N/A. |
|Weight_Kg|`Int32?`||Cargo weight in kg, affected by this operation. null when unknown or N/A. |
