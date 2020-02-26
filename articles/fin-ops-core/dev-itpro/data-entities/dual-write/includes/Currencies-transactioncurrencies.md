## <a name="currencies-to-transactioncurrencies"></a>Valuta naar transactioncurrencies

Deze sjabloon synchroniseert gegevens tussen Finance and Operations-apps en Common Data Service.

Bronfilter: ((CURRENCYCODE! = "999"))

Finance and Operations-veld | Toewijzingstype | Ander Dynamics 365-veld | Standaardwaarde
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
geen | >> | exchangerate | 1
