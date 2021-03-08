# Table Bpm_Process_Node_Events

Abstract root of all process node events. Currently - not used. Entity: Bpm_Process_Node_Events

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Node_Event_Id|`Guid`|`PK`, Readonly||
|Boundary_Of_Process_Node_Id|`Guid?`||When the event is boundary, contains the node to which the event is bound. Otherwise contains null. `Filter(multi eq)` |
|Event_Key|`String`||The unique event key, which is thrown or caught. `Required` |
|Event_Type|`String`||Event type. S=Start, T=Intermediate Throw, C=Intermediate Catch, B=Boundary, E=End. `Required` |
|Is_Cancel|`Boolean`||True if this is cancel event. `Required` |
|Is_Compensation|`Boolean`||True if this is compensation event. `Required` |
|Is_Error|`Boolean`||True if this is error event. `Required` |
|Is_Escalation|`Boolean`||True if this is escalation event. `Required` |
|Is_Message|`Boolean`||True if this is message event. `Required` |
|Is_Signal|`Boolean`||True if this is signal event. `Required` |
|Is_Timer|`Boolean`||True if this is timer event. `Required` |
|Process_Node_Id|`Guid`||The node of this node event. `Required` `Filter(multi eq)` |
