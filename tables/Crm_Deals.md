# Table Crm_Deals

Potential deals (Opportunities). Entity: Crm_Deals

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Deal_Id](#deal_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Leading_Sales_Person_Id](#leading_sales_person_id)|`uniqueidentifier` |The sales person, responsible for the opportunity|
|[Party_Id](#party_id)|`uniqueidentifier` |The prospect customers party. The party might not yet have a customer record.|
|[Expected_Revenue](#expected_revenue)|`decimal(18, 2)` |Expected total revenue. For automatically renewed contracts it's the amount until the first renewal.|
|[Expected_Revenue_Currency_Id](#expected_revenue_currency_id)|`uniqueidentifier` |The currency of Expected Revenue|
|[Revenue_Start_Date](#revenue_start_date)|`datetime` |Expected date on which revenue from this deal will start.|
|[Revenue_End_Date](#revenue_end_date)|`datetime` |Expected date on which the last revenue from this deal will occur.|
|[Success_Probability](#success_probability)|`decimal(3, 2)` |Probability of success of that opportunity in percents (for example, 15 percent is stored as 0.15).|
|[Deal_Status](#deal_status)|`nvarchar(3)` Allowed: `INP`, `SUC`, `UNS`|Current status of this deal. 'SUC' = Successful, 'UNS' = Unsuccessful, 'INP' = In progress|
|[Dealer_Id](#dealer_id)|`uniqueidentifier` |The external dealer, which provided the opportunity|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Deal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Leading_Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Expected_Revenue

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Expected_Revenue_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Revenue_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Revenue_End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Success_Probability

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Deal_Status

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Dealer_Id

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


