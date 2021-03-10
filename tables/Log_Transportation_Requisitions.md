# Table Log_Transportation_Requisitions

Client requisition for transportation. Entity: Log_Transportation_Requisitions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Requisition_Id](#transportation_requisition_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Requested_Departure_Date](#requested_departure_date)|`date` |Requested date of departure. NULL when no specific date is requested.|
|[Requested_Departure_Time](#requested_departure_time)|`time` |Requested time of departure. NULL when no specific time is requested.|
|[Requested_Arrival_Date](#requested_arrival_date)|`date` |Requested arrival date. NULL when no specific date is requested.|
|[Requested_Arrival_Time](#requested_arrival_time)|`time` |Requested arrival time. NULL when no specific time is requested.|
|[Transport_From_Party_Id](#transport_from_party_id)|`uniqueidentifier` |Shipping party.|
|[Transport_From_Party_Contact_Mechanism_Id](#transport_from_party_contact_mechanism_id)|`uniqueidentifier` |Loading address.|
|[Transport_From_Geo_Point_Id](#transport_from_geo_point_id)|`uniqueidentifier` |Geographical location of the loading, if available.|
|[Transport_To_Party_Id](#transport_to_party_id)|`uniqueidentifier` |Receiving party.|
|[Transport_To_Party_Contact_Mechanism_Id](#transport_to_party_contact_mechanism_id)|`uniqueidentifier` |Unload address.|
|[Transport_To_Geo_Point_Id](#transport_to_geo_point_id)|`uniqueidentifier` |Geographical location of the unloading, if available.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transportation_Requisition_Id


Transportation_Requisition_Id

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
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Transportation_Requisition_Id](Log_Transportation_Requisitions.md#transportation_requisition_id)|
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
|Equals|NULL|no|no|

### Document_Id


Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Document_Id](Log_Transportation_Requisitions.md#document_id)|
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
|Equals|NULL|no|no|

### Requested_Departure_Date


Requested_Departure_Date


Requested date of departure. NULL when no specific date is requested.


Requested date of departure. NULL when no specific date is requested.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Requested_Departure_Date](Log_Transportation_Requisitions.md#requested_departure_date)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Requested_Departure_Time


Requested_Departure_Time


Requested time of departure. NULL when no specific time is requested.


Requested time of departure. NULL when no specific time is requested.

| Property | Value |
| - | - |
|Type|time|
|DateTime Format|Time|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Requested_Departure_Time](Log_Transportation_Requisitions.md#requested_departure_time)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Requested_Arrival_Date


Requested_Arrival_Date


Requested arrival date. NULL when no specific date is requested.


Requested arrival date. NULL when no specific date is requested.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Requested_Arrival_Date](Log_Transportation_Requisitions.md#requested_arrival_date)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Requested_Arrival_Time


Requested_Arrival_Time


Requested arrival time. NULL when no specific time is requested.


Requested arrival time. NULL when no specific time is requested.

| Property | Value |
| - | - |
|Type|time|
|DateTime Format|Time|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Requested_Arrival_Time](Log_Transportation_Requisitions.md#requested_arrival_time)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Transport_From_Party_Id


Transport_From_Party_Id


Shipping party.


Shipping party.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Transport_From_Party_Id](Log_Transportation_Requisitions.md#transport_from_party_id)|
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
|Equals|NULL|no|no|

### Transport_From_Party_Contact_Mechanism_Id


Transport_From_Party_Contact_Mechanism_Id


Loading address.


Loading address.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Transport_From_Party_Contact_Mechanism_Id](Log_Transportation_Requisitions.md#transport_from_party_contact_mechanism_id)|
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
|Equals|NULL|no|no|

### Transport_From_Geo_Point_Id


Transport_From_Geo_Point_Id


Geographical location of the loading, if available.


Geographical location of the loading, if available.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Geo_Points](Gen_Geo_Points.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Transport_From_Geo_Point_Id](Log_Transportation_Requisitions.md#transport_from_geo_point_id)|
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

### Transport_To_Party_Id


Transport_To_Party_Id


Receiving party.


Receiving party.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Transport_To_Party_Id](Log_Transportation_Requisitions.md#transport_to_party_id)|
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
|Equals|NULL|no|no|

### Transport_To_Party_Contact_Mechanism_Id


Transport_To_Party_Contact_Mechanism_Id


Unload address.


Unload address.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Transport_To_Party_Contact_Mechanism_Id](Log_Transportation_Requisitions.md#transport_to_party_contact_mechanism_id)|
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
|Equals|NULL|no|no|

### Transport_To_Geo_Point_Id


Transport_To_Geo_Point_Id


Geographical location of the unloading, if available.


Geographical location of the unloading, if available.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Geo_Points](Gen_Geo_Points.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Transport_To_Geo_Point_Id](Log_Transportation_Requisitions.md#transport_to_geo_point_id)|
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
|Derived From|[Log_Transportation_Requisitions](Log_Transportation_Requisitions.md).[Row_Version](Log_Transportation_Requisitions.md#row_version)|
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


