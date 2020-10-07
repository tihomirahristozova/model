# Crm.Customers

Customer contracts list. For each combination of Enterprise Company and external Party there can be zero or one records of this. Entity: Crm_Customers

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Customers.md#Id) | guid |  
| [Active](Crm.Customers.md#Active) | boolean | True if the customer is active, false - not to list in combo boxes for choosing in new documents. [Required] [Default(true)] [Filter(eq)] 
| [AllowUseAsPrimaryCustomer](Crm.Customers.md#AllowUseAsPrimaryCustomer) | boolean | Specifies whether to allow the customer to be used as primary customer in a sales deal. [Required] [Default(false)] [Filter(eq)] 
| [AllowUseAsShipToCustomer](Crm.Customers.md#AllowUseAsShipToCustomer) | boolean | True to allow the customer to be used as ship to customer in a sales deal. [Required] [Default(false)] [Filter(eq)] 
| [CreationTime](Crm.Customers.md#CreationTime) | datetime (nullable) | Date and time when the Customer was created. [Filter(ge;le)] [ReadOnly] 
| [CreationUser](Crm.Customers.md#CreationUser) | string (nullable) | Login name of the user, who created the Customer. [Filter(like)] [ReadOnly] 
| [CreditLimit](Crm.Customers.md#CreditLimit) | [Amount](../data-types/Amount.md) (nullable) | Total credit limit for the customer in the customers' default currency. null means there is no limit. [Currency: DefaultCurrency] 
| [Number](Crm.Customers.md#Number) | string (nullable) | Unique customer number. [Filter(eq;like)] [ORD] 
| [DefaultDeliveryTermDays](Crm.Customers.md#DefaultDeliveryTermDays) | int32 | Default term in days for goods delivery, starting at the day of sale. [Required] [Default(0)] 
| [DefaultPaymentStartDays](Crm.Customers.md#DefaultPaymentStartDays) | int32 | Specifies the number of days after the sales order, when the payment becomes due. 0 means that the payment is due immediately. [Required] [Default(0)] 
| [DefaultPaymentTermDays](Crm.Customers.md#DefaultPaymentTermDays) | int32 | Default payment term in days when issuing documents for this customer. [Required] [Default(0)] 
| [FromDate](Crm.Customers.md#FromDate) | datetime (nullable) | Start date of the customer relationship. [Default(Today)] [Filter(ge;le)] 
| [GracePeriodDays](Crm.Customers.md#GracePeriodDays) | int32 | Number of days after the payment deadline, during which the system still allows new sales orders for the customer. [Required] [Default(0)] 
| [PersistSalesOrdersLots](Crm.Customers.md#PersistSalesOrdersLots) | boolean | If checked, specifies that the lots set in the Sales orders for this customer, cannot be changed during the execution of the Store transactions for these Sales orders. [Required] [Default(false)] [Filter(eq)] 
| [ThruDate](Crm.Customers.md#ThruDate) | datetime (nullable) | The date of customer relationship termination. null for active customers. [Filter(ge;le)] 
| [UpdateTime](Crm.Customers.md#UpdateTime) | datetime (nullable) | Date and time when the Customer was last updated. [Filter(ge;le)] [ReadOnly] 
| [UpdateUser](Crm.Customers.md#UpdateUser) | string (nullable) | Login name of the user, who last updated the Customer. [Filter(like)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CollectionsResponsibleEmployee](Crm.Customers.md#CollectionsResponsibleEmployee) | [General.Contacts.CompanyEmployees](General.Contacts.CompanyEmployees.md) (nullable) | The employee, who is responsible for the collections from the customer. [Filter(multi eq)] |
| [CustomerType](Crm.Customers.md#CustomerType) | [Crm.CustomerTypes](Crm.CustomerTypes.md) (nullable) | The user-defined type of this customer. null when there is no specific type. Record-level security from the customer type is applied to the individual customers and can be used for security purposes. [Filter(multi eq)] |
| [DefaultCurrency](Crm.Customers.md#DefaultCurrency) | [General.Currencies](General.Currencies.md) (nullable) | The primary currency for value calculations for this customer - for credit limit, due amounts, etc. [Filter(multi eq)] |
| [DefaultDistributionChannel](Crm.Customers.md#DefaultDistributionChannel) | [Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable) | The default distribution channel used when selling to the customer. [Filter(multi eq)] |
| [DefaultPaymentAccount](Crm.Customers.md#DefaultPaymentAccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | The default payment account to use when creating new documents for this customer. [Filter(multi eq)] |
| [DefaultPaymentType](Crm.Customers.md#DefaultPaymentType) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | If not null, specifies default payment type for the sales, offers and invoices for this customer. [Filter(multi eq)] |
| [DefaultPriceList](Crm.Customers.md#DefaultPriceList) | [Crm.PriceLists](Crm.PriceLists.md) (nullable) | If not null, specifies default price list when selling to this customer. [Filter(multi eq)] |
| [EnterpriseCompany](Crm.Customers.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company for which this customer is recorded. The same external party can be listed with different conditions for the different enterprise companies. [Filter(multi eq)] |
| [Party](Crm.Customers.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | Base party Id. [Required] [Filter(multi eq)] [Owner] |
| [SalesPerson](Crm.Customers.md#SalesPerson) | [Crm.SalesPersons](Crm.SalesPersons.md) (nullable) | The default sales person for new sales documents for this customer. [Filter(multi eq)] |
| [ServicedByEnterpriseCompanyLocation](Crm.Customers.md#ServicedByEnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location, which sells to this client by default. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Products | [Crm.CustomerProducts](Crm.CustomerProducts.md) | List of [CustomerProduct](Crm.CustomerProducts.md) child objects, based on the [Crm.CustomerProduct.Customer](Crm.CustomerProducts.md#Customer) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Active

> True if the customer is active, false - not to list in combo boxes for choosing in new documents. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### AllowUseAsPrimaryCustomer

> Specifies whether to allow the customer to be used as primary customer in a sales deal. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AllowUseAsShipToCustomer

> True to allow the customer to be used as ship to customer in a sales deal. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### CreationTime

> Date and time when the Customer was created. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationUser

> Login name of the user, who created the Customer. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CreditLimit

> Total credit limit for the customer in the customers' default currency. null means there is no limit. [Currency: DefaultCurrency]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((obj.DefaultCurrency != null), obj.EnterpriseCompany.DefaultCustomerCreditLimitBase, obj.CreditLimit)`

_Front-End Recalc Expressions:_  
`IIF((obj.DefaultCurrency != null), obj.EnterpriseCompany.DefaultCustomerCreditLimitBase, obj.CreditLimit)`
### Number

> Unique customer number. [Filter(eq;like)] [ORD]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DefaultDeliveryTermDays

> Default term in days for goods delivery, starting at the day of sale. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### DefaultPaymentStartDays

> Specifies the number of days after the sales order, when the payment becomes due. 0 means that the payment is due immediately. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### DefaultPaymentTermDays

> Default payment term in days when issuing documents for this customer. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### FromDate

> Start date of the customer relationship. [Default(Today)] [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### GracePeriodDays

> Number of days after the payment deadline, during which the system still allows new sales orders for the customer. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### PersistSalesOrdersLots

> If checked, specifies that the lots set in the Sales orders for this customer, cannot be changed during the execution of the Store transactions for these Sales orders. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ThruDate

> The date of customer relationship termination. null for active customers. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UpdateTime

> Date and time when the Customer was last updated. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UpdateUser

> Login name of the user, who last updated the Customer. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### CollectionsResponsibleEmployee

> The employee, who is responsible for the collections from the customer. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyEmployees](General.Contacts.CompanyEmployees.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CustomerType

> The user-defined type of this customer. null when there is no specific type. Record-level security from the customer type is applied to the individual customers and can be used for security purposes. [Filter(multi eq)]

_Type_: **[Crm.CustomerTypes](Crm.CustomerTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DefaultCurrency

> The primary currency for value calculations for this customer - for credit limit, due amounts, etc. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.EnterpriseCompany.BaseCurrency`
### DefaultDistributionChannel

> The default distribution channel used when selling to the customer. [Filter(multi eq)]

_Type_: **[Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DefaultPaymentAccount

> The default payment account to use when creating new documents for this customer. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DefaultPaymentType.GetDefaultPaymentAccount().IfNullThen(obj.DefaultPaymentAccount)`
### DefaultPaymentType

> If not null, specifies default payment type for the sales, offers and invoices for this customer. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DefaultPriceList

> If not null, specifies default price list when selling to this customer. [Filter(multi eq)]

_Type_: **[Crm.PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The Enterprise Company for which this customer is recorded. The same external party can be listed with different conditions for the different enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Transaction.CurrentEnterpriseCompany`
### Party

> Base party Id. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SalesPerson

> The default sales person for new sales documents for this customer. [Filter(multi eq)]

_Type_: **[Crm.SalesPersons](Crm.SalesPersons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServicedByEnterpriseCompanyLocation

> The enterprise company location, which sells to this client by default. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Customers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Customers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Customers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Customers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Customers?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Customers?$top=10>

