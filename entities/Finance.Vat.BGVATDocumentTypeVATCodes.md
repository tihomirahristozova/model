---
uid: Finance.Vat.BGVATDocumentTypeVATCodes
---
# Finance.Vat.BGVATDocumentTypeVATCodes

Contains the VAT codes, which should be used, when reporting VAT for the different document types. Entity: Nat_BG_VAT_Document_Type_VAT_Codes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Vat.BGVATDocumentTypeVATCodes.md#Id) | guid |  
| [CashReportingVATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#CashReportingVATCode) | [Finance.Vat.BGVATDocumentTypeVATCodesRepository.CashReportingVATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#CashReportingVATCode) (nullable) | VAT code, which will be used when Cash Reporting mode is used for the entry. Allowed values are the same as for VAT Code. 
| [VATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#VATCode) | [Finance.Vat.BGVATDocumentTypeVATCodesRepository.VATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#VATCode) (nullable) | VAT code to use when creating VAT export files for the specified Document Type. Allowed values is government-regulated list of values. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](Finance.Vat.BGVATDocumentTypeVATCodes.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | Document type that generates VAT entries. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CashReportingVATCode

> VAT code, which will be used when Cash Reporting mode is used for the entry. Allowed values are the same as for VAT Code.

_Type_: **[Finance.Vat.BGVATDocumentTypeVATCodesRepository.CashReportingVATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#CashReportingVATCode) (nullable)**  
Allowed values for the [CashReportingVATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#CashReportingVATCode) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Invoice | Invoice value. Stored as '01'. <br /> _Database Value:_ '01' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Invoice' |
| DebitNote | DebitNote value. Stored as '02'. <br /> _Database Value:_ '02' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'DebitNote' |
| CreditNote | CreditNote value. Stored as '03'. <br /> _Database Value:_ '03' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'CreditNote' |
| CallOffStockRegisterTheGoodsAreSentOrTransportedFromTheCountryToAnotherEUCountry | CallOffStockRegisterTheGoodsAreSentOrTransportedFromTheCountryToAnotherEUCountry value. Stored as '04'. <br /> _Database Value:_ '04' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'CallOffStockRegisterTheGoodsAreSentOrTransportedFromTheCountryToAnotherEUCountry' |
| CallOffStockRegisterTheGoodsAreReceivedInTheCountry | CallOffStockRegisterTheGoodsAreReceivedInTheCountry value. Stored as '05'. <br /> _Database Value:_ '05' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CallOffStockRegisterTheGoodsAreReceivedInTheCountry' |
| CustomHouseEntry | CustomHouseEntry value. Stored as '07'. <br /> _Database Value:_ '07' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CustomHouseEntry' |
| Protocol | Protocol value. Stored as '09'. <br /> _Database Value:_ '09' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Protocol' |
| InvoiceCashReporting | InvoiceCashReporting value. Stored as '11'. <br /> _Database Value:_ '11' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'InvoiceCashReporting' |
| DebitNoteCashReporting | DebitNoteCashReporting value. Stored as '12'. <br /> _Database Value:_ '12' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'DebitNoteCashReporting' |
| CreditNoteCashReporting | CreditNoteCashReporting value. Stored as '13'. <br /> _Database Value:_ '13' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'CreditNoteCashReporting' |
| SalesReport | SalesReport value. Stored as '81'. <br /> _Database Value:_ '81' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'SalesReport' |
| SpecialTaxOrderSalesReport | SpecialTaxOrderSalesReport value. Stored as '82'. <br /> _Database Value:_ '82' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'SpecialTaxOrderSalesReport' |
| RecordForRecoverableTaxByArticle151vAl3OfBGVATLaw | RecordForRecoverableTaxByArticle151vAl3OfBGVATLaw value. Stored as '91'. <br /> _Database Value:_ '91' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'RecordForRecoverableTaxByArticle151vAl3OfBGVATLaw' |
| RecordForTaxCreditByArticle151gAl3OfBGVATLawOrReportByArt104zhAl14 | RecordForTaxCreditByArticle151gAl3OfBGVATLawOrReportByArt104zhAl14 value. Stored as '92'. <br /> _Database Value:_ '92' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'RecordForTaxCreditByArticle151gAl3OfBGVATLawOrReportByArt104zhAl14' |
| RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithNoCashReportingReceiver | RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithNoCashReportingReceiver value. Stored as '93'. <br /> _Database Value:_ '93' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithNoCashReportingReceiver' |
| RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithCashReportingReceiver | RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithCashReportingReceiver value. Stored as '94'. <br /> _Database Value:_ '94' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithCashReportingReceiver' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VATCode

> VAT code to use when creating VAT export files for the specified Document Type. Allowed values is government-regulated list of values.

_Type_: **[Finance.Vat.BGVATDocumentTypeVATCodesRepository.VATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#VATCode) (nullable)**  
Allowed values for the [VATCode](Finance.Vat.BGVATDocumentTypeVATCodes.md#VATCode) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Invoice | Invoice value. Stored as '01'. <br /> _Database Value:_ '01' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Invoice' |
| DebitNote | DebitNote value. Stored as '02'. <br /> _Database Value:_ '02' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'DebitNote' |
| CreditNote | CreditNote value. Stored as '03'. <br /> _Database Value:_ '03' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'CreditNote' |
| CallOffStockRegisterTheGoodsAreSentOrTransportedFromTheCountryToAnotherEUCountry | CallOffStockRegisterTheGoodsAreSentOrTransportedFromTheCountryToAnotherEUCountry value. Stored as '04'. <br /> _Database Value:_ '04' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'CallOffStockRegisterTheGoodsAreSentOrTransportedFromTheCountryToAnotherEUCountry' |
| CallOffStockRegisterTheGoodsAreReceivedInTheCountry | CallOffStockRegisterTheGoodsAreReceivedInTheCountry value. Stored as '05'. <br /> _Database Value:_ '05' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CallOffStockRegisterTheGoodsAreReceivedInTheCountry' |
| CustomHouseEntry | CustomHouseEntry value. Stored as '07'. <br /> _Database Value:_ '07' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CustomHouseEntry' |
| Protocol | Protocol value. Stored as '09'. <br /> _Database Value:_ '09' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Protocol' |
| InvoiceCashReporting | InvoiceCashReporting value. Stored as '11'. <br /> _Database Value:_ '11' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'InvoiceCashReporting' |
| DebitNoteCashReporting | DebitNoteCashReporting value. Stored as '12'. <br /> _Database Value:_ '12' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'DebitNoteCashReporting' |
| CreditNoteCashReporting | CreditNoteCashReporting value. Stored as '13'. <br /> _Database Value:_ '13' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'CreditNoteCashReporting' |
| SalesReport | SalesReport value. Stored as '81'. <br /> _Database Value:_ '81' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'SalesReport' |
| SpecialTaxOrderSalesReport | SpecialTaxOrderSalesReport value. Stored as '82'. <br /> _Database Value:_ '82' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'SpecialTaxOrderSalesReport' |
| RecordForRecoverableTaxByArticle151vAl3OfBGVATLaw | RecordForRecoverableTaxByArticle151vAl3OfBGVATLaw value. Stored as '91'. <br /> _Database Value:_ '91' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'RecordForRecoverableTaxByArticle151vAl3OfBGVATLaw' |
| RecordForTaxCreditByArticle151gAl3OfBGVATLawOrReportByArt104zhAl14 | RecordForTaxCreditByArticle151gAl3OfBGVATLawOrReportByArt104zhAl14 value. Stored as '92'. <br /> _Database Value:_ '92' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'RecordForTaxCreditByArticle151gAl3OfBGVATLawOrReportByArt104zhAl14' |
| RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithNoCashReportingReceiver | RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithNoCashReportingReceiver value. Stored as '93'. <br /> _Database Value:_ '93' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithNoCashReportingReceiver' |
| RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithCashReportingReceiver | RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithCashReportingReceiver value. Stored as '94'. <br /> _Database Value:_ '94' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'RecordForRecoverableTaxByArticle151vAl7OfBGVATLawWithCashReportingReceiver' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DocumentType

> Document type that generates VAT entries. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Vat.BGVATDocumentTypeVATCodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Vat.BGVATDocumentTypeVATCodes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Vat.BGVATDocumentTypeVATCodes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_BGVATDocumentTypeVATCodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_BGVATDocumentTypeVATCodes?$top=10>

