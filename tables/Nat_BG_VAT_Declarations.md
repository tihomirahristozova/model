# Table Nat_BG_VAT_Declarations

National data: Contains the VAT declarations, issued by the enterprise company, according to the Bulgarian legislation. Entity: Nat_BG_VAT_Declarations

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[VAT_Declaration_Id](#vat_declaration_id)|`uniqueidentifier` `PK`|Unique identification of the VAT declaration.|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[VAT_Period_Start](#vat_period_start)|`date` |Start date of the period fot which the VAT declaration is made.|
|[VAT_Period_End](#vat_period_end)|`date` |End date of the period fot which the VAT declaration is made.|
|[Declaring_Person_Id](#declaring_person_id)|`uniqueidentifier` |Specific declaring person for this declaration. If the declaring person isn't specified then the default declaring person for the enterprise company is used|
|[Coefficient_VATL_Article_73](#coefficient_vatl_article_73)|`decimal(3, 2)` |Field 01 - 33 from the declaration. Must be between 0.00 and 1.00.|
|[Deducted_VAT_Amount_Article_92_Paragraph_1](#deducted_vat_amount_article_92_paragraph_1)|`decimal(14, 2)` |Field 01 - 70 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[Deposited_VAT_Amount](#deposited_vat_amount)|`decimal(14, 2)` |Field 01 - 71 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Amount_To_Recoup_Article_92_Paragraph_1](#vat_amount_to_recoup_article_92_paragraph_1)|`decimal(14, 2)` |Field 01 - 80 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Amount_To_Recoup_Article_92_Paragraph_3](#vat_amount_to_recoup_article_92_paragraph_3)|`decimal(14, 2)` |Field 01 - 81 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Amount_To_Recoup_Article_92_Paragraph_4](#vat_amount_to_recoup_article_92_paragraph_4)|`decimal(14, 2)` |Field 01 - 82 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Declaration_Representing_Person_Id](#vat_declaration_representing_person_id)|`uniqueidentifier` |Representing person for the purposes of submitting of VAT declarations.|
|[VAT_Declaration_Representing_Person_Position](#vat_declaration_representing_person_position)|`nvarchar(64)` |Position of the representing person for the purposes of submitting of VAT declarations.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### VAT_Declaration_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Period_Start

| Property | Value |
| - | - |
|Type|date|

### VAT_Period_End

| Property | Value |
| - | - |
|Type|date|

### Declaring_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Coefficient_VATL_Article_73

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Deducted_VAT_Amount_Article_92_Paragraph_1

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Deposited_VAT_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### VAT_Amount_To_Recoup_Article_92_Paragraph_1

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### VAT_Amount_To_Recoup_Article_92_Paragraph_3

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### VAT_Amount_To_Recoup_Article_92_Paragraph_4

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### VAT_Declaration_Representing_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Declaration_Representing_Person_Position

| Property | Value |
| - | - |
|Type|nvarchar(64)|

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


