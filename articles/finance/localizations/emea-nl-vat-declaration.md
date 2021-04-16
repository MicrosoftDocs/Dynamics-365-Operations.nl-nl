---
title: Btw-aangifte voor Nederland
description: In dit onderwerp wordt uitgelegd hoe u de btw-aangifte voor rechtspersonen kunt instellen en genereren in Nederland.
author: anasyash
ms.author: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Netherlands
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 62fd9705db65b89677f455ee2ef07b41f6fa29de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816871"
---
# <a name="vat-declaration-for-the-netherlands"></a>Btw-aangifte voor Nederland

[!include [banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u de btw-aangifte voor rechtspersonen kunt instellen en genereren in Nederland. Zie [Btw-aangifte voor Europa](emea-vat-reporting.md) voor algemene informatie over het opstellen van het btw-overzicht.

## <a name="set-up-sales-tax-reporting-codes-for-vat-reporting"></a>Btw-codes instellen voor btw-aangifte

Stel btw-aangiftecodes in door de instructies te volgen in [Btw-aangiftecodes instellen](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/SE-VAT-declaration/articles/finance/general-ledger/tasks/set-up-sales-tax-reporting-codes.md). De volgende tabel bevat een voorbeeld van btw-aangiftecodes voor Nederland.

| **Btw-rapportcode** | **Beschrijving**                                                                                                                                                                                                 | **Overeenkomstig vak in de aangifte** | **Element in XML**                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|--------------------------------------------------------------|
| 110                          | De fiscale basis voor leveringen/diensten waarvoor 21 procent wordt berekend.                                                                                                                                                | 1a (basis)                                | TaxedTurnoverSuppliesServicesGeneralTariff                   |
| 111                          | Het fiscale bedrag voor leveringen/diensten die tegen 21 procent worden belast.                                                                                                                                                | 1a (belasting)                                 | ValueAddedTaxSuppliesServicesGeneralTariff                   |
| 120                          | De fiscale basis voor leveringen/diensten waarvoor 9 procent wordt berekend.                                                                                                                                                 | 1b (basis)                                | TaxedTurnoverSuppliesServicesReducedTariff                   |
| 121                          | Het fiscale bedrag voor leveringen/diensten die tegen 9 procent worden belast.                                                                                                                                                 | 1b (belasting)                                 | ValueAddedTaxSuppliesServicesReducedTariff                   |
| 130                          | De fiscale basis voor leveringen/diensten waarvoor andere tarieven, behalve 0 procent, worden berekend.                                                                                                                             | 1c (basis)                                | TaxedTurnoverSuppliesServicesOtherRates                      |
| 131                          | Het fiscale bedrag voor leveringen/diensten die met andere tarieven, behalve 0 procent, worden belast.                                                                                                                             | 1c (belasting)                                 | ValueAddedTaxSuppliesServicesOtherRates                      |
| 140                          | Persoonlijk gebruik (basis).                                                                                                                                                                                             | 1d (basis)                                | TaxedTurnoverPrivateUse                                      |
| 141                          | Privégebruik (belastingbedrag).                                                                                                                                                                                       | 1d (belasting)                                 | ValueAddedTaxPrivateUse                                      |
| 150                          | De fiscale basis voor leveringen/diensten waarvoor 0 procent wordt berekend of die niet worden belast.                                                                                                                           | 1e                                       | SuppliesServicesNotTaxed                                     |
| 210                          | Belastingbasis voor leveringen/diensten waarbij de betaling van btw naar u is verlegd (terugboeking).                                                                                                         | 2a (basis)                                | TurnoverSuppliesServicesByWhichVATTaxationIsTransferred      |
| 211                          | Belastingbedrag voor leveringen/diensten waarbij de betaling van btw naar u is verlegd (terugboeking).                                                                                                       | 2a (belasting)                                 | ValueAddedTaxSuppliesServicesByWhichVATTaxationIsTransferred |
| 310                          | Belastingbasis voor leveringen aan landen of regio's buiten de Europese Unie (EU).                                                                                                                                | 3a                                       | SuppliesToCountriesOutsideTheEC                              |
| 320                          | De belastingbasis voor leveringen aan landen in de EU.                                                                                                                                                                 | 3b                                       | SuppliesToCountriesWithinTheEC                               |
| 330                          | Belastingbasis voor installatie en verkoop op afstand in de EU.                                                                                                                                                       | 3c                                       | InstallationDistanceSalesWithinTheEC                         |
| 410                          | Belastingbasis voor leveringen uit landen of regio's buiten de EU.                                                                                                                                               | 4a (basis)                                | TurnoverFromTaxedSuppliesFromCountriesOutsideTheEC           |
| 411                          | Belastingbedrag voor leveringen uit landen of regio's buiten de EU.                                                                                                                                             | 4a (belasting)                                 | ValueAddedTaxOnSuppliesFromCountriesOutsideTheEC             |
| 420                          | Belastingbasis voor de verwerving van goederen uit landen in de EU.                                                                                                                                                 | 4b (basis)                                | TurnoverFromTaxedSuppliesFromCountriesWithinTheEC            |
| 421                          | Belastingbedrag voor de verwerving van goederen uit landen in de EU.                                                                                                                                               | 4b (belasting)                                 | ValueAddedTaxOnSuppliesFromCountriesWithinTheEC              |
| 510                          | Totaal te betalen btw. De waarde in dit vak wordt automatisch berekend als de som van de aangiftecodes 111, 121, 131, 141, 211, 411 en 421.                                                                      | 5a                                       | ValueAddedTaxOwed                                            |
| 521                          | Invoer-btw voor aftrek.                                                                                                                                                                                            | 5b                                       | ValueAddedTaxOnInput                                         |
| 541                          | Belastingvermindering onder de kleineondernemersregeling.                                                                                                                                                                   | 5d                                       | SmallEnterpreneurProvisionReduction                          |
| 571                          | Het netto btw-bedrag dat aan de belastingdienst wordt betaald of wordt teruggevorderd. De waarde in dit vak wordt automatisch berekend als aangiftecode 510 minus aangiftecode 521, plus aangiftecodes 541, 551 en 561. | 5g                                       | ValueAddedTaxOwedToBePaidBack                                |


## <a name="set-up-sales-tax-codes"></a>Btw-codes instellen

Stel btw-aangiftecodes in door de instructies te volgen in [Btw-codes voor btw-aangiftecodes](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) en [Btw-overzicht](../general-ledger/indirect-taxes-overview.md).

## <a name="set-up-the-ob-declaration"></a>De OB-aangifte instellen

"OB-aangifte" betekent "omzetbelastingaangifte", waarbij omzetbelasting gelijk is aan "btw, belasting toegevoegde waarde".

1. Ga naar **Organisatiebeheer \> Organisaties \> Rechtspersonen**.
2. Voer op de pagina **Rechtspersonen**, in het sneltabblad **Belastingregistratie**, in het veld **Btw-registratienummer** het btw-registratienummer van uw bedrijf in.
3. Selecteer **Registratie-id's** en voer hetzelfde btw-registratienummer in. Zie [Registratie-id's](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/NL-VAT-declaration/articles/finance/localizations/emea-registration-ids.md) voor meer informatie over het instellen van registratie-id's.
4. In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van ER-configuraties (elektronische aangifte) voor de volgende indeling van de btw-aangifte:

-   OB-aangifte (NL)

   Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/NL-VAT-declaration/articles/fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

5. Ga naar **Belasting** \> **Btw** \> **Parameters voor elektronische btw-aangifte**.
6. Selecteer op het tabblad **Algemeen** in het veld **Btw-contacttype** de **belastingplichtige** of **intermediair**.
7. Stel de velden **Contactpersoon-id**, **Initialen contactpersoon**, **Voorvoegsel contactpersoon** en **Telefoon** in.
8. Stel de optie **Bedrijf onderdeel van fiscale groep** in op **Ja** als deze instelling van toepassing is en selecteer vervolgens in het veld **Fiscale groep** de naam van de fiscale groep. De fiscale groepen moeten al zijn gemaakt op de pagina **Btw-nummers**.
9. Selecteer in het veld **Indelingstoewijzing** de indeling **OB-aangifte (NL)** die u eerder hebt gedownload.

    ![Pagina met parameters voor elektronische btw-aangifte, tabblad Algemeen](media/1_Electronic_tax_declaration_parameters.png)

10. Selecteer op het tabblad **Nummerreeksen** in het veld **Nummerreekscode** een nummerreekscode voor de verwijzing **Elektronische OB-aangifte-id** om de nummering van OB-aangiften in te stellen.

## <a name="set-up-electronic-transmission-of-the-vat-declaration-to-digipoort"></a>Elektronische transmissie van de btw-aangifte instellen op Digipoort

Digipoort is de service die wordt gebruikt om aangiften naar de Nederlandse overheid te verzenden. Digipoort werkt als een elektronisch postkantoor: het ontvangt een bericht, controleert het bericht en bevestigt vervolgens de ontvangst van het bericht.
 
### <a name="set-up-azure-key-vault-for-certificate-storage"></a>Azure-sleutelkluis instellen voor certificaatopslag

1. Ga naar **Systeembeheer \> Instellen \> Systeemparameters**.
2. Stel op het tabblad **Algemeen** de optie **Geavanceerd certificaatarchief gebruiken** in op **Ja**.
3. Ga naar **Systeembeheer \> Instellen \> Sleutelkluisparameters**.
4. Selecteer **Nieuw** en stel de velden **Naam** en **Omschrijving** in.
5. Stel op het sneltabblad **Algemeen** de volgende velden in:

- **URL sleutelkluis**: geef de standaard-URL voor Azure-sleutelkluis op.
- **Client sleutelkluis**: geef de interactieve client-id op van de Azure Active Directory (Azure AD)-toepassing die aan de sleutelkluisopslag is gekoppeld voor verificatie.
- **Geheime sleutel voor sleutelkluis**: voer een geheime sleutel in die hoort bij de Azure AD-toepassing die voor verificatie wordt gebruikt voor de sleutelkluisopslag.

6. Selecteer op het sneltabblad **Geheimen** de optie **Toevoegen** en maak regels voor de sleutelkluisgeheimen voor de Digipoort-server- en clientcertificaten.

![Pagina Parameters voor sleutelkluis](media/2_Key_Vault_parameters.png)

Zie [Client voor Azure-sleutelkluis instellen](setting-up-azure-key-vault-client.md) voor meer informatie over het instellen van sleutelkluisparameters.

### <a name="set-up-electronic-tax-declaration-parameters"></a>Parameters voor elektronische belastingaangifte instellen

1. Ga naar **Belasting** \> **Instellen** \> **Btw** \> **Parameters voor elektronische btw-aangifte**.
2. Stel de volgende velden in op het tabblad **Systeem**:

- **Leverings-URL Digipoort**: voer de doel-URL voor de Digipoort-service in. Voer bijvoorbeeld `https://preprod-dgp2.procesinfrastructuur.nl/wus/2.0/aanleverservice/1.2` in.
- **URL van Digipoort-status**: voer de URL in voor de berichtstatus. Voer bijvoorbeeld `https://preprod-dgp2.procesinfrastructuur.nl/wus/2.0/statusinformatieservice/1.2` in.
- **Autorisatieadres**: voer de URL voor de autorisatie in. Voer bijvoorbeeld `http://geenausp.nl` in.
- **Servercertificaat**: selecteer de regel die u hebt gemaakt voor het sleutelkluisgeheim voor het Digipoort-servercertificaat.
- **Clientcertificaat**: selecteer de regel die u hebt gemaakt voor het sleutelkluisgeheim voor het Digipoort-clientcertificaat.

![Parameters voor elektronische btw-aangifte, tabblad Systeem](media/3_Electronic_tax_declaration_parameters.png)

## <a name="generate-and-send-the-ob-declaration"></a>De OB-aangifte genereren en verzenden

1. Ga naar **Belasting \> Aangiften \> Btw \> Elektronische btw-aangifte**.
2. Selecteer **Nieuw**.
3. Stel in het dialoogvenster **Elektronische OB-aangifte** de velden **Vereffeningsperiode** en **Begindatum** in.
4. Selecteer **OK** en bekijk de berekende resultaten.

![Pagina Elektronische OB-aangifte](media/4_Electronic_OB_declaration.png)

5. Selecteer **XML weergeven** om de OB-aangifte in XML-indeling te controleren.
6. Selecteer **XML verzenden** om het bestand naar de belastingdienst Digipoort te verzenden.

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld ziet u hoe u btw-codes en btwaangifte codes kunt instellen, transacties kunt boeken en de Nederlandse btw-aangifte kunt genereren.

1. Ga naar **Belasting \> Indirecte belastingen \> Btw \> Btw-codes** en stel de volgende btw-codes in.

| **Btw-code** | **Percentage** | **Beschrijving**                                                                          |
|--------------------|----------------|------------------------------------------------------------------------------------------|
| NL21               | 21             | Binnenlandse verkoop en inkoop met een tarief van 21 procent.                                    |
| NL9                | 9              | Binnenlandse verkoop en inkoop met een tarief van 9 procent.                                     |
| NLEU21             | 21             | EU-inkoop met een tarief van 21 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.    |
| NLEU9              | 9              | EU-inkoop met een tarief van 9 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.     |
| NLImp21            | 21             | Import met een tarief van 21 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.         |
| NLImp9             | 9              | Import met een tarief van 9 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.          |
| NLRC21             | 21             | Terugboekingen met een tarief van 21 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**. |
| NLRC9              | 9              | Terugboekingen met een tarief van 9 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.  |
| NLEUS              | 0              | EU-verkoop waarvoor de optie **Vrijstelling** is ingesteld op **Ja**.                                  |
| NLThird            | 0              | Exportverkoop waarvoor de optie **Vrijstelling** is ingesteld op **Ja**.                              |

2. Wijs op de pagina **Btw-codes** op het sneltabblad **Rapportinstellingen** aangiftecodes toe aan btw-codes.

   > [!NOTE]
   > De voorgaande configuratie is slechts een voorbeeld en is afhankelijk van de structuur van de btw-codes die worden gebruikt. Als u wilt dat waarden worden berekend en overgeboekt naar de btw-aangifte, moet u voor elke btw-code die in het btw-betalingsproces wordt gebruikt, een relevante btw-aangiftecode instellen in een of meer velden op het tabblad **Rapportinstellingen**.

| **Btw-code** | **Belastbare verkoop** | **Verkoop zonder btw** | **Te betalen btw** | **Belastbare inkopen** | **Te ontvangen btw** | **Belastbare import** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| NL21               | 110               |                   | 111                   |                       | 521                      |                    |             |                    |
| NL9                | 120               |                   | 121                   |                       | 521                      |                    |             |                    |
| NLEU21             |                   |                   |                       |                       |                          | 420                | 521         | 421                |
| NLEU9              |                   |                   |                       |                       |                          | 420                | 521         | 421                |
| NLImp21            |                   |                   |                       |                       |                          | 410                | 521         | 411                |
| NLImp9             |                   |                   |                       |                       |                          | 410                | 521         | 411                |
| NLRC21             |                   |                   |                       |                       |                          | 210                | 521         | 211                |
| NLRC9              |                   |                   |                       |                       |                          | 210                | 521         | 211                |
| NLEUS              |                   | 320               |                       |                       |                          |                    |             |                    |
| NLThird            |                   | 310               |                       |                       |                          |                    |             |                    |

3. Ga naar **Organisatiebeheer \> Organisaties \> Rechtspersonen**.
4. Voer **203118030B12** in het veld **Btw-registratienummer** in op het sneltabblad **Belastingregistratie**.
5. Selecteer **Registratie-id's** en voer hetzelfde btw-registratienummer in.
6. Ga naar **Belasting \> Btw \> Parameters voor elektronische btw-aangifte**.
7. Stel op het tabblad **Algemeen** de volgende velden in op de opgegeven waarden:

    - **Contactpersoon-id:** 203118030B12
    - **Initialen van contactpersoon**: initialen
    - **Voorvoegsel van contactpersoon**: voorvoegsel
    - **Telefoon:** telefoon
    - **Indelingstoewijzing**: OB-aangifte (NL)

8. Ga naar het tabblad **Nummerreeksen** en selecteer een nummerreekscode voor de verwijzing **Id elektronische OB-aangifte**.
9. Boek de volgende transacties.

| **Datum**        | **Transactietype**            | **Nettobedrag** | **Btw-bedrag** | **Btw-code** | **Verwachte belastingbasis: aangiftecode** | **Verwacht belastingbedrag: aangiftecode** | **Overeenkomstig vak in de aangifte** |
|-----------------|---------------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|------------------------------------------|
| 1 januari 2020 | Klantfactuur (binnenland)     | 100            | 21             | NL21               | 110                                    | 111                                      | 1a                                       |
| 1 januari 2020 | Leveranciersfactuur (EU)             | 100            | 9              | NLEU9              | 420                                    | 421 – te betalen belasting 521 – belastingaftrek    | 4b 5b                                    |
| 1 januari 2020 | Leveranciersfactuur (import)         | 100            | 21             | NLImp21            | 410                                    | 411 – te betalen belasting 521 – belastingaftrek    | 4a 5b                                    |
| 1 januari 2020 | Klantfactuur (EU)           | 100            | 0              | NLEUS              | 320                                    | Niet van toepassing                           | 3b                                       |
| 1 januari 2020 | Klantfactuur (export)       | 100            | 0              | NLThird            | 310                                    | Niet van toepassing                           | 3a                                       |
| 1 januari 2020 | Leveranciersfactuur (terugboeking) | 100            | 9              | NLRC9              | 210                                    | 211 – te betalen belasting 521 – belastingaftrek    | 2a 5b                                    |

10. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Elektronische btw-aangifte**.
11. Selecteer **Nieuw** en stel in het dialoogvenster dat verschijnt de volgende velden in op de opgegeven waarden:

    - **Vereffeningsperiode:** maand
    - **Begindatum:** 1-1-2020

12. Selecteer **OK**. Controleer de koptekst die voor de aangifte is gegenereerd.

![Pagina Elektronische OB-aangifte, gegenereerde koptekst](media/5_Electronic_OB_declaration.png)

13. Controleer de gegevens die voor de aangifte zijn gegenereerd.

![Paginadetails Elektronische OB-aangifte](media/6_Details.png)

14. Selecteer **XML weergeven** als u een voorbeeld van het XML-bestand wilt bekijken.

![XML-voorbeeld](media/7_XML.png)

### <a name="correction-transactions"></a>Correctietransacties


Boek een nieuwe transactie. Als u bijvoorbeeld een klantfactuur wilt boeken, gaat u naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**.

| **Datum**        | **Transactietype**        | **Nettobedrag** | **Btw-bedrag** | **Btw-code** | **Verwachte belastingbasis: aangiftecode** | **Verwacht belastingbedrag: aangiftecode** | **Overeenkomstig vak in de aangifte** |
|-----------------|-----------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|------------------------------------------|
| 1 januari 2020 | Klantfactuur (binnenland) | 100            | 9              | NL9                | 120                                    | 121                                      | 1b                                       |

1. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Elektronische btw-aangifte**.
2. Selecteer **Nieuw** en stel in het dialoogvenster dat verschijnt de volgende velden in op de opgegeven waarden:

   - **Vereffeningsperiode:** maand
   - **Begindatum:** 1-1-2020

3. Selecteer **OK** en bekijk de aangiftegegevens.

![Paginadetails Elektronische OB-aangifte](media/8_Details.png)

 Een schermopname van een mobiele telefoon met een omschrijving die automatisch wordt gegenereerd

> [!NOTE]
> Er wordt een correctietransactie toegevoegd aan de aangifte in de codes **120** en **121**.

## <a name="review-declaration-amounts-in-printed-form"></a>Aangiftebedragen in afgedrukte vorm bekijken

### <a name="set-up-the-report-layout-for-sales-tax-authorities"></a>De rapportindeling voor btw-diensten instellen

1. Ga naar **Belasting \> Indirecte belastingen \> Btw \> Btw-dienst**.
2. Selecteer op de pagina **Btw-diensten** de btw-dienst die in de btw-codes wordt gebruikt voor de btw-vereffeningsperiode.
3. Selecteer **Indeling Nederlandse aangifte** in het veld **Rapport indeling**.

### <a name="generate-a-sales-tax-payment-and-print-the-dutch-sales-tax-report"></a>Een btw-betaling genereren en de Nederlandse btw-aangifte afdrukken

De btw-bedragen voor de vereffeningsperiode worden aan het einde van de btw-verslagperiode berekend.

1. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw vereffenen en boeken**.
2. Stel de volgende velden in het dialoogvenster **Btw vereffenen en boeken** in.

| **Veld**                 | **Beschrijving**                                                                                                                                                                                                                                                                         |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vereffeningsperiode         | Selecteer de toepasselijke aangifteperiode.                                                                                                                                                                                                                                                 |
| Begindatum                 | Voer de eerste datum van de btw-vereffeningsperiode in waarvoor btw moet worden berekend. Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**.                                                                                 |
| Transactiedatum          | Voer de datum in waarvoor de btw-aangifte wordt berekend. De standaardwaarde is de huidige datum. De btw-betaling wordt berekend voor alle transacties die zijn geboekt tijdens de vereffeningsperiode.                                                                                  |
| Versie van btw-betaling | Selecteer het type btw-vereffening. Selecteer **Origineel** als deze btw-vereffening de eerste btw-vereffening voor de periode is. Als er al een btw-vereffening is gegenereerd, selecteert u **Laatste correcties**. Zie voor meer informatie Een btw-betaling maken. |

3. Selecteer **OK** om de btw-betaling te genereren.

### <a name="print-a-sales-tax-payment-report-from-a-sales-tax-payment"></a>Een btw-betalingsrapport van een btw-betaling afdrukken

1. Ga naar **Belasting** \> **Query's en rapporten** \> **Btw-betalingen**.
2. Selecteer op de pagina **Btw-betalingen** de record en vervolgens **Rapport afdrukken**.
3. Stel in het dialoogvenster de velden in zoals beschreven in de vorige sectie en selecteer vervolgens **OK**.

### <a name="report-sales-tax-for-the-settlement-period"></a>Btw aangeven voor de vereffeningsperiode

U kunt ook de Nederlandse btw-aangifte genereren met de query **Btw rapporteren voor vereffeningsperiode**.

1. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw rapporteren voor vereffeningsperiode**.
2. Stel in het dialoogvenster de velden **Vereffeningsperiode** en **Begindatum** in zoals is beschreven in het gedeelte Een btw-betaling genereren en de Nederlandse btw-aangifte afdrukken eerder in dit onderwerp.
3. Selecteer in het veld **Versie van btw-betaling** een van de volgende waarden:

- **Origineel**: genereer een rapport voor btw-transacties van de eerste geboekte vereffeningsberekening voor de periode.
- **Correcties**: genereer een rapport voor btw-transacties van volgende vereffeningsberekeningen voor de periode.
- **Totaal overzicht** : genereer een rapport voor alle verkooptransacties voor de periode. Deze transacties omvatten originele en gecorrigeerde transacties.

4. Selecteer **OK**.
5. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw vereffenen en boeken**. Selecteer in het dialoogvenster **Btw vereffenen en boeken** in het veld **Versie van btw-betaling** de optie **Origineel**.
6. Druk het rapport af en controleer de gegevens.

![Gegenereerd btw-betalingsrapport](media/9_Sales_tax_payment.png)

  Let op de volgende punten:

- Vak 5e komt overeen met rapporteringscode 551.
- Vak 5f komt overeen met rapporteringscode 561.
- De vakken 6a en 6b zijn niet ingevuld.

   Deze waarden zijn niet aanwezig in de XML voor de OB-aangifte.

4. Boek de nieuwe transactie.

| **Datum**   | **Transactietype**        | **Nettobedrag** | **Btw-bedrag** | **Btw-code** | **Verwachte belastingbasis: aangiftecode** | **Verwacht belastingbedrag: aangiftecode** |
|------------|-----------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| 1 januari 2020 | Klantfactuur (binnenland) | 100            | 9              | NL9                | 120                                    | 121                                      |

5. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw vereffenen en boeken**. Selecteer in het dialoogvenster **Btw vereffenen en boeken** in het veld **Versie van btw-betaling** de optie **Laatste correcties**.
6. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw rapporteren voor vereffeningsperiode**. Selecteer **Correcties** in het veld **Versie van btw-betaling**. Het volgende resultaat wordt weergegeven.

![Gegenereerd btw-betalingsrapport](media/10_Sales_tax_payment.png)

7. Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw rapporteren voor vereffeningsperiode**. Selecteer **Totaal overzicht** in het veld **Versie van btw-betaling**. Het volgende resultaat wordt weergegeven.

![Gegenereerd btw-betalingsrapport](media/11_Sales_tax_payment.png)

   > [!NOTE]
   > Als u de OB-aangifte genereert nadat u de oorspronkelijke en gecorrigeerde btw-betalingen hebt gemaakt, worden in de OB-aangifte alleen bedragen weergegeven van de oorspronkelijke btw-betaling.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]