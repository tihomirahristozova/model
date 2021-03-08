# Table Acc_Templates

Accounting templates are used to automate the postings for repetitive business transactions. Templates can be bound to almost all documents and automate their postings. Entity: Acc_Templates

# Aggregate Hierarchy

* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Template_Id|`Guid`|`PK`, Readonly||
|Template_Name|`String`||The name of this Template. `Required` `Filter(like)` |
|Voucher_Date_Source|`String`||Determines the source for the document date of the generated voucher. If not specified the voucher date is set as usual. |
|Voucher_Description_Mask|`String`||Template voucher description. Can use field substitutes, surrounded with square brackets. |
