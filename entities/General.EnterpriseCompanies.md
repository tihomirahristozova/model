# General.EnterpriseCompanies

The companies in the enterprise that issue documents. Entity: Gen_Enterprise_Companies

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.EnterpriseCompanies.md#Id) | guid |  
| [BIStartDate](General.EnterpriseCompanies.md#BIStartDate) | datetime (nullable) | Defines the period for which BI extracts data. BI includes documents with "Document Date" greater than or equal to "BI Start Date". [Filter(eq)] (Introduced in version 18.2.100.0) 
| [DefaultCostingMethod](General.EnterpriseCompanies.md#DefaultCostingMethod) | [General.EnterpriseCompaniesRepository.DefaultCostingMethod](General.EnterpriseCompanies.md#DefaultCostingMethod) | Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost. [Required] [Default("AVG")] 
| [DefaultCustomerCreditLimitBase](General.EnterpriseCompanies.md#DefaultCustomerCreditLimitBase) | [Amount](../data-types/Amount.md) (nullable) | Customer credit limit, which is used by default when creating new customers. It is specified in the base currency of the enterprise company. [Currency: BaseCurrency] [Filter(eq;like)] 
| [DefaultLanguage](General.EnterpriseCompanies.md#DefaultLanguage) | [General.EnterpriseCompaniesRepository.DefaultLanguage](General.EnterpriseCompanies.md#DefaultLanguage) (nullable) | The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...). [Default("en")] 
| [EditPeriodStartDate](General.EnterpriseCompanies.md#EditPeriodStartDate) | datetime (nullable) | Start date of the priod when the documents can be edited. 
| [IsActive](General.EnterpriseCompanies.md#IsActive) | boolean | Indicates whether the current Enterprise company  is active. [Required] [Default(true)] [Filter(multi eq)] (Introduced in version 20.1.100.0) 
| [PrintImagesRetentionMonths](General.EnterpriseCompanies.md#PrintImagesRetentionMonths) | int32 | A period of months for which the printed images of the documents will be kept. [Required] [Default(60)] [Filter(multi eq;ge;le)] (Introduced in version 20.1.100.0) 
| [UIBaseColor](General.EnterpriseCompanies.md#UIBaseColor) | int32 (nullable) | When not null, specifies the background color to use for visualization of the UI when the current enterprise company is selected. The color is in RGBA color format. (Introduced in version 18.2.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](General.EnterpriseCompanies.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this EnterpriseCompany. Null means that all users have unlimited permissions. [Filter(multi eq)] |
| [AdvanceProduct](General.EnterpriseCompanies.md#AdvanceProduct) | [General.Products.Products](General.Products.Products.md) (nullable) | Product that is used for handling advances in trade documents. [Filter(multi eq)] |
| [BaseCurrency](General.EnterpriseCompanies.md#BaseCurrency) | [General.Currencies](General.Currencies.md) | The base currency for summary reporting for this company. [Required] [Filter(multi eq)] |
| [Company](General.EnterpriseCompanies.md#Company) | [General.Contacts.Companies](General.Contacts.Companies.md) | Contains the base company data on which this enterprise company is based. [Required] [Filter(multi eq)] |
| [ExchangeDifferenceCreditAccount](General.EnterpriseCompanies.md#ExchangeDifferenceCreditAccount) | [Finance.Accounting.Accounts](Finance.Accounting.Accounts.md) (nullable) | Account for balancing accounting vouchers with credit difference due to currency exchanges. [Filter(multi eq)] |
| [ExchangeDifferenceDebitAccount](General.EnterpriseCompanies.md#ExchangeDifferenceDebitAccount) | [Finance.Accounting.Accounts](Finance.Accounting.Accounts.md) (nullable) | Account for balancing accounting vouchers with debit difference due to currency exchanges. [Filter(multi eq)] |
| [VATDocumentAmountType](General.EnterpriseCompanies.md#VATDocumentAmountType) | [General.DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable) | The document amount that is used to determine the amount of the VAT entries when they are generated. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Assets | [Finance.Assets.Assets](Finance.Assets.Assets.md) | List of [Asset](Finance.Assets.Assets.md) child objects, based on the [Finance.Assets.Asset.EnterpriseCompany](Finance.Assets.Assets.md#EnterpriseCompany) back reference 
| Crews | [Applications.Fleet.Crews](Applications.Fleet.Crews.md) | List of [Crew](Applications.Fleet.Crews.md) child objects, based on the [Applications.Fleet.Crew.EnterpriseCompany](Applications.Fleet.Crews.md#EnterpriseCompany) back reference 
| VehicleSets | [Applications.Fleet.VehicleSets](Applications.Fleet.VehicleSets.md) | List of [VehicleSet](Applications.Fleet.VehicleSets.md) child objects, based on the [Applications.Fleet.VehicleSet.EnterpriseCompany](Applications.Fleet.VehicleSets.md#EnterpriseCompany) back reference 
| MapPoints | [General.Geography.MapPoints](General.Geography.MapPoints.md) | List of [MapPoint](General.Geography.MapPoints.md) child objects, based on the [General.Geography.MapPoint.EnterpriseCompany](General.Geography.MapPoints.md#EnterpriseCompany) back reference 
| BGVATDeclaringPersons | [Finance.Vat.BGVATDeclaringPersons](Finance.Vat.BGVATDeclaringPersons.md) | List of [BGVATDeclaringPerson](Finance.Vat.BGVATDeclaringPersons.md) child objects, based on the [Finance.Vat.BGVATDeclaringPerson.EnterpriseCompany](Finance.Vat.BGVATDeclaringPersons.md#EnterpriseCompany) back reference 
| Resources | [Projects.Resources](Projects.Resources.md) | List of [Resource](Projects.Resources.md) child objects, based on the [Projects.Resource.EnterpriseCompany](Projects.Resources.md#EnterpriseCompany) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BIStartDate

> Defines the period for which BI extracts data. BI includes documents with "Document Date" greater than or equal to "BI Start Date". [Filter(eq)] (Introduced in version 18.2.100.0)

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### DefaultCostingMethod

> Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost. [Required] [Default("AVG")]

_Type_: **[General.EnterpriseCompaniesRepository.DefaultCostingMethod](General.EnterpriseCompanies.md#DefaultCostingMethod)**  
Allowed values for the [DefaultCostingMethod](General.EnterpriseCompanies.md#DefaultCostingMethod) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| AverageCost | AverageCost value. Stored as 'AVG'. <br /> _Database Value:_ 'AVG' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AverageCost' |
| ExplicitlySpecifyLot | ExplicitlySpecifyLot value. Stored as 'EXP'. <br /> _Database Value:_ 'EXP' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ExplicitlySpecifyLot' |
| SetByBlockedForDocument | SetByBlockedForDocument value. Stored as 'BLD'. <br /> _Database Value:_ 'BLD' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'SetByBlockedForDocument' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **AverageCost**  

### DefaultCustomerCreditLimitBase

> Customer credit limit, which is used by default when creating new customers. It is specified in the base currency of the enterprise company. [Currency: BaseCurrency] [Filter(eq;like)]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### DefaultLanguage

> The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...). [Default("en")]

_Type_: **[General.EnterpriseCompaniesRepository.DefaultLanguage](General.EnterpriseCompanies.md#DefaultLanguage) (nullable)**  
Allowed values for the [DefaultLanguage](General.EnterpriseCompanies.md#DefaultLanguage) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Bulgarian | Bulgarian value. Stored as 'bg'. <br /> _Database Value:_ 'bg' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Bulgarian' |
| English | English value. Stored as 'en'. <br /> _Database Value:_ 'en' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'English' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **English**  

### EditPeriodStartDate

> Start date of the priod when the documents can be edited.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsActive

> Indicates whether the current Enterprise company  is active. [Required] [Default(true)] [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PrintImagesRetentionMonths

> A period of months for which the printed images of the documents will be kept. [Required] [Default(60)] [Filter(multi eq;ge;le)] (Introduced in version 20.1.100.0)

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **60**  

### UIBaseColor

> When not null, specifies the background color to use for visualization of the UI when the current enterprise company is selected. The color is in RGBA color format. (Introduced in version 18.2.100.0)

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

> The access key, containing the user permissions for this EnterpriseCompany. Null means that all users have unlimited permissions. [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AdvanceProduct

> Product that is used for handling advances in trade documents. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### BaseCurrency

> The base currency for summary reporting for this company. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Company

> Contains the base company data on which this enterprise company is based. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Companies](General.Contacts.Companies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ExchangeDifferenceCreditAccount

> Account for balancing accounting vouchers with credit difference due to currency exchanges. [Filter(multi eq)]

_Type_: **[Finance.Accounting.Accounts](Finance.Accounting.Accounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ExchangeDifferenceDebitAccount

> Account for balancing accounting vouchers with debit difference due to currency exchanges. [Filter(multi eq)]

_Type_: **[Finance.Accounting.Accounts](Finance.Accounting.Accounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### VATDocumentAmountType

> The document amount that is used to determine the amount of the VAT entries when they are generated. [Filter(multi eq)]

_Type_: **[General.DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.EnterpriseCompanies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.EnterpriseCompanies erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.EnterpriseCompanies erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_EnterpriseCompanies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_EnterpriseCompanies?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Enterprise_Companies?$top=10>

