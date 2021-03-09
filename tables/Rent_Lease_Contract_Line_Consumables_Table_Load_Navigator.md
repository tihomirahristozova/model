# Query Rent_Lease_Contract_Line_Consumables_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Lease_Line_Consumable_Id](#lease_line_consumable_id)|`uniqueidentifier` `PK`||
|[Lease_Line_Id](#lease_line_id)|`uniqueidentifier` |Lease line with which the current consumable is given.|
|[Product_Id](#product_id)|`uniqueidentifier` |The consumable to be sold accompanying the asset.|
|[Consumable_Quantity](#consumable_quantity)|`decimal(12, 3)` |The quantity sold of the consumable.|
|[Consumable_Quantity_Unit_Id](#consumable_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Consumable Quantity.|
|[Store_Id](#store_id)|`uniqueidentifier` |Store from which the consumable is issued.|
|[Line_No](#line_no)|`int` |Consecutive number of the consumable within the lease contract line.|
|[Lease_Contract_Id](#lease_contract_id)|`uniqueidentifier` ||
|[Rental_Asset_Id](#rental_asset_id)|`uniqueidentifier` |The asset which is rented with the current contract.|
|[Start_Date](#start_date)|`date` |Starting date of lease for this asset|
|[End_Date](#end_date)|`date` |Ending date of lease of this asset|
|[Line_Notes](#line_notes)|`nvarchar` |Notes for this line.|
|[Guarantee_Amount](#guarantee_amount)|`decimal(0, 0)` ||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Lessee_Customer_Id](#lessee_customer_id)|`uniqueidentifier` |The customer record of the lessee|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the lease contract amounts|
|[Credit_Limit_Override](#credit_limit_override)|`bit` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[From_Party_Id](#from_party_id)|`uniqueidentifier` |The party which issued the document|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company which issued the document|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.|
|[Document_No](#document_no)|`nvarchar` |Document number, unique within Document_Type_Id|
|[Document_Date](#document_date)|`date` |The date on which the document was issued|
|[Reference_Date](#reference_date)|`datetime` |The date to which this document refers, i.e. when the action really occurred. If NULL, Document_Date is taken|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.|
|[Void](#void)|`bit` Readonly|1 if the document is null and void|
|[To_Party_Id](#to_party_id)|`uniqueidentifier` |The party which should receive the document|
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` |The currency directory, containing all the convertion rates, used by the document. NULL means that the document does not need currency convertions|
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` |In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |In a multi-document tree, this is the direct parent document. If this is the root it is NULL|
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` Readonly|The primary document, which the current document adjusts. NULL when this is not an adjustment document|
|[Adjustment_Number](#adjustment_number)|`int` Readonly|Consecutive number of the correction that this document is applying to the adjusted document.|
|[Creation_Time](#creation_time)|`datetime` Readonly|Date/Time when the document was created|
|[Creation_User](#creation_user)|`nvarchar` Readonly|The login name of the user, who created the document|
|[Void_Time](#void_time)|`datetime` Readonly|Date/time when the document has become void|
|[Void_User](#void_user)|`nvarchar` Readonly|The user who voided the document|
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly|Date/time when the document last has been adjusted by corrective document|
|[Adjustment_User](#adjustment_user)|`nvarchar` Readonly|The user who adjusted the document|
|[Read_Only](#read_only)|`bit` Readonly|1 - the document is read only; 0 - the document is not read only|
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Document_Version](#document_version)|`int` Readonly|Consecutive version number, starting with 1. Each update produces a new version of the document.|
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.|
|[Void_Reason](#void_reason)|`nvarchar` Readonly|Reason for voiding the document, entered by the user|
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly|The document which the current document is reverse of|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location which issued the document. NULL means that there is only one location within the enterprise company and locations are not used|
|[Planning_Only](#planning_only)|`bit` Readonly|Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned)|
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` |The document that is the prime cause for creation of the current document|
|[Release_Time](#release_time)|`datetime` Readonly|Date and time when the document was released (State set to Released).|
|[Complete_Time](#complete_time)|`datetime` Readonly|Date and time when the document was completed (State set to Completed).|
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`, Readonly|Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.|
|[Reference_Document_No](#reference_document_no)|`nvarchar` |The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly|The user status of this document if applicable for this document type. NULL means unknown or not yet set|
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` |The division of the company, issuing the document. NULL when the document is not issued by any specific division|
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` |The division of the company, receiving the document. NULL when the document is not received by any specific division|
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Rental_Asset_Type_Id](#rental_asset_type_id)|`uniqueidentifier` |The type of the asset.|
|[Rental_Asset_Group_Id](#rental_asset_group_id)|`uniqueidentifier` |The logical group of the rental asset.|
|[Rental_Asset_Code](#rental_asset_code)|`nvarchar` |Unique rental asset code|
|[Rental_Asset_Name](#rental_asset_name)|`nvarchar` |The name of the rental asset.|
|[Notes](#notes)|`nvarchar` ||
|[Accounting_Asset_Id](#accounting_asset_id)|`uniqueidentifier` |When not NULL identifies the corresponding accounting asset|
|[Sales_Product_Id](#sales_product_id)|`uniqueidentifier` ||
|[Work_Schedule_Id](#work_schedule_id)|`uniqueidentifier` ||
|[Time_Period_Type](#time_period_type)|`nvarchar` Allowed: `D`, `M`||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Standard_Guarantee_Amount](#standard_guarantee_amount)|`decimal(0, 0)` ||
|[Standard_Guarantee_Amount_Currency_Id](#standard_guarantee_amount_currency_id)|`uniqueidentifier` ||
|[Is_Active](#is_active)|`bit` ||
|[Rent_Assets_Enterprise_Company_Id](#rent_assets_enterprise_company_id)|`uniqueidentifier` ||

## Columns

### Lease_Line_Consumable_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lease_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumable_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Consumable_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Lease_Contract_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date

| Property | Value |
| - | - |
|Type|date|

### End_Date

| Property | Value |
| - | - |
|Type|date|

### Line_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Guarantee_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lessee_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Limit_Override

| Property | Value |
| - | - |
|Type|bit|

### Payment_Account_Id

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

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Reference_Date

| Property | Value |
| - | - |
|Type|datetime|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Void

| Property | Value |
| - | - |
|Type|bit|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Adjustment_Time

| Property | Value |
| - | - |
|Type|datetime|

### Adjustment_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planning_Only

| Property | Value |
| - | - |
|Type|bit|

### Prime_Cause_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Time

| Property | Value |
| - | - |
|Type|datetime|

### Complete_Time

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Reference_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Rental_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Rental_Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Accounting_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Schedule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Time_Period_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Guarantee_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Guarantee_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Rent_Assets_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


