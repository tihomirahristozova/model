---
uid: Finance.Intrastat.DeclarationLines
---
# Finance.Intrastat.DeclarationLines

Contains the details of the Intrastat declarations, issued by the enterprise companies. Entity: Its_Declaration_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DeliveryTerms](Finance.Intrastat.DeclarationLines.md#deliveryterms) | [DeliveryTerms](Finance.Intrastat.DeclarationLines.md#deliveryterms) | Delivery terms - classification according to Intrastat (which uses the common abbreviations). [Required] 
| [Id](Finance.Intrastat.DeclarationLines.md#id) | guid |  
| [InvoicedValueAmountBase](Finance.Intrastat.DeclarationLines.md#invoicedvalueamountbase) | [Amount](../data-types.md#amount) | Invoiced value of the goods in the base currency. [Currency: IntrastatDeclaration.EnterpriseCompany.BaseCurrency] [Required] 
| [LineAction](Finance.Intrastat.DeclarationLines.md#lineaction) | [LineAction](Finance.Intrastat.DeclarationLines.md#lineaction) | Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted. [Required] [Default("NEW")] 
| [LineNo](Finance.Intrastat.DeclarationLines.md#lineno) | int32 | Consequtive line number within the intrastat declaration. [Required] [Filter(eq)] 
| [NetMassKg](Finance.Intrastat.DeclarationLines.md#netmasskg) | decimal | Net mass of the goods in kg. [Required] [Filter(multi eq)] 
| [QuantitySupplementaryUnit](Finance.Intrastat.DeclarationLines.md#quantitysupplementaryunit) | decimal (nullable) | Quantity of the goods in the supplementary unit. null when no supplementary unit is specified. 
| [StatisticalValueAmountBase](Finance.Intrastat.DeclarationLines.md#statisticalvalueamountbase) | [Amount](../data-types.md#amount) (nullable) | Statistical value of the goods in the base currency. [Currency: IntrastatDeclaration.EnterpriseCompany.BaseCurrency] 
| [TransactionNature](Finance.Intrastat.DeclarationLines.md#transactionnature) | [TransactionNature](Finance.Intrastat.DeclarationLines.md#transactionnature) | Transaction nature, according to the Intrastat classification. [Required] 
| [TransportMode](Finance.Intrastat.DeclarationLines.md#transportmode) | [TransportMode](Finance.Intrastat.DeclarationLines.md#transportmode) | Transportation mode - type of transportation used. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AdministrativeRegion](Finance.Intrastat.DeclarationLines.md#administrativeregion) | [General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) | Administrative region of the enterprise company at the time of the declaration. [Required] [Filter(multi eq)] |
| [IntrastatCommodityCode](Finance.Intrastat.DeclarationLines.md#intrastatcommoditycode) | [Finance.Intrastat.CommodityCodes](Finance.Intrastat.CommodityCodes.md) | The commodity code of the goods, according to the Intrastat commodity classification. [Required] [Filter(multi eq)] |
| [IntrastatDeclaration](Finance.Intrastat.DeclarationLines.md#intrastatdeclaration) | [Finance.Intrastat.Declarations](Finance.Intrastat.Declarations.md) | The intrastat declaration, to which this line belongs. [Required] [Filter(multi eq)] [Owner] |
| [OriginCountry](Finance.Intrastat.DeclarationLines.md#origincountry) | [General.Geography.Countries](General.Geography.Countries.md) (nullable) | The country of origin of the goods. null for outbound declarations. [Filter(multi eq)] |
| [PartyCountry](Finance.Intrastat.DeclarationLines.md#partycountry) | [General.Geography.Countries](General.Geography.Countries.md) | The country of the partner. [Required] [Filter(multi eq)] |
| [TransportCountry](Finance.Intrastat.DeclarationLines.md#transportcountry) | [General.Geography.Countries](General.Geography.Countries.md) | The country of the transportation company. [Required] [Filter(multi eq)] |


## Attribute Details

### DeliveryTerms

> Delivery terms - classification according to Intrastat (which uses the common abbreviations). [Required]

_Type_: **[DeliveryTerms](Finance.Intrastat.DeclarationLines.md#deliveryterms)**  
Allowed values for the [DeliveryTerms](Finance.Intrastat.DeclarationLines.md#deliveryterms) data attribute  
_Allowed Values (Finance.Intrastat.DeclarationLinesRepository.DeliveryTerms Enum Members)_  

| Value | Description |
| ---- | --- |
| ExWorks | ExWorks value. Stored as 'EXW'. <br /> _Database Value:_ 'EXW' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ExWorks' |
| FrancoCarrier | FrancoCarrier value. Stored as 'FCA'. <br /> _Database Value:_ 'FCA' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'FrancoCarrier' |
| FreeAlongsideShip | FreeAlongsideShip value. Stored as 'FAS'. <br /> _Database Value:_ 'FAS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'FreeAlongsideShip' |
| FreeOnBoard | FreeOnBoard value. Stored as 'FOB'. <br /> _Database Value:_ 'FOB' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FreeOnBoard' |
| CostAndFreightCF | CostAndFreightCF value. Stored as 'CFR'. <br /> _Database Value:_ 'CFR' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CostAndFreightCF' |
| CostInsuranceAndFreight | CostInsuranceAndFreight value. Stored as 'CIF'. <br /> _Database Value:_ 'CIF' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CostInsuranceAndFreight' |
| CarriagePaidTo | CarriagePaidTo value. Stored as 'CPT'. <br /> _Database Value:_ 'CPT' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'CarriagePaidTo' |
| CarriageAndInsurancePaidTo | CarriageAndInsurancePaidTo value. Stored as 'CIP'. <br /> _Database Value:_ 'CIP' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'CarriageAndInsurancePaidTo' |
| DeliveredAtPlace | DeliveredAtPlace value. Stored as 'DAP'. <br /> _Database Value:_ 'DAP' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'DeliveredAtPlace' |
| DeliveredAtTerminal | DeliveredAtTerminal value. Stored as 'DAT'. <br /> _Database Value:_ 'DAT' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'DeliveredAtTerminal' |
| DeliveredDutyPaid | DeliveredDutyPaid value. Stored as 'DDP'. <br /> _Database Value:_ 'DDP' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'DeliveredDutyPaid' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### InvoicedValueAmountBase

> Invoiced value of the goods in the base currency. [Currency: IntrastatDeclaration.EnterpriseCompany.BaseCurrency] [Required]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineAction

> Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted. [Required] [Default("NEW")]

_Type_: **[LineAction](Finance.Intrastat.DeclarationLines.md#lineaction)**  
Allowed values for the [LineAction](Finance.Intrastat.DeclarationLines.md#lineaction) data attribute  
_Allowed Values (Finance.Intrastat.DeclarationLinesRepository.LineAction Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New value. Stored as 'NEW'. <br /> _Database Value:_ 'NEW' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| EditedNew | EditedNew value. Stored as 'EDN'. <br /> _Database Value:_ 'EDN' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'EditedNew' |
| EditedOld | EditedOld value. Stored as 'EDO'. <br /> _Database Value:_ 'EDO' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'EditedOld' |
| Deleted | Deleted value. Stored as 'DEL'. <br /> _Database Value:_ 'DEL' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Deleted' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **New**  

### LineNo

> Consequtive line number within the intrastat declaration. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.IntrastatDeclaration.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.IntrastatDeclaration.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### NetMassKg

> Net mass of the goods in kg. [Required] [Filter(multi eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantitySupplementaryUnit

> Quantity of the goods in the supplementary unit. null when no supplementary unit is specified.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StatisticalValueAmountBase

> Statistical value of the goods in the base currency. [Currency: IntrastatDeclaration.EnterpriseCompany.BaseCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TransactionNature

> Transaction nature, according to the Intrastat classification. [Required]

_Type_: **[TransactionNature](Finance.Intrastat.DeclarationLines.md#transactionnature)**  
Allowed values for the [TransactionNature](Finance.Intrastat.DeclarationLines.md#transactionnature) data attribute  
_Allowed Values (Finance.Intrastat.DeclarationLinesRepository.TransactionNature Enum Members)_  

| Value | Description |
| ---- | --- |
| OutrightPurchaseOrSale | OutrightPurchaseOrSale value. Stored as '11'. <br /> _Database Value:_ '11' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'OutrightPurchaseOrSale' |
| SupplyForSale | SupplyForSale value. Stored as '12'. <br /> _Database Value:_ '12' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'SupplyForSale' |
| BarterTrade | BarterTrade value. Stored as '13'. <br /> _Database Value:_ '13' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BarterTrade' |
| FinancialLeasing | FinancialLeasing value. Stored as '14'. <br /> _Database Value:_ '14' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FinancialLeasing' |
| OtherTransactions | OtherTransactions value. Stored as '19'. <br /> _Database Value:_ '19' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'OtherTransactions' |
| ReturnStokilizing | ReturnStokilizing value. Stored as '21'. <br /> _Database Value:_ '21' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'ReturnStokilizing' |
| ReplacementForReturnedGoods | ReplacementForReturnedGoods value. Stored as '22'. <br /> _Database Value:_ '22' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'ReplacementForReturnedGoods' |
| ReplacementOfGoodsNotBeingReturned | ReplacementOfGoodsNotBeingReturned value. Stored as '23'. <br /> _Database Value:_ '23' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'ReplacementOfGoodsNotBeingReturned' |
| ReturnOrExchangeOfOtherGoods | ReturnOrExchangeOfOtherGoods value. Stored as '29'. <br /> _Database Value:_ '29' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'ReturnOrExchangeOfOtherGoods' |
| SpecificTransactions | SpecificTransactions value. Stored as '60'. <br /> _Database Value:_ '60' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'SpecificTransactions' |
| OperationsOnJointProjects | OperationsOnJointProjects value. Stored as '70'. <br /> _Database Value:_ '70' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'OperationsOnJointProjects' |
| TransactionsOfConstructionMaterialsAndEquipment | TransactionsOfConstructionMaterialsAndEquipment value. Stored as '80'. <br /> _Database Value:_ '80' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'TransactionsOfConstructionMaterialsAndEquipment' |
| OtherTransactionsLeasing | OtherTransactionsLeasing value. Stored as '91'. <br /> _Database Value:_ '91' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'OtherTransactionsLeasing' |
| OtherTransactionsOther | OtherTransactionsOther value. Stored as '99'. <br /> _Database Value:_ '99' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'OtherTransactionsOther' |
| DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind | DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind value. Stored as '30'. <br /> _Database Value:_ '30' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind' |
| GoodsThatAreExpectedToBeReturnedToSender | GoodsThatAreExpectedToBeReturnedToSender value. Stored as '41'. <br /> _Database Value:_ '41' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'GoodsThatAreExpectedToBeReturnedToSender' |
| GoodsThatAreNotExpectedToBeReturnedToSender | GoodsThatAreNotExpectedToBeReturnedToSender value. Stored as '42'. <br /> _Database Value:_ '42' <br /> _Model Value:_ 16 <br /> _Domain API Value:_ 'GoodsThatAreNotExpectedToBeReturnedToSender' |
| GoodsThatAreReturnedToSender | GoodsThatAreReturnedToSender value. Stored as '51'. <br /> _Database Value:_ '51' <br /> _Model Value:_ 17 <br /> _Domain API Value:_ 'GoodsThatAreReturnedToSender' |
| GoodsThatAreNotReturnedToSender | GoodsThatAreNotReturnedToSender value. Stored as '52'. <br /> _Database Value:_ '52' <br /> _Model Value:_ 18 <br /> _Domain API Value:_ 'GoodsThatAreNotReturnedToSender' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TransportMode

> Transportation mode - type of transportation used. [Required]

_Type_: **[TransportMode](Finance.Intrastat.DeclarationLines.md#transportmode)**  
Allowed values for the [TransportMode](Finance.Intrastat.DeclarationLines.md#transportmode) data attribute  
_Allowed Values (Finance.Intrastat.DeclarationLinesRepository.TransportMode Enum Members)_  

| Value | Description |
| ---- | --- |
| Shipping | Shipping value. Stored as '1'. <br /> _Database Value:_ '1' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Shipping' |
| RailwayTransport | RailwayTransport value. Stored as '2'. <br /> _Database Value:_ '2' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RailwayTransport' |
| RoadTransport | RoadTransport value. Stored as '3'. <br /> _Database Value:_ '3' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RoadTransport' |
| AirTransport | AirTransport value. Stored as '4'. <br /> _Database Value:_ '4' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'AirTransport' |
| Mail | Mail value. Stored as '5'. <br /> _Database Value:_ '5' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Mail' |
| FixedTransportInstallations | FixedTransportInstallations value. Stored as '7'. <br /> _Database Value:_ '7' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'FixedTransportInstallations' |
| RiverTransport | RiverTransport value. Stored as '8'. <br /> _Database Value:_ '8' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'RiverTransport' |
| SelfPropelled | SelfPropelled value. Stored as '9'. <br /> _Database Value:_ '9' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'SelfPropelled' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AdministrativeRegion

> Administrative region of the enterprise company at the time of the declaration. [Required] [Filter(multi eq)]

_Type_: **[General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### IntrastatCommodityCode

> The commodity code of the goods, according to the Intrastat commodity classification. [Required] [Filter(multi eq)]

_Type_: **[Finance.Intrastat.CommodityCodes](Finance.Intrastat.CommodityCodes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### IntrastatDeclaration

> The intrastat declaration, to which this line belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Intrastat.Declarations](Finance.Intrastat.Declarations.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### OriginCountry

> The country of origin of the goods. null for outbound declarations. [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PartyCountry

> The country of the partner. [Required] [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportCountry

> The country of the transportation company. [Required] [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Intrastat.DeclarationLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Intrastat.DeclarationLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Intrastat.DeclarationLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Intrastat_DeclarationLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Intrastat_DeclarationLines?$top=10>

