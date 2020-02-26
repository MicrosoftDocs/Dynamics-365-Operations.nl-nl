## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>Bronbelastingcodes naar msdyn_withholdingtaxcodes

Deze sjabloon synchroniseert gegevens tussen Finance and Operations-apps en Common Data Service.

Finance and Operations-veld | Toewijzingstype | Ander Dynamics 365-veld | Standaardwaarde
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
