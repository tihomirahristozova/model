# Table Log_Shipments

Represents shipments of sales orders to customers. Entity: Log_Shipments

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Shipment_Id](#shipment_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Ship_To_Party_Contact_Mechanism_Id](#ship_to_party_contact_mechanism_id)|`uniqueidentifier` |Destination address where the goods should be shipped|
|[Required_Delivery_Date](#required_delivery_date)|`datetime` |Required delivery date. Depending on the shipment route travel time, the shipment should be released accordingly. When NULL means that the required delivery date is unknown or the document contains many required delivery dates (e.g. in the lines)|
|[Ship_From_Store_Id](#ship_from_store_id)|`uniqueidentifier` |The store from which the shipment should be effected|
|[Issued_By_Person_Id](#issued_by_person_id)|`uniqueidentifier` |The person who signed for the shipment|
|[Received_By_Person_Id](#received_by_person_id)|`uniqueidentifier` |The person who received the goods for/from the shipment |
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Shipment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Ship_From_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Issued_By_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Received_By_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


