---
title: Btw-aangifte (België)
description: Dit artikel bevat informatie over de btw-aangifte voor België.
author: anasyash
ms.date: 06/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Belgium
ms.author: anasyash
ms.search.validFrom: 2019-01-04
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5a16493e56c306e1abd3880b73a336da536249ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904307"
---
# <a name="vat-declaration-belgium"></a>Btw-aangifte (België)

[!include [banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u de btw-aangifte voor België in XML-indeling kunt instellen en hoe u een voorbeeld kunt bekijken van de btw-aangifte en verkoop- en inkooptransacties in Microsoft Excel.

Als u de aangiftes automatisch wilt genereren, maakt u eerst voldoende btw-codes om een afzonderlijke btw-boekhouding bij te houden voor elk vak in de btw-aangifte. In de toepassingsspecifieke parameters van de ER-indeling (elektronische aangifte) voor de btw-aangifte koppelt u bovendien btw-codes aan het zoekresultaat van de zoekopdrachten voor de vakken in de btw-aangifte.

Voor België moet u de volgende elementen configureren:

- Zoekopdracht voor rapportveld
- Aard
- Voorschotten die zijn gerelateerd aan intracommunautaire verwervingen

Zie de sectie [Toepassingsspecifieke parameters instellen voor btw-aangiftevelden](#set-up-application-specific-parameters-for-vat-declaration-fields) verderop in dit artikel voor meer informatie over het instellen van toepassingsspecifieke parameters.

In de volgende tabel ziet u in de kolom 'Opzoekresultaat' het opzoekresultaat dat vooraf is geconfigureerd voor een specifieke btw-aangifterij in de indeling voor de btw-aangifte. Gebruik deze informatie om btw-codes correct aan het opzoekresultaat en vervolgens aan de rij van de btw-aangifte te koppelen.

## <a name="vat-declaration-overview"></a>Overzicht van btw-aangifte

De btw-aangifte in België bevat de volgende informatie.

**SECTIE II UITGAANDE ACTIVITEITEN**

U kunt de volgende tabel gebruiken om te bepalen hoe een opzoekresultaat dat vooraf in de indeling is geconfigureerd, wordt gekoppeld aan een btw-aangiftevak.

Een opzoekresultaat kan een bedrag in diverse vakken genereren. Die vakken worden tussen haakjes weergegeven. Voor het opzoekresultaat van **01_SalesLowerReducedRate** geeft (01/54) bijvoorbeeld aan dat het btw-basisbedrag van de transactie wordt weergegeven in vak 01 en het btw-bedrag van de transactie wordt weergegeven in vak 54.

| Description   | Doos | Opzoekresultaat van opzoekactie in veld voor aangifte (btw-basis)   |
|---------------|-----|---------------------------------------------------|
| A. Activiteiten waarvoor een speciale regeling geldt    | 00  | 00_ExemptSalesSpecialScheme    |
| B. Transacties waarvoor de btw moet worden betaald door de declarant:              | &nbsp;    |   &nbsp;  |
| \- tegen een tarief van 6 procent.     | 01  | 01_SalesLowerReducedRate (01/54)   |
| \- tegen een tarief van 12 procent.    | 02  | 02_SalesHigherReducedRate (02/54)  |
| \- tegen een tarief van 21 procent.    | 03  | 03_SalesStandardRate (03/54)       |
| C. Diensten waarvoor de buitenlandse btw door de contracterende partner moet worden betaald | 44  | 44_ForeignSalesServicesReverseCharge  |
| D. Transacties waarvoor de btw door de contracterende partner moet worden betaald     | 45  | 45_SalesReverseCharge  |
| E. Intracommunautaire leveringen vrijgesteld in België en ABC-verkoop        | 46  | 46_EUSales  |
| F. Overige vrijgestelde activiteiten en andere in het buitenland uitgevoerde activiteiten        | 47  | 47_OtherExemptSales  |
| G. Bedrag aan uitgegeven creditnota's en negatieve correcties:              | &nbsp;    | &nbsp;     |
| \- met betrekking tot de activiteiten die in de rasters 44 en 46 zijn geregistreerd          | 48  | **Opzoekresultaten voor creditnota's:** 48_ForeignSalesServicesReverseChargeCreditNoteCorr</br> 48_EUSalesCreditNoteCorr    |
| \- met betrekking tot andere activiteiten van Sectie II    | 49  | **Opzoekresultaten voor creditnota's:** 49_ExemptSalesSpecialSchemeCreditNoteCorr</br> 49_SalesStandardRateCreditNote (49/64)</br> 49_SalesHigherReducedRateCreditNote (49/64)</br> 49_SalesLowerReducedRateCreditNote (49/64)</br> 49_SalesLowerReducedRateNegativeCorrection (49/62)</br> 49_SalesHigherReducedRateNegativeCorrection (49/62)</br> 49_SalesStandardRateNegativeCorrection (49/62)</br> 49_SalesReverseChargeCreditNoteCorr</br> 49_OtherExemptSalesCreditNoteCorr |

**SECTIE III BINNENKOMENDE ACTIVITEITEN**

U kunt de volgende tabel gebruiken om te bepalen hoe een opzoekresultaat dat vooraf in de indeling is geconfigureerd, wordt gekoppeld aan een btw-aangiftevak.

Een opzoekresultaat kan een bedrag in verschillende vakken genereren en de bedragen kunnen verschillende tekens hebben. Die vakken en tekens worden tussen haakjes weergegeven. Voor het opzoekresultaat **8185_PurchasesGoodsCreditNote** geeft (-81 +85/63) bijvoorbeeld aan dat het btw-basisbedrag van de transactie in vak 81 wordt weergegeven als een negatieve waarde en in vak 85 als een positieve waarde. Het btw-bedrag van de transactie wordt in vak 63 weergegeven als een positieve waarde.

> [!NOTE]
> De vakken 81, 82 en 83 bevatten altijd het btw-basisbedrag plus het bedrag van de niet-aftrekbare btw. Andere vakken in deze sectie bevatten het btw-basisbedrag.

| Description    | Doos | Opzoekresultaat van opzoekactie in veld voor aangifte |
|----------------|-----|--------------------------------------|
| A. Aantal inkomende activiteiten rekening houdend met de ontvangen creditnota's en andere correcties:</br>  \- goederen, grondstoffen en verbruiksartikelen    | 81  | 81_PurchasesGoods (81/59)</br> 81_PurchasesGoodsRegularizations (-81 +61)</br> **Opzoekresultaat voor creditnota's:**</br> 8185_PurchasesGoodsCreditNote (-81 +85/63)</br> **Opzoekresultaten voor gebruiksbelasting:**</br> 8681_EUPurchasesGoodsUseTax (86/81 55/59)</br> 8781_OtherPurchasesDomesticReverseChargeGoodsUseTax (87/81 56/59)</br> 8781_OtherPurchasesImportsDeferredTaxGoodsUseTax (87/81 57/59)</br> **Opzoekresultaten voor creditnota's met gebruiksbelasting:**</br> 868184_EUPurchasesGoodsCreditNoteUseTax (-86/81 +84/61/62)</br> 878185_OtherPurchasesDomesticReverseChargeGoodsCNUseTax (-87/81 +85/61/62)</br> 878185_OtherPurchasesImportsDeferredTaxGoodsCNUseTax (-87/81 +85/61/62)  |
| \- diensten en diverse goederen  | 82  | 82_PurchasesServicesMisc (82/59)</br>  82_PurchasesServicesRegularizations (-82 +61)</br> **Opzoekresultaat voor creditnota's:**</br> 8285_PurchasesServicesMiscCreditNote (-82 +85/63)</br> **Opzoekresultaten voor gebruiksbelasting:**</br> 8682_EUPurchasesMiscUseTax (86/82 55/59)</br> 8782_OtherPurchasesDomesticReverseChargeMiscUseTax (87/82 56/59)</br> 8782_OtherPurchasesImportsDeferredTaxMiscUseTax (87/82 57/59)</br> 8882_EUPurchasesServicesUseTax (88/82 55/59)</br> **Opzoekresultaten voor creditnota's met gebruiksbelasting:**</br> 868284_EUPurchasesMiscCreditNoteUseTax (-86/82 +84/61/62)</br> 878285_OtherPurchasesDomesticReverseChargeMiscCNUseTax (-87/82 +85/61/62)</br> 878285_OtherPurchasesImportsDeferredTaxMiscCNUseTax (-87/82 +85/61/62)</br> 888284_EUPurchasesServicesCreditNoteUseTax (-88/82 +84/61/62)  |
| \- bedrijfsactiva   | 83  | 83_PurchasesCapitalGoods (83/59)</br>  83_PurchasesCapitalGoodsRegularizations (-83 +61)</br>  **Opzoekresultaat voor creditnota's:**</br>  8385_PurchasesCapitalGoodsCreditNote (-83 +85/63)</br>  **Opzoekresultaten voor gebruiksbelasting:**</br>  8683_EUPurchasesCapitalGoodsUseTax (86/83 55/59)</br>  8783_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (87/83 56/59) </br> 8783_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (87/83 57/59)</br>  **Opzoekresultaten voor creditnota's met gebruiksbelasting:**</br>  868384_EUPurchasesCapitalGoodsCreditNoteUseTax (-86/83 +84/61/62)</br>  878385_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (-87/83 +85/61/62) </br> 878385_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (-87/83 +85/61/62)  |
| B. Bedrag aan ontvangen creditnota's en negatieve correcties:  |  &nbsp;   |  &nbsp;  |
| \- met betrekking tot de activiteiten die in de vakken 86 en 88 zijn geregistreerd   | 84  | **Opzoekresultaten voor creditnota's:**</br>  8684_EUPurchasesCreditNoteRC (-86 +84/62)</br>  8884_EUPurchasesServicesCreditNoteRC (-88 +84/62)</br>  **Opzoekresultaten voor creditnota's met gebruiksbelasting:**</br>  868184_EUPurchasesGoodsCreditNoteUseTax (-86/81 +84/61/62)</br>  868284_EUPurchasesMiscCreditNoteUseTax (-86/82 +84/61/62)</br>  868384_EUPurchasesCapitalGoodsCreditNoteUseTax (-86/83 +84/61/62)</br>  888284_EUPurchasesServicesCreditNoteUseTax (-88/82 +84/61/62)  |
| \- met betrekking tot de overige activiteiten van Vak III   | 85  | **Opzoekresultaten voor creditnota's:**</br>  8185_PurchasesGoodsCreditNote (-81 +85/63)</br>  8285_PurchasesServicesMiscCreditNote (-82 +85/63)</br>  8785_OtherPurchasesImportsDeferredTaxCreditNote (-87 +85/62)</br>  **Opzoekresultaten voor creditnota's met gebruiksbelasting:**</br>  878185_OtherPurchasesDomesticReverseChargeGoodsCNUseTax (-87/81 +85/61/62)</br>  878285_OtherPurchasesDomesticReverseChargeMiscCNUseTax (-87/82 +85/61/62)</br>  878385_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (-87/83 +85/61/62)</br>  878185_OtherPurchasesImportsDeferredTaxGoodsCNUseTax (-87/81 +85/61/62)</br>  878285_OtherPurchasesImportsDeferredTaxMiscCNUseTax (-87/82 +85/61/62)</br>  878385_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (-87/83 +85/61/62)   |
| C. Intracommunautaire verwervingen uitgevoerd in België en ABC-verkoop   | 86  | 86_EUPurchasesRC (86/55)</br>  **Opzoekresultaat voor creditnota's:**</br>  8684_EUPurchasesCreditNoteRC (-86 +84/62)</br>  **Opzoekresultaten voor gebruiksbelasting:**</br>  8681_EUPurchasesGoodsUseTax (86/81 55/59)</br>  8682_EUPurchasesMiscUseTax (86/82 55/59)</br>  8683_EUPurchasesCapitalGoodsUseTax (86/83 55/59)</br>  **Opzoekresultaten voor creditnota's met gebruiksbelasting:** </br> 868184_EUPurchasesGoodsCreditNoteUseTax (-86/81 +84/61/62)</br>  868284_EUPurchasesMiscCreditNoteUseTax (-86/82 +84/61/62) </br> 868384_EUPurchasesCapitalGoodsCreditNoteUseTax (-86/83 +84/61/62)   |
| D. Overige binnenkomende activiteiten waarvoor de btw moet worden betaald door de declarant    | 87  | 87_OtherPurchasesDomesticReverseCharge (87/56) </br> 87_OtherPurchasesImportsDeferredTax (87/57)</br>  **Opzoekresultaten voor creditnota's:**</br>  8785_OtherPurchasesDomesticReverseChargeCreditNote (-87 +85/62) </br> 8785_OtherPurchasesImportsDeferredTaxCreditNote (-87 +85/62)</br>  **Opzoekresultaten voor gebruiksbelasting:**</br>  8781_OtherPurchasesImportsDeferredTaxGoodsUseTax (87/81 57/59)</br>  8782_OtherPurchasesImportsDeferredTaxMiscUseTax (87/82 57/59)</br>  8783_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (87/83 57/59) </br> 8781_OtherPurchasesDomesticReverseChargeGoodsUseTax (87/81 56/59)</br>  8782_OtherPurchasesDomesticReverseChargeMiscUseTax (87/82 56/59) </br> 8783_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (87/83 56/59)</br>  **Opzoekresultaten voor creditnota's met gebruiksbelasting:** </br> 878185_OtherPurchasesImportsDeferredTaxGoodsCNUseTax (-87/81 +85/61/62)</br>  878285_OtherPurchasesImportsDeferredTaxMiscCNUseTax (-87/82 +85/61/62) </br> 878385_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (-87/83 +85/61/62)</br>  878185_OtherPurchasesDomesticReverseChargeGoodsCNUseTax (-87/81 +85/61/62) </br> 878285_OtherPurchasesDomesticReverseChargeMiscCNUseTax (-87/82 +85/61/62)</br>  878385_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (-87/83 +85/61/62) |
| E. Intracommunautaire diensten met omgekeerde toeslag    | 88  | 88_EUPurchasesServicesRC (88/55)</br>  **Opzoekresultaat voor creditnota's:**</br>  8884_EUPurchasesServicesCreditNoteRC (-88 +84/62)</br>  **Opzoekresultaat voor gebruiksbelasting:**</br>  8882_EUPurchasesServicesUseTax (88/82 55/59) </br> **Opzoekresultaat voor creditnota's met gebruiksbelasting:**</br>  888284_EUPurchasesServicesCreditNoteUseTax (-88/82 +84/61/62)    |

**SECTIE IV TE BETALEN BTW**

U kunt de volgende tabel gebruiken om te bepalen hoe een opzoekresultaat dat vooraf in de indeling is geconfigureerd, wordt gekoppeld aan een btw-aangiftevak.

| Description   | Doos    | Opzoekresultaat van opzoekactie in veld voor aangifte   |
|---------------|--------|----------------------------------------|
|A. Btw op de activiteiten die worden aangegeven in:</br>  \- de vakken 01, 02 en 03     | 54    | 01_SalesLowerReducedRate (01/54)</br> 02_SalesHigherReducedRate (02/54)</br> 03_SalesStandardRate (03/54)   |
| \- de vakken 86 en 88  | 55  | 86_EUPurchasesRC (86/55)</br> 88_EUPurchasesServicesRC (88/55)</br> **Opzoekresultaten voor gebruiksbelasting:**</br> 8681_EUPurchasesGoodsUseTax (86/81 55/59)</br> 8682_EUPurchasesMiscUseTax (86/82 55/59)</br> 8882_EUPurchasesServicesUseTax (88/82 55/59) </br>8683_EUPurchasesCapitalGoodsUseTax (86/83 55/59) |
| \- vak 87, met uitzondering van import met omgekeerde toeslag | 56   | 87_OtherPurchasesDomesticReverseCharge (87/56)</br> **Opzoekresultaten voor gebruiksbelasting:** </br>8781_OtherPurchasesDomesticReverseChargeGoodsUseTax (87/81 56/59)</br> 8782_OtherPurchasesDomesticReverseChargeMiscUseTax (87/82 56/59) </br>8783_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (87/83 56/59)  |
| B. Btw op import met omgekeerde toeslag  | 57   | 87_OtherPurchasesImportsDeferredTax (87/57)</br> **Opzoekresultaten voor gebruiksbelasting:** </br>8781_OtherPurchasesImportsDeferredTaxGoodsUseTax (87/81 57/59)</br> 8782_OtherPurchasesImportsDeferredTaxMiscUseTax (87/82 57/59) </br>8783_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (87/83 57/59)   |
| C. Diverse btw-regularisaties ten gunste van de staat   | 61   | 61_VATRegularizationsDue</br> 81_PurchasesGoodsRegularizations (-81 +61)</br> 82_PurchasesServicesRegularizations (-82 +61)</br> 83_PurchasesCapitalGoodsRegularizations (-83 +61)</br> **Opzoekresultaten voor creditnota's met gebruiksbelasting:** </br>868184_EUPurchasesGoodsCreditNoteUseTax (-86/81 +84/61/62)</br> 868284_EUPurchasesMiscCreditNoteUseTax (-86/82 +84/61/62)</br> 868384_EUPurchasesCapitalGoodsCreditNoteUseTax (-86/83 +84/61/62)</br> 878185_OtherPurchasesDomesticReverseChargeGoodsCNUseTax (-87/81 +85/61/62)</br> 878285_OtherPurchasesDomesticReverseChargeMiscCNUseTax (-87/82 +85/61/62)</br> 878385_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (-87/83 +85/61/62) </br>878185_OtherPurchasesImportsDeferredTaxGoodsCNUseTax (-87/81 +85/61/62)</br> 878285_OtherPurchasesImportsDeferredTaxMiscCNUseTax (-87/82 +85/61/62) </br>878385_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (-87/83 +85/61/62)</br> 888284_EUPurchasesServicesCreditNoteUseTax (-88/82 +84/61/62)</br> |
| D. Terug te betalen btw, vermeld op ontvangen creditnota's   | 63  | **Opzoekresultaten voor creditnota's:**</br> 8185_PurchasesGoodsCreditNote (-81 +85/63) </br>8285_PurchasesServicesMiscCreditNote (-82 +85/63)</br> 8385_PurchasesCapitalGoodsCreditNote (-83 +85/63)     |
| **Totaal van de vakken 54, 55, 56, 57, 61 en 63**    | **XX** | **54 + 55 + 56 + 57 + 61 + 63**    |

**SECTIE V AFTREKBARE BELASTING**

U kunt de volgende tabel gebruiken om te bepalen hoe een opzoekresultaat dat vooraf in de indeling is geconfigureerd, wordt gekoppeld aan een btw-aangiftevak.

| Description  | Doos    | Opzoekresultaat van opzoekactie in veld voor aangifte  |
|--------------|--------|---------------------------------------|
| A. Aftrekbare btw  | 59  | 81_PurchasesGoods (81/59)</br> 82_PurchasesServicesMisc (82/59)</br> 83_PurchasesCapitalGoods (83/59)</br> **Opzoekresultaten voor gebruiksbelasting:**</br> 8681_EUPurchasesGoodsUseTax (86/81 55/59)</br> 8682_EUPurchasesMiscUseTax (86/82 55/59) </br>8683_EUPurchasesCapitalGoodsUseTax (86/83 55/59)</br> 8781_OtherPurchasesDomesticReverseChargeGoodsUseTax (87/81 56/59) </br>8782_OtherPurchasesDomesticReverseChargeMiscUseTax (87/82 56/59)</br> 8783_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (87/83 56/59) </br>8781_OtherPurchasesImportsDeferredTaxGoodsUseTax (87/81 57/59)</br> 8782_OtherPurchasesImportsDeferredTaxMiscUseTax (87/82 57/59) </br>8783_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (87/83 57/59)</br> 8882_EUPurchasesServicesUseTax (88/82 55/59) |
| B. Diverse btw-regularisaties ten gunste van de declarant | 62  | 62_VATRegularizationsDeduction</br> **Opzoekresultaten voor creditnota's en correcties:** </br>49_SalesLowerReducedRateNegativeCorrection (49/62)</br> 49_SalesHigherReducedRateNegativeCorrection (49/62)</br> 49_SalesStandardRateNegativeCorrection (49/62) </br>8684_EUPurchasesCreditNoteRC (-86 +84/62)</br> 8884_EUPurchasesServicesCreditNoteRC (-88 +84/62)</br> 8785_OtherPurchasesImportsDeferredTaxCreditNote (-87 +85/62) </br>8785_OtherPurchasesDomesticReverseChargeCreditNote (-87 +85/62)</br> 8884_EUPurchasesServicesCreditNoteRC (-88 +84/62)</br> **Opzoekresultaten voor creditnota's met gebruiksbelasting:**</br>868184_EUPurchasesGoodsCreditNoteUseTax (-86/81 +84/61/62)</br> 868284_EUPurchasesMiscCreditNoteUseTax (-86/82 +84/61/62) </br>868384_EUPurchasesCapitalGoodsCreditNoteUseTax (-86/83 +84/61/62)</br> 878185_OtherPurchasesDomesticReverseChargeGoodsCNUseTax (-87/81 +85/61/62) </br>878285_OtherPurchasesDomesticReverseChargeMiscCNUseTax (-87/82 +85/61/62)</br> 878385_OtherPurchasesDomesticReverseChargeCapitalGoodsUseTax (-87/83 +85/61/62)</br> 878185_OtherPurchasesImportsDeferredTaxGoodsCNUseTax (-87/81 +85/61/62)</br> 878285_OtherPurchasesImportsDeferredTaxMiscCNUseTax (-87/82 +85/61/62) </br>878385_OtherPurchasesImportsDeferredTaxCapitalGoodsUseTax (-87/83 +85/61/62)</br> 888284_EUPurchasesServicesCreditNoteUseTax (-88/82 +84/61/62) |
| C. Terug te vorderen btw, vermeld op uitgegeven creditnota's   | 64   | **Opzoekresultaten voor creditnota's:**</br> 49_SalesStandardRateCreditNote (49/64)</br> 49_SalesHigherReducedRateCreditNote (49/64)</br> 49_SalesLowerReducedRateCreditNote (49/64)  |
| **Totaal van de vakken 59, 62 en 64**    | **YY** | **59 + 62 + 64**  |

**SECTIE VI SALDO**

| Description                                           | Doos | Berekening           |
|-------------------------------------------------------|-----|-----------------------|
| Slechts één van de twee volgende vakken kan worden ingevuld: |     |                       |
| Belasting verschuldigd aan de staat: vak XX - vak YY                 | 71  | XX – YY, als XX \>= YY |
| Bedragen verschuldigd door de staat: vak YY - vak XX            | 72  | YY – XX, als YY \> XX  |

**SECTIE VII DEPOSITO**

| Description  | Doos | Berekening   |
|--------------|-----|---------------|
| Werkelijke btw verschuldigd voor de periode van 1 tot 20 december in de maandelijkse aangifte of voor de periode van 1 oktober tot en met 20 december in de kwartaalaangifte | 91  | De invoerparameter **91 Depositobedrag dat in december moet worden betaald** in het dialoogvenster voor gebruikers |

## <a name="purchase-reverse-charge-vat"></a>Omgekeerde toeslag van te vorderen btw

Als u btw-codes configureert om inkomende omgekeerde toeslagen te boeken via gebruiksbelasting, koppelt u uw btw-codes aan het opzoekresultaat van **Rapportveld zoeken** dat "UseTax" in de naam heeft.

U kunt ook twee afzonderlijke btw-codes configureren: één voor te betalen btw en één voor btw-aftrek. Koppel vervolgens elke code aan de bijbehorende opzoekresultaten voor **Rapportveld zoeken**.

Zo configureert u bijvoorbeeld voor belastbare intracommunautaire verwervingen met een btw-code **UT_S_EU** met gebruiksbelasting en koppelt u deze aan het opzoekresultaat **8681_EUPurchasesGoodsUseTax (86/81 55/59)** van **Rapportveld zoeken**. In dit geval worden belastingbedragen die gebruikmaken van btw-code **UT_S_EU** weergegeven in de vakken 59 (Aftrekbare btw) en 55 (Btw op de activiteiten die worden aangegeven in de vakken 86, 88). De belastingbasis wordt weergegeven in de vakken 81 (Bedrag van inkomende activiteiten: goederen, grondstoffen en verbruiksartikelen) en 86 (Intracommunautaire verwervingen uitgevoerd in België en ABC-verkoop).

U kunt ook twee btw-codes configureren:

- **VAT_S_EU**, met een btw-tariefwaarde van -25 procent
- **InVAT_S_EU**, met een btw-tariefwaarde van 25 procent

Vervolgens koppelt u als volgt de codes aan opzoekresultaten van **Rapportveld zoeken**:

- Koppel **VAT_S_EU** aan het opzoekresultaat **EUPurchaseStandard (86/55)**.
- Koppel **InVAT_S_EU** aan het opzoekresultaat **EUPurchaseStandardDeduction (81/59)**.

In dit geval worden bedragen die gebruikmaken van btw-code **VAT_S_EU** weergegeven in de vakken 55 (Btw op de activiteiten die worden aangegeven in de vakken 86, 88) en 86 (Intracommunautaire verwervingen uitgevoerd in België en ABC-verkoop). Bedragen die de btw-code **InVAT_S_EU** gebruiken, worden weergegeven in vakken 59 (Aftrekbare btw) en 81 (Bedrag van inkomende activiteiten: goederen, grondstoffen en verbruiksartikelen).

Zie [Terugboekingen](emea-reverse-charge.md) voor meer informatie over het configureren van omgekeerde toeslagen.

## <a name="credit-notes-and-negative-corrections"></a>Creditnota's en negatieve correcties

In België worden bedragen van creditnota's en negatieve correcties weergegeven in afzonderlijke vakken op de btw-aangifte. Daarom zijn in de voorgaande tabellen specifieke opzoekresultaten voor **Zoekopdracht voor rapportveld** toegewezen aan creditnota's en negatieve correcties.

**Voorbeeld: Verkoop**

Een verkoop van goederen (factuur 1) heeft een btw-basis van 1000,00 euro (EUR) en een btw-bedrag van 210,00 EUR. U kunt deze verkoop zien in de volgende vakken:

- **Vak 03 (Transacties waarvoor de btw moet worden betaald door de declarant: tegen een tarief van 21 procent):** 1000,00
- **Vak 54 (Btw op de activiteiten die worden aangegeven in de vakken 01, 02 en 03):** 210,00

Een creditnota (Creditnota 1) die wordt uitgegeven of een negatieve correctie voor de voorgaande factuur heeft een btw-basis van -300,00 EUR en een btw-bedrag van -63,00 EUR. Deze creditnota of correctie kan in de volgende vakken worden weergegeven:

- **Vak 49 (Bedrag van uitgegeven creditnota's en negatieve correcties met betrekking tot andere activiteiten van Sectie II):** 300,00
- **Vak 64 (Terug te vorderen btw, vermeld op uitgegeven creditnota's):** 63,00

**Voorbeeld: Inkoop**

Een inkoop van goederen (factuur 2) heeft een btw-basis van 1000,00 euro (EUR) en een btw-bedrag van 210,00 EUR. U kunt deze inkoop zien in de volgende vakken:

- **Vak 81 (Aantal inkomende activiteiten rekening houdend met de ontvangen creditnota's en andere correcties - goederen, grondstoffen en verbruiksartikelen):** 1000,00
- **Vak 59 (Niet-aftrekbare btw):** 210,00

Een creditnota (Creditnota 2) die wordt ontvangen of een negatieve correctie voor de voorgaande factuur heeft een btw-basis van -400 EUR en een btw-bedrag van -84 EUR. Deze creditnota of correctie kan in de volgende vakken worden weergegeven:

- **Vak 81 (Aantal inkomende activiteiten rekening houdend met de ontvangen creditnota's en andere correcties - goederen, grondstoffen en verbruiksartikelen):** -400,00
- **Vak 85 (Bedrag van uitgegeven creditnota's en negatieve correcties met betrekking tot de andere activiteiten van Vak III):** 400,00
- **Vak 63 (Terug te betalen btw, vermeld op ontvangen creditnota's):** 84,00

## <a name="sales-transaction-and-purchase-transaction-overview"></a>Overzicht van verkoop- en inkooptransacties

In België kunt u een lijst met verkoop- en inkooptransacties genereren.

In de volgende voorbeelden ziet u hoe deze rapporten er voor de voorbeelden uit de vorige sectie uitzien.

**Voorbeeld: Verkooptransacties**

| Documentnummer | Vak 03   | Vak 54 | Vak 49 | Vak 64 |
|-----------------|----------|--------|--------|--------|
| Factuur 1       | 1,000.00 | 210.00 | 00,00  | 00,00  |
| Creditnota 1   | 00,00    | 00,00  | 300,00 | 63.00  |

**Voorbeeld: Inkooptransacties**

| Documentnummer | Vak 81   | Vak 59 | Vak 85 | Vak 63 |
|-----------------|----------|--------|--------|--------|
| Factuur 2       | 1,000.00 | 210.00 | 00,00  | 00,00  |
| Creditnota 2   | \-400.00 | 00,00  | 400.00 | 84.00  |

## <a name="set-up-a-vat-declaration-for-belgium"></a>Een btw-aangifte instellen voor België

### <a name="configure-system-parameters"></a>Systeemparameters configureren

Voor het genereren van een btw-aangifte moet u het fiscale ondernemingsnummer configureren.

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
2. Selecteer de rechtspersoon en selecteer **Registratie-id's**.
3. Selecteer of maak het adres in België en selecteer vervolgens op het sneltabblad **Registratie-id's** de optie **Toevoegen**.
4. Selecteer in het veld **Registratietype** het registratietype dat is toegewezen aan België en dat gebruikmaakt van de registratiecategorie **Ondernemings-id (COID)**.
5. Voer in het veld **Registratienummer** het belastingnummer met de indeling *BTW BE 1234.567.890* in.
6. Voer op het tabblad **Algemeen** in het veld **Geldig vanaf** de datum in waarop het nummer van kracht wordt.

Zie [Registratie-id's](emea-registration-ids.md) voor meer informatie over het instellen van registratiecategorieën en registratietypen.

### <a name="import-er-configurations"></a>ER-configuraties importeren

- Open de werkruimte **Elektronische rapportage** en importeer de volgende ER-indelingen:
- XML-indeling van btw-aangifte (BE)
- Excel-indeling van btw-aangifte (BE)

Meer informatie is te vinden in [ER-configuraties downloaden uit de Algemene opslagplaats van de configuratieservice](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Toepassingsspecifieke parameters instellen voor btw-aangiftevelden

> [!NOTE]
> U kunt het beste **Toepassingsspecifieke parameters van vorige versies van ER-indelingen** inschakelen in de werkruimte **Functiebeheer**. Wanneer deze functie is ingeschakeld, worden parameters die zijn geconfigureerd voor eerdere versies van een ER-indeling automatisch van toepassing op latere versies van dezelfde indeling. Als deze functie niet is ingeschakeld, moet u toepassingsspecifieke parameters expliciet voor elke indelingsversie configureren. De functie **Toepassingsspecifieke parameters van vorige versies van ER-indelingen** is beschikbaar in de werkruimte **Functiebeheer** vanaf Dynamics 365 Finance-versie 10.0.23. Zie [De parameters voor een ER-indeling per rechtspersoon instellen](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md) voor meer informatie over het instellen van de parameters van een ER-indeling voor elke rechtspersoon.

Als u automatisch een btw-aangifte wilt genereren, koppelt u btw-codes aan de toepassing en zoekresultaten in de ER-configuratie.

#### <a name="set-up-application-specific-parameters-for-report-field-lookup"></a>Toepassingsspecifieke parameters instellen voor Zoekopdracht voor rapportveld

Volg deze stappen om te definiëren door welke btw-codes welke vakken worden gegenereerd in de btw-aangifte.

1. Ga naar **Werkruimten** > **Elektronische rapportage** en selecteer **Rapportageconfiguraties**.
2.  Selecteer de configuratie **Btw-aangifte XML (BE)** en selecteer vervolgens **Configuraties \> Toepassingsspecifieke parameters instellen**.
3.  Selecteer op de pagina **Toepassingsspecifieke parameters** op het sneltabblad **Zoekopdrachten** de optie **Rapportveld zoeken**.
4.  Stel op het sneltabblad **Voorwaarden** de volgende velden in om de btw-codes en rapportvelden te koppelen.

    | Veld     | Description   |
    |-----------|---------------|
    | Zoekresultaat  | Selecteer de waarde van het rapportveld. Zie de sectie eerder in dit artikel [Overzicht van btw-aangifte](#vat-declaration-overview) voor meer informatie over de waarden en hun toewijzing aan rijen voor btw-aangifte.  |
    | Belastingcode   | Selecteer de btw-code die u aan het rapportveld wilt koppelen. Geboekte btw-transacties die de geselecteerde btw-code gebruiken, worden in het desbetreffende aangiftevak verzameld. Het is raadzaam om btw-codes zo te scheiden, dat één btw-code bedragen in slechts één aangiftevak genereert. |
    | Transactieclassificatie | Selecteer een transactieclassificatie. De volgende transactieclassificaties zijn beschikbaar: </br> - **Inkoop** (te ontvangen btw) </br> - **PurchaseExempt** (inkoop met belastingvrijstelling)  </br>- **PurchaseReverseCharge** (terug te ontvangen btw van een omgekeerde toeslag op een inkoopfactuur)  </br> - **Verkoop** (te betalen btw) </br> -  **SalesExempt** (verkoop met btw-vrijstelling) </br>- **SalesReverseCharge** (te betalen btw van een omgekeerde toeslag op een inkoopfactuur) </br>- **Gebruiksbelasting** (gebruiksbelasting) </br> Voor elke transactieclassificatie is er ook een classificatie voor de creditnota beschikbaar. Een van deze classificaties is bijvoorbeeld **PurchaseCreditNote** (creditnota voor inkoop). Zorg ervoor dat u twee regels maakt voor elke btw-code: een met de waarde van de transactieclassificatie en een met de transactieclassificatie voor de waarde van de creditnota.  |

> [!NOTE]
> Koppel alle btw-codes aan opzoekresultaten. Als btw-codes geen waarden op de btw-aangifte moeten genereren, koppelt u deze aan het opzoekresultaat **Overige**. Er is een waarde voor het opzoekresultaat **Privé**. Als u een btw-code aan het opzoekresultaat **Privé** koppelt, wordt het transactiebedrag met de geselecteerde btw-code in geen enkel vak van de btw-aangifte weergegeven. In plaats daarvan wordt deze weergegeven in de kolom **Privé** van het rapport **Inkooptransacties**. U kunt inkopen identificeren die voor privédoeleinden worden gebruikt, door alleen een btw-code in te stellen met het veld Niet-aftrekbaar percentage ingesteld op 100 procent. Als inkopen gedeeltelijk worden gebruikt voor privédoeleinden, moet u afzonderlijke btw-codes hebben voor normaal gebruik en privégebruik.

##### <a name="credit-notes-and-negative-corrections"></a>Creditnota's en negatieve correcties

> [!IMPORTANT]
> Negatieve btw-transacties worden geclassificeerd als creditnota in het veld **Transactieclassificatie**. Voordat u toepassingsspecifieke parameters gaat instellen, moet u zorgvuldig alle typen negatieve bewerkingen in de toepassing controleren die betrekking hebben op creditnota's, negatieve correcties en annuleringen. Voordat u activiteiten boekt, moet u besluiten of u extra btw-codes moet configureren voor alle of enkele negatieve transacties of dat dezelfde btw-codes die u voor facturen gebruikt, kunnen worden gebruikt voor sommige negatieve transacties.

De volgende voorbeelden laten zien hoe verschillende instellingen invloed kunnen hebben op de resultaten van de btw-aangifte.

**Scenario 1: Een factuur en een negatieve factuur worden geboekt met dezelfde btw-code**

Een factuur heeft bijvoorbeeld een btw-basis van 1000,00 EUR en een btw-bedrag van 210,00 EUR. Een negatieve factuur heeft een btw-basis van -600,00 en een btw-bedrag van -126,00 EUR. Beide worden geboekt met de btw-code **VAT_S**.

**Case 1:** Opzoekresultaten worden als volgt ingesteld.

| Zoekresultaat                  | Label                                                                                 | Regel | Belastingcode | Transactieclassificatie |
|--------------------------------|---------------------------------------------------------------------------------------|------|----------|------------------------|
| 03_SalesStandardRate           | 03/54 Transacties waarvoor het tarief van 21% geldt                                        | 1    | VAT_S    | Sales                  |
| 49_SalesStandardRateCreditNote | 49/64 Uitgegeven creditnota's voor transacties waarvoor het tarief van 21% geldt [03] | 2    | VAT_S    | SalesCreditNote        |

In dit geval laat de btw-aangifte de volgende resultaten zien:

- **Vak 03:** 1000,00
- **Vak 54:** 210,00
- **Vak 49:** 600,00
- **Vak 64:** 126,00

**Case 2:** Opzoekresultaten worden als volgt ingesteld.

| Zoekresultaat | Label    | Regel | Belastingcode | Transactieclassificatie |
|---------------|----------|------|----------|------------------------|
| 03_SalesStandardRate  | 03/54 Transacties waarvoor het tarief van 21% geldt   | 1   | VAT_S   | Sales |
| 49_SalesStandardRateNegativeCorrection (49/62) | 49/62 Negatieve correcties voor transacties waarvoor het tarief van 21% geldt [03] | 2  | VAT_S | SalesCreditNote  |

In dit geval laat de btw-aangifte de volgende resultaten zien:

- **Vak 03:** 1000,00
- **Vak 54:** 210,00
- **Vak 49:** 600,00
- **Vak 62:** 126,00

**Case 3:** Opzoekresultaten worden als volgt ingesteld.

| Zoekresultaat        | Label                                          | Regel | Belastingcode | Transactieclassificatie |
|----------------------|------------------------------------------------|------|----------|------------------------|
| 03_SalesStandardRate | 03/54 Transacties waarvoor het tarief van 21% geldt | 1    | VAT_S    | Sales                  |
| 03_SalesStandardRate | 03/54 Transacties waarvoor het tarief van 21% geldt | 2    | VAT_S    | SalesCreditNote        |

In dit geval laat de btw-aangifte de volgende resultaten zien.

- **Vak 03:** 400,00
- **Vak 54:** 84,00

**Scenario 2: Een factuur en één negatieve factuur worden geboekt met dezelfde btw-code, maar een andere negatieve factuur wordt geboekt met een speciaal gedefinieerde btw-code.**

Een factuur heeft bijvoorbeeld een btw-basis van 1000,00 EUR en een btw-bedrag van 210,00 EUR. Negatieve factuur 1 heeft een btw-basis van -600,00 en een btw-bedrag van -126,00 EUR. Negatieve factuur 2 heeft een btw-basis van -100,00 en een btw-bedrag van -21,00 EUR.

De factuur en negatieve factuur 1 worden geboekt met de btw-code **VAT_S**, maar negatieve factuur 2 wordt geboekt met de speciaal gedefinieerde btw-code **VAT_S_CN**.

Opzoekresultaten worden als volgt ingesteld.

| Zoekresultaat  | Label | Regel | Belastingcode | Transactieclassificatie |
|----------------|-------|------|----------|------------------------|
| 03_SalesStandardRate | 03/54 Transacties waarvoor het tarief van 21% geldt   | 1  | VAT_S  | Sales  |
| 49_SalesStandardRateNegativeCorrection (49/62) | 49/62 Negatieve correcties voor transacties waarvoor het tarief van 21% geldt [03] | 2  | VAT_S | SalesCreditNote |
| 49_SalesStandardRateCreditNote | 49/64 Uitgegeven creditnota's voor transacties waarvoor het tarief van 21% geldt [03]  | 3  | VAT_S_CN | SalesCreditNote |

In dit geval laat de btw-aangifte de volgende resultaten zien:

- **Vak 03:** 1000,00
- **Vak 54:** 210,00
- **Vak 49:** 700,00 (= 600,00 + 100,00)
- **Vak 64:** 126,00
- **Vak 62:** 21,00

#### <a name="set-up-application-specific-parameters-for-advances-related-to-intra-community-acquisitions"></a>Toepassingsspecifieke parameters instellen voor voorschotten met betrekking tot intracommunautaire verwervingen

In België bevatten de rapporten **Uitgaande activiteiten** en **Binnenkomende activiteiten** een kolom waarin het bedrag aan voorschotten gerelateerd aan intracommunautaire verwervingen moet worden vermeld. U moet een afzonderlijke btw-code hebben voor dit type voorschotten.

Volg deze stappen om te definiëren welke btw-codes het bedrag aan voorschotten genereren die betrekking hebben op intracommunautaire verwervingen. Deze stappen zijn een voorzetting van de stappen in de sectie [Toepassingsspecifieke parameters instellen voor Zoekopdracht voor rapportveld](#set-up-application-specific-parameters-for-report-field-lookup).

1. Selecteer op de pagina **Toepassingsspecifieke parameters** op het sneltabblad **Zoekopdrachten** de optie **Voorschotten gerelateerd aan intracommunautaire verwervingen.**.
2. Maak op het sneltabblad **Voorwaarden** een nieuwe regel en stel de volgende velden in:

    - **Opzoekresultaat**: selecteer **Ja** als de btw-code wordt gebruikt voor voorschotten die betrekking hebben op intracommunautaire verwervingen.
    - **Btw-code**: selecteer een btw-code.

3. Maak op het sneltabblad **Voorwaarden** een nieuwe regel en stel de volgende velden in:

    - **Opzoekresultaat**: selecteer **Nee**
    - **Btw-code**: selecteer **Niet leeg** als u wilt opgeven dat alle andere btw-codes niet betrekking hebben op intracommunautaire verwervingen.

#### <a name="set-up-application-specific-parameters-for-nature"></a>Toepassingsspecifieke parameters instellen voor Aard

Het rapport **Binnenkomende activiteiten** bevat een kolom **Aard** met een omschrijving van goederen en diensten.

Volg deze stappen om te definiëren welke btw-groepen voor artikelen welke omschrijving van de aard in het rapport genereren. Deze stappen zijn een voorzetting van de stappen in de vorige sectie.

1. Selecteer op de pagina **Toepassingsspecifieke parameters** op het sneltabblad **Zoekopdrachten** de optie **Aard**.
2. Stel op het sneltabblad **Voorwaarden** de volgende velden in:

    - **Opzoekresultaat**: definieer de tekst van de aard.
    - **Belastinggroep voor artikel**: selecteer een btw-groep voor het artikel.

3. Wijzig in het veld **Status** de waarde in **Voltooid**.
4. Selecteer in het actievenster de optie **Exporteren** om de instellingen in een XML-bestand te exporteren. Sluit de pagina vervolgens.
5. Selecteer de configuratie **Btw-aangifte Excel (BE)** en selecteer vervolgens **Configuraties** \> **Toepassingsspecifieke parameters instellen**.
6. Selecteer **Importeren** en selecteer het bestand dat u eerder hebt geëxporteerd.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>De notatie voor btw-aangifte instellen voor voorbeeldbedragen in Excel

1. Zoek in het werkgebied **Functiebeheer** de functie **Indelingsrapporten voor btw-overzicht**, selecteer deze en selecteer vervolgens **Nu inschakelen**.
2. Ga naar **Grootboek \> Instellen \> Grootboekparameters**.
3. Selecteer op het tabblad **Btw** op het sneltabblad **Btw-opties** in het veld **Toewijzing indeling btw-overzicht** de ER-indeling **Btw-aangifte Excel (BE)**.

   Deze indeling wordt afgedrukt wanneer u het rapport **Btw rapporteren voor vereffeningsperiode** uitvoert. Deze wordt ook afgedrukt wanneer u **Afdrukken** selecteert op de pagina **Btw-betalingen**.

4. Selecteer op de pagina **Belastingdienst** de belastingdienst en selecteer vervolgens in het veld **Rapportindeling** de optie **Standaard**.

Als u de btw-aangifte configureert in een rechtspersoon met meerdere [btw-registraties](emea-reporting-for-multiple-vat-registrations.md), volgt u deze stappen.

1. Ga naar **Grootboek** > **Instellingen** > **Grootboekparameters**.
2. Selecteer op het tabblad **Btw-aangifte** op het sneltabblad **Elektronische aangifte voor landen/regio's** op de regel voor **BEL** de ER-indeling **Btw-aangifte Excel (BE)**.

## <a name="set-up-electronic-messages"></a>Elektronische berichten instellen

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Het gegevenspakket met voorbeeldinstellingen voor elektronische berichten downloaden en importeren

Het gegevenspakket bevat elektronische berichtinstellingen die worden gebruikt om de btw-aangifte te bekijken in Excel. U kunt deze instellingen uitbreiden of uw eigen instellingen maken. Zie [Elektronische berichten](../general-ledger/electronic-messaging.md) voor meer informatie over het werken met elektronische berichten en het maken van uw eigen instellingen.

1. Selecteer in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) in de Bibliotheek voor gedeelde activa de optie **Gegevenspakket** als activatype en download vervolgens **BE VAT declaration package**. De naam van het gedownloade bestand is **BE VAT declaration package.zip**.
2. Selecteer in Finance, in het werkgebied **Gegevensbeheer**, de optie **Importeren**.
3. Voer op het sneltabblad **Importeren** in het veld **Groepsnaam** een naam in voor de taak.
4. Selecteer op het sneltabblad **Geselecteerde entiteiten** de optie **Bestand toevoegen**.
5. Controleer in het dialoogvenster **Bestand toevoegen** of het veld **Brongegevensindeling** is ingesteld op **Pakket**, selecteer **Uploaden en toevoegen** en selecteer vervolgens het zip-bestand dat u eerder hebt gedownload.
6. Selecteer **Sluiten**.
7. Nadat de gegevensentiteiten zijn geüpload, selecteert u **Importeren** in het actievenster.
8. Ga naar **Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Elektronische berichten** en valideer de verwerking van elektronische berichten die u hebt geïmporteerd (**BE Btw-aangifte**).

### <a name="configure-electronic-messages"></a>Elektronische berichten configureren

1. Ga naar **Belasting** \> **Instellingen** \> **Elektronische berichtens** \> **Acties voor invullen van record**.
2. Selecteer de regel voor **BE Records voor btw-retouren invullen** en selecteer vervolgens **Query bewerken**.
3. Gebruik het filter om de vereffeningsperioden op te geven die u in het rapport wilt opnemen.
4. Als u btw-transacties van andere vereffeningsperioden in een andere aangifte moet rapporteren, maakt u een nieuwe actie **Records invullen** en selecteert u de juiste vereffeningsperioden.

## <a name="preview-the-vat-declaration-incoming-transactions-and-outgoing-transactions-in-excel"></a>Een voorbeeld weergeven van de btw-aangifte, inkomende transacties en uitgaande transacties in Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Een voorbeeld weergeven van de btw-aangifte in Excel vanuit de periodieke taak Btw rapporteren voor vereffeningsperiode

1. Ga naar **Belasting** \> **Periodieke taken** \> **Aangiften** \> **Btw** \> **Btw rapporteren voor vereffeningsperiode**.
2. Stel de volgende velden in.

    | Veld                     | Description                                    |
    |---------------------------|------------------------------------------------|
    | Vereffeningsperiode         | Selecteer de vereffeningsperiode.                  |
    | Begindatum                 | Selecteer de begindatum van de rapportageperiode.|

3. Selecteer **OK** en stel in het dialoogvenster **Parameters van elektronische rapportage** de volgende velden in.

    | Veld   | Description  |
    |---------|--------------|
    | 91 Depositobedrag dat in december moet worden betaald | Voer het bedrag in, indien van toepassing. |
    | Rapporten genereren  | Selecteer de rapporten die moeten worden gegenereerd:</br> - Binnenkomende activiteiten </br>- Uitgaande activiteiten</br>- Voorbeeld van btw-aangifte  |
    | Velden opnemen  | Selecteer de kolommen die zichtbaar moeten zijn in de rapporten **Binnenkomende activiteiten** en **Uitgaande activiteiten**, naast de kolommen **Datum**, **Leverancier** en **Klantnaam**: </br> -   Documentdatum</br>-   Documentnummer </br>   -   Rekening </br> -   Boekstuk </br> -   Btw-nummer|

4. Selecteer **OK** en bekijk het Excel-rapport.

### <a name="settle-and-post-sales-tax"></a>Btw vereffenen en boeken

1. Ga naar **Belasting** \> **Periodieke taken** \> **Aangiften** \> **Btw** \> **Btw vereffenen en boeken**.
2. Stel de volgende velden in.

    | Veld                     | Description                                    |
    |---------------------------|------------------------------------------------|
    | Vereffeningsperiode         | Selecteer de vereffeningsperiode.                  |
    | Begindatum                 | Selecteer de begindatum van de rapportageperiode. |

3. Selecteer **OK**.

### <a name="preview-the-vat-declaration-incoming-operations-and-outgoing-operations-in-excel-from-a-sales-tax-payment"></a>Een voorbeeld weergeven van de btw-aangifte, binnenkomende activiteiten en uitgaande activiteiten in Excel vanuit een btw-betaling

1. Ga naar **Belasting** \> **Query's en rapporten** \> **Vragen over btw** \> **Btw-betalingen** en selecteer een btw-betalingsregel.
2. Selecteer **Rapport afdrukken** en selecteer **OK**.
3. Controleer het Excel-bestand dat is gegenereerd voor de geselecteerde btw-betalingsregel.

> [!NOTE]
> Het rapport wordt alleen gegenereerd voor de geselecteerde regel van de btw-betaling. Als u bijvoorbeeld een correctieaangifte wilt genereren die alle correcties voor de periode bevat, of een vervangende aangifte met de oorspronkelijke gegevens en alle correcties, gebruikt u de periodieke taak **Btw rapporteren voor de vereffeningsperiode**.

## <a name="generate-a-vat-declaration-incoming-operations-and-outgoing-operations-from-electronic-messages"></a>Een btw-aangifte, binnenkomende activiteiten en uitgaande activiteiten genereren vanuit elektronische berichten

Wanneer u elektronische berichten gebruikt om het rapport te genereren, kunt u belastinggegevens verzamelen van meerdere rechtspersonen. Zie de sectie [Btw-aangifte uitvoeren voor meerdere rechtspersonen](#run-a-vat-declaration-for-multiple-legal-entities) verderop in dit artikel voor meer informatie.

De volgende procedure is van toepassing op het voorbeeld van de verwerking van elektronische berichten die u eerder hebt geïmporteerd uit de bibliotheek met gedeelde activa van LCS.

1. Ga naar **Belasting \> Query's en rapporten \> Elektronische berichten \> Elektronische berichten**.
2. Selecteer **BE Btw-aangifte** in het linkerdeelvenster.
3. Selecteer op het sneltabblad **Berichten** die optie **Nieuw** en selecteer vervolgens, in het dialoogvenster **Verwerking uitvoeren** de optie **OK**.
4. Selecteer de berichtregel die is gemaakt, voer een beschrijving in en geef vervolgens de begin- en einddatum voor de aangifte op.

> [!NOTE]
> Stappen 5 tot en met 7 zijn optioneel.

5. Optioneel: selecteer op het sneltabblad **Berichten** de optie **Gegevens verzamelen** en selecteer vervolgens **OK**. De btw-betalingen die eerder zijn gegenereerd, worden toegevoegd aan het bericht. Zie de sectie [Btw vereffenen en boeken](#settle-and-post-sales-tax) eerder in dit artikel voor meer informatie. Als u deze stap overslaat, kunt u nog steeds een btw-aangifte genereren via het veld **Versie btw-aangifte** in het dialoogvenster **Aangifte**.
6. Optioneel: controleer op het sneltabblad **Berichtitems** de btw-betalingen die zijn overgeboekt voor verwerking. Standaard worden alle btw-betalingen opgenomen van de geselecteerde periode die niet in een ander bericht van dezelfde verwerking zijn opgenomen.
7. Optioneel: selecteer **Oorspronkelijk document** om de btw-betalingen te controleren of selecteer **Verwijderen** om de verwerking van btw-betalingen uit te sluiten. Als u deze stap overslaat, kunt u nog steeds een btw-aangifte genereren via het veld **Versie btw-aangifte** in het dialoogvenster **Aangifte**.
8. Selecteer op het sneltabblad **Berichten** de optie **Status bijwerken**. Selecteer in het dialoogvenster **Status bijwerken** de optie **Gereed om te genereren** en selecteer vervolgens **OK**. Controleer of de berichtstatus is gewijzigd in **Gereed om te genereren**.
9. Selecteer **Rapport genereren**. Als u een voorbeeld wilt weergeven van de btw-aangiftebedragen, selecteert u in het dialoogvenster **Verwerking uitvoeren** de optie **Voorbeeldrapport** en selecteert u vervolgens **OK**.
10. Stel in het dialoogvenster **Parameters elektronische rapportage** de velden in zoals beschreven in [Een voorbeeld weergeven van de btw-aangifte in Excel vanuit de periodieke taak Btw rapporteren voor vereffeningsperiode](#preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task) eerder in dit artikel en selecteer vervolgens **OK**.
11. Selecteer de knop **Bijlagen** (paperclipsymbool) in de rechterbovenhoek van de pagina en vervolgens **Openen** om het bestand te openen. Controleer de bedragen in de Excel-documenten.
12. Selecteer **Rapport genereren**.
13. Als u een aangifte in XML-indeling wilt genereren, selecteert u in het dialoogvenster **Verwerking uitvoeren** de optie **Rapport genereren** en selecteert u vervolgens **OK**.
14. Stel de volgende velden in.

    | Veld                       | Description                  |
    |-----------------------------|------------------------------|
    | Periodiciteit aangifte          | Selecteer **Maandelijks** of **Driemaandelijks**.  |
    | 61 Meegenomen te betalen bedrag voor btw-regularisaties</br> 62 Meegenomen inhoudingsbedrag voor btw-regularisaties</br> 81 Meegenomen bedrag voor inkopen van goederen</br> 82 Meegenomen bedrag voor inkopen van diensten</br> 83 Meegenomen bedrag voor inkopen van kapitaalgoederen</br> 86 Meegenomen bedrag voor EU-inkopen van goederen</br> 87 Overige inkopen met meegenomen te betalen btw-bedrag</br> 88 Meegenomen bedrag voor EU-inkopen van diensten | In deze velden kunt u een bedrag invoeren dat wordt opgeteld bij het volgende vakbedrag. U kunt een negatief bedrag invoeren. U moet deze velden bijvoorbeeld instellen als het bedrag in een vak negatief was in de vorige periode en u 0 (nul) moet aangeven omdat negatieve bedragen niet zijn toegestaan voor het vak. U kunt het bedrag uit de vorige periode echter overdragen naar de huidige periode. |
    | 91 Depositobedrag dat in december moet worden betaald   | Voer het bedrag in, indien van toepassing.  |
    | Vervangen btw-aangifte  | Voer het nummer in van de aangifte die u vervangt, als u correcties rapporteert.   |
    | Aanvraag van teruggaaf | Selecteer **Ja** of laat de waarde ingesteld op **Nee**.    |
    | Aanvraag van betalingsformulieren | Selecteer **Ja** of laat de waarde ingesteld op **Nee**.    |
    | Geen jaaroverzichten        | Selecteer **Ja** of laat de waarde ingesteld op **Nee**.    |

15. Selecteer **OK**. 
16. Selecteer de knop **Bijlagen** (paperclipsymbool) in de rechterbovenhoek van de pagina en download het elektronische bestand dat is gegenereerd. Upload dit bestand vervolgens handmatig naar de overheidsportal.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Een btw-aangifte uitvoeren voor meerdere rechtspersonen

Als u de indelingen wilt gebruiken om de btw-aangifte voor een groep rechtspersonen te rapporteren, moet u eerst toepassingsspecifieke parameters instellen voor de ER-indelingen voor btw-codes van alle vereiste rechtspersonen.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Elektronische berichten instellen om btw-gegevens van verschillende rechtspersonen te verzamelen

Volg deze stappen om elektronische berichten in te stellen om gegevens van meerdere rechtspersonen te verzamelen.

1. Ga naar **Werkruimten \> Functiebeheer**.
2. Zoek en selecteer de functie **Query's voor meerdere bedrijven voor acties voor het invullen van records** en selecteer vervolgens **Nu inschakelen**.
3. Ga naar **Belasting \> Instellingen \> Elektronische berichten \> Acties voor invullen van record**.
4. Selecteer op de pagina **Actie voor invullen van record** de regel voor **BE Records voor btw-retouren invullen**.

   In het raster **Instelling van gegevensbronnen** is een nieuw veld **Bedrijf** beschikbaar. Voor bestaande records toont dit veld de identificatie van de huidige rechtspersoon.

5. Voeg in het raster **Instelling voor gegevensbronnen** een regel toe voor elke aanvullende rechtspersoon die in de rapportage moet worden opgenomen. Stel voor elke nieuwe regel de volgende velden in.

    | Veld                  | Description                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Name                   | Voer een waarde in om beter te begrijpen waar deze record vandaan komt. Voer bijvoorbeeld **Btw-betaling van dochtermaatschappij 1** in. |
    | Type berichtitem      | Selecteer **Btw-retour**. Dit is de enige waarde die beschikbaar is voor alle records.                                    |
    | Rekeningtype           | Selecteer **Alles**.                                                                                                               |
    | Naam van hoofdtabel      | Geef **TaxReportVoucher** op voor alle records.                                                                             |
    | Veld met documentnummer  | Geef **Voucher** op voor alle records.                                                                                      |
    | Veld met documentdatum    | Geef **TransDate** op voor alle records.                                                                                    |
    | Accountveld van document | Geef **TaxPeriod** op voor alle records.                                                                                    |
    | Bedrijf                | Selecteer de id van de rechtspersoon.                                                                                            |
    | Gebruikersquery             | Dit selectievakje wordt automatisch ingeschakeld wanneer u criteria definieert door **Query bewerken** te selecteren.                                 |

6. Selecteer voor elke nieuwe regel de optie **Query bewerken** en geef een gerelateerde vereffeningsperiode op voor de rechtspersoon die is opgegeven in het veld **Bedrijf** op de regel.

Wanneer de instelling is voltooid, verzamelt de functie **Gegevens verzamelen** op de pagina **Elektronische berichten** btw-betalingen van alle rechtspersonen die u hebt gedefinieerd.

## <a name="migrating-a-setup-of-reporting-codes-to-a-setup-of-application-specific-parameters"></a>Een configuratie van aangiftecodes migreren naar een configuratie van toepassingsspecifieke parameters

Deze sectie bevat aanbevelingen voor het migreren van uw configuratie van de INTERVAT-aangifte die is gebaseerd op het raamwerk van aangiftecodes naar de configuratie van de btw-aangifte (BE) die is gebaseerd op toepassingsspecifieke parameters in de werkruimte **Elektronische aangifte**.

> [!NOTE]
> In de volgende voorbeelden wordt dezelfde btw-code gebruikt voor verschillende typen transacties: binnenlandse verkoop, intracommunautaire verkoop, binnenlandse inkopen, intracommunautaire inkopen, intracommunautaire inkopen, enzovoort. Deze benadering is alleen ter illustratie gebruikt. Voor een eenvoudiger gebruik wanneer u uw belastingen afstemt, is het raadzaam om zo veel mogelijk btw-codes te maken, zodat elke btw-code een uniek transactietype kan identificeren. Vervolgens kunt u tijdens een belastingcontrole de bron van elke transactie op basis van de btw-code verklaren en hoeft u alleen standaardaangiftes voor btw-afstemming te gebruiken.
> 
> In de voorbeelden worden alle negatieve btw-transacties bovendien zo geconfigureerd dat ze als creditnota's worden beschouwd. Deze benadering is ook alleen ter illustratie gebruikt. Als u de juiste instellingen wilt configureren, moet u rekening houden met de informatie in de sectie [Creditnota's en negatieve correcties](#credit-notes-and-negative-corrections-1) eerder in dit artikel.

In de tabellen in deze sectie worden de volgende afkortingen gebruikt:

- **ICA**: intracommunautaire verwervingen
- **ICS**: intracommunautaire leveringen

### <a name="commercial-goods-and-services-at-a-standard-rate"></a>Commerciële goederen en diensten tegen een standaardtarief

Bijvoorbeeld voor de volgende btw-code:

| Btw-code | Percentage | Opmerking                                                                                  |
|----------------|------------|------------------------------------------------------------------------------------------|
| CommGoods      | 21         | Commerciële goederen en diensten die in België en de Europese Unie (EU) worden verhandeld |

U hebt de volgende instellingen voor aangiftecodes.

| **Transactie**       | **Belastbare verkoop** | **Te betalen btw** | **Verkoop zonder btw (ICS)** | **Belastbare inkopen** | **Te ontvangen btw** | **Inkopen zonder btw** | **Belastbare import** | **Belastbare import tegenrekenen** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|-------------|-------------------|-----------------------|--------------------------|-----------------------|--------------------------|------------------------|--------------------|---------------------------|-------------|--------------------|
| Factuur     | 03   | 54    | 46     | 81   | 59    |    &nbsp;     | 81     | 86   | 59          | 55   |
| Creditnota | 49                | 64                    | 48                       | \-81+85               | 63                       |    &nbsp;                     | \-81 +84           | \-86                      | 61          | 62                 |

In dit geval kunt u de volgende instellingen voor toepassingsspecifieke parameters hebben.

| Zoekresultaat  | Label  | Regel | Belastingcode  | Transactieclassificatie |
|----------------|--------|------|-----------|------------------------|
| 03_SalesStandardRate  | 03/54 Transacties waarvoor het tarief van 21% geldt  | 1    | CommGoods | Sales  |
| 49_SalesStandardRateCreditNote   | 49/64 Uitgegeven creditnota's voor transacties waarvoor het tarief van 21% geldt [03]  | 2    | CommGoods | SalesCreditNote  |
| 46_EUSales  | 46 Intracommunautaire leveringen vrijgesteld in België en ABC-verkoop | 3    | CommGoods | SalesExempt  |
| 48_EUSalesCreditNoteCorr  | 48 Uitgegeven creditnota's en negatieve correcties met betrekking tot vrijgestelde intracommunautaire leveringen in België en ABC-verkoop [46] | 4    | CommGoods | SalesExemptCreditNote  |
| 81_PurchasesGoods   | 81/59 Aankopen van commerciële goederen, grondstoffen en verbruiksartikelen (voor belastingbasis - rekening houdend met de ontvangen creditnota's en andere correcties) | 5 | CommGoods | Inkoop  |
| 8185_PurchasesGoodsCreditNote   | \-81 +85/63 Ontvangen creditnota's en negatieve correcties met betrekking tot de aankoop van commerciële goederen, grondstoffen en verbruiksartikelen | 6  | CommGoods | PurchaseCreditNote  |
| 8681_EUPurchasesGoodsUseTax  | 86/81 55/59 Intracommunautaire verwervingen van handelsgoederen, grondstoffen en verbruiksartikelen die zijn uitgevoerd in België en ABC-verkoop - gebruiksbelasting  | 7  | CommGoods | Gebruiksbelasting                 |
| 868184_EUPurchasesGoodsCreditNoteUseTax | \-86/81 +84/61/62 Ontvangen creditnota's en negatieve correcties met betrekking tot aankopen van commerciële goederen, grondstoffen en verbruiksartikelen - gebruiksbelasting | 8  | CommGoods | UseTaxCreditNote   |

### <a name="commercial-goods-and-services-at-a-reduced-rate"></a>Commerciële goederen en diensten tegen een gereduceerd tarief

Bijvoorbeeld voor de volgende btw-code:

| Btw-code | Percentage | Opmerking                                                                                               |
|----------------|------------|-------------------------------------------------------------------------------------------------------|
| RedComGood     | 6          | Artikelen/goederen (maar geen diensten) die een gereduceerd btw-tarief hebben en worden verhandeld in België en de EU |

U hebt de volgende instellingen voor aangiftecodes.

| **Transactie**   | **Belastbare verkoop** | **Te betalen btw** | **Verkoop zonder btw (ICS)** | **Belastbare inkopen** | **Te ontvangen btw** | **Inkopen zonder btw** | **Belastbare import** | **Belastbare import tegenrekenen** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|-------------|-------------------|-----------------------|--------------------------|-----------------------|--------------------------|------------------------|--------------------|---------------------------|-------------|--------------------|
| Factuur     | 01                | 54                    | 46                       | 81                    | 59                       |     &nbsp;                    | 81                 | 86                        | 59          | 55                 |
| Creditnota | 49                | 64                    | 48                       | \-81 +85              | 63                       |      &nbsp;                   | \-81 +84           | \-86                      | 61          | 62                 |

In dit geval kunt u de volgende instellingen voor toepassingsspecifieke parameters hebben.

| Zoekresultaat  | Label  | Regel | Belastingcode  | Transactieclassificatie |
|----------------|--------|------|------------|------------------------|
| 01_SalesLowerReducedRate  | 01/54 Transacties waarvoor het tarief van 6% geldt  | 1  | RedComGood | Sales   |
| 49_SalesLowerReducedRateCreditNote  | 49/64 Uitgegeven creditnota's voor transacties waarvoor het tarief van 6% geldt [01]  | 2  | RedComGood | SalesCreditNote   |
| 46_EUSales  | 46 Intracommunautaire leveringen vrijgesteld in België en ABC-verkoop | 3    | RedComGood | SalesExempt  |
| 48_EUSalesCreditNoteCorr  | 48 Uitgegeven creditnota's en negatieve correcties met betrekking tot vrijgestelde intracommunautaire leveringen in België en ABC-verkoop [46] | 4  | RedComGood | SalesExemptCreditNote  |
| 81_PurchasesGoods  | 81/59 Aankopen van commerciële goederen, grondstoffen en verbruiksartikelen (voor belastingbasis - rekening houdend met de ontvangen creditnota's en andere correcties) | 5   | RedComGood | Inkoop    |
| 8185_PurchasesGoodsCreditNote  | \-81 +85/63 Ontvangen creditnota's en negatieve correcties met betrekking tot de aankoop van commerciële goederen, grondstoffen en verbruiksartikelen  | 6   | RedComGood | PurchaseCreditNote  |
| 8681_EUPurchasesGoodsUseTax  | 86/81 55/59 Intracommunautaire verwervingen van handelsgoederen, grondstoffen en verbruiksartikelen die zijn uitgevoerd in België en ABC-verkoop - gebruiksbelasting  | 7  | RedComGood | Gebruiksbelasting                 |
| 868184_EUPurchasesGoodsCreditNoteUseTax | \-86/81 +84/61/62 Ontvangen creditnota's en negatieve correcties met betrekking tot aankopen van commerciële goederen, grondstoffen en verbruiksartikelen - gebruiksbelasting      | 8    | RedComGood | UseTaxCreditNote  |

### <a name="commercial-goods-for-trade-outside-the-eu"></a>Commerciële goederen voor handel buiten de EU

Bijvoorbeeld voor de volgende btw-code:

| Btw-code | Percentage | Opmerking                                                                |
|----------------|------------|------------------------------------------------------------------------|
| ComGood-3      | 21         | Commerciële goederen die worden geïmporteerd uit of geëxporteerd naar derde landen |

U hebt de volgende instellingen voor aangiftecodes.

|  **Transactie**  | **Belastbare verkoop** | **Te betalen btw**                        | **Verkoop zonder btw (ICS)**       | **Belastbare inkopen** | **Te ontvangen btw** | **Inkopen zonder btw** | **Belastbare import** | **Belastbare import tegenrekenen** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|-------------|-------------------|----------------------------------------------|--------------------------------|-----------------------|--------------------------|------------------------|--------------------|---------------------------|-------------|--------------------|
| Factuur     |     &nbsp;               |             &nbsp;                                  | 47                             | 81                    | 59                       | 81                     | 81                 | 87                        | 59          | 57                 |
| Creditnota |       &nbsp;             |      &nbsp;                                         | 49                             | \-81 +85              | 63                       | \-81 +85               | \-81 +85           | \-87                      | 61          | 62                 |

In dit geval kunt u de volgende instellingen voor toepassingsspecifieke parameters hebben.

| Zoekresultaat  | Label | Regel | Belastingcode  | Transactieclassificatie   |
|----------------|-------|------|-----------|--------------------------|
| 47_OtherExemptSales   | 47 Overige vrijgestelde transacties en andere transacties die in het buitenland zijn uitgevoerd | 1   | ComGood-3 | SalesExempt   |
| 49_ExemptSalesSpecialSchemeCreditNoteCorr  | 49 Uitgegeven creditnota's en negatieve correcties met betrekking tot transacties waarvoor speciale regelingen gelden [00]  | 2  | ComGood-3 | SalesExemptCreditNote  |
| 81_PurchasesGoods  | 81/59 Aankopen van commerciële goederen, grondstoffen en verbruiksartikelen (voor belastingbasis - rekening houdend met de ontvangen creditnota's en andere correcties)  | 3    | ComGood-3 | Inkoop  |
| 8185_PurchasesGoodsCreditNote  | \-81 +85/63 Ontvangen creditnota's en negatieve correcties met betrekking tot de aankoop van commerciële goederen, grondstoffen en verbruiksartikelen   | 4  | ComGood-3 | PurchaseCreditNote  |
| 81_PurchasesGoods  | 81/59 Aankopen van commerciële goederen, grondstoffen en verbruiksartikelen (voor belastingbasis - rekening houdend met de ontvangen creditnota's en andere correcties)  | 5    | ComGood-3 | PurchaseExempt  |
| 8185_PurchasesGoodsCreditNote  | \-81 +85/63 Ontvangen creditnota's en negatieve correcties met betrekking tot de aankoop van commerciële goederen, grondstoffen en verbruiksartikelen | 6  | ComGood-3 | PurchaseExemptCreditNote |
| 8781_OtherPurchasesImportsDeferredTaxGoodsUseTax | 87/81 57/59 Overige aankopen van commerciële goederen, grondstoffen en verbruiksartikelen waarvoor btw verschuldigd is door de declarant (import met uitgestelde belastinginning) - gebruiksbelasting  | 7    | ComGood-3 | Gebruiksbelasting   |
| 878185_OtherPurchasesImportsDeferredTaxGoodsCNUseTax | \-87/81 +85/61/62 Ontvangen creditnota's en negatieve correcties met betrekking tot andere aankopen van commerciële goederen, grondstoffen en verbruiksartikelen waarvoor de declarant btw verschuldigd is (import met uitgestelde belastinginning) - gebruiksbelasting | 8  | ComGood-3 | UseTaxCreditNote    |

### <a name="services-at-a-standard-rate-and-goods-purchased-for-internal-use"></a>Diensten tegen een standaardtarief en goederen die voor intern gebruik zijn ingekocht

Bijvoorbeeld voor de volgende btw-code:

| Btw-code | Percentage | Opmerking                                                                                        |
|----------------|------------|------------------------------------------------------------------------------------------------|
| Service21      | 21         | Diensten en intern gebruikte goederen die in België, de EU en derde landen worden verhandeld |

U hebt de volgende instellingen voor aangiftecodes.

| **Transactie**   | **Belastbare verkoop**       | **Te betalen btw**       | **Verkoop zonder btw (ICS)**                                                           | **Belastbare inkopen** | **Te ontvangen btw** | **Inkopen zonder btw** | **Belastbare import** | **Belastbare import tegenrekenen** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|-------------|-------------------------|-----------------------------|------------------------------------------------------------------------------------|-----------------------|--------------------------|------------------------|--------------------|---------------------------|-------------|--------------------|
| Factuur     | 03                      | 54                          | 47                                                                                 | 82                    | 59                       | 82                     | 82                 |    &nbsp;                        |    &nbsp;          |     &nbsp;                |
| Creditnota | 49                      | 64                          | 49                                                                                 | \-82 +85              | 63                       | \-82 +85               | \-82 +85           |      &nbsp;                      |     &nbsp;         |    &nbsp;                 |

In dit geval kunt u de volgende instellingen voor toepassingsspecifieke parameters hebben.

| Zoekresultaat    | Label     | Regel | Belastingcode  | Transactieclassificatie   |
|------------------|-----------|------|-----------|--------------------------|
| 03_SalesStandardRate   | 03/54 Transacties waarvoor het tarief van 21% geldt  | 1  | Service21 | Sales  |
| 49_SalesStandardRateCreditNote  | 49/64 Uitgegeven creditnota's voor transacties waarvoor het tarief van 21% geldt [03]  | 2 | Service21 | SalesCreditNote  |
| 47_OtherExemptSales | 47 Overige vrijgestelde transacties en andere transacties die in het buitenland zijn uitgevoerd  | 3  | Service21 | SalesExempt  |
| 49_ExemptSalesSpecialSchemeCreditNoteCorr | 49 Uitgegeven creditnota's en negatieve correcties met betrekking tot transacties waarvoor speciale regelingen gelden [00]  | 4  | Service21 | SalesExemptCreditNote  |
| 82_PurchasesServicesMisc  | 82/59 Aankopen van diensten en diverse goederen (voor belastingbasis - rekening houdend met de ontvangen creditnota's en andere correcties) | 5   | Service21 | Inkoop  |
| 8285_PurchasesServicesMiscCreditNote  | \-82 +85/63 Ontvangen creditnota's en negatieve correcties met betrekking tot de aankoop van diensten en diverse goederen | 6  | Service21 | PurchaseCreditNote  |
| 82_PurchasesServicesMisc  | 82/59 Aankopen van diensten en diverse goederen (voor belastingbasis - rekening houdend met de ontvangen creditnota's en andere correcties) | 7  | Service21 | PurchaseExempt  |
| 8285_PurchasesServicesMiscCreditNote   | \-82 +85/63 Ontvangen creditnota's en negatieve correcties met betrekking tot de aankoop van diensten en diverse goederen | 8    | Service21 | PurchaseExemptCreditNote |

> [!NOTE]
> In dit voorbeeld moet u de inkoop voor gebruiksbelasting niet boeken en **Gebruiksbelasting** niet instellen in de toepassingsspecifieke parameters. Gebruik de transactie **belastbare inkopen** of **inkopen zonder btw** voor de aankoop van diensten van buiten België.

### <a name="capital-goods"></a>Kapitaalgoederen

Bijvoorbeeld voor de volgende btw-code:

| Belastingcode  | Percentage | Opmerking                                                 |
|-----------|------------|---------------------------------------------------------|
| Capital21 | 21         | Kapitaalitems die in België en de EU worden verhandeld |

U hebt de volgende instellingen voor aangiftecodes.

| **Transactie**            | **Belastbare verkoop** | **Te betalen btw**       | **Verkoop zonder btw (ICS)**             | **Belastbare inkopen** | **Te ontvangen btw** | **Inkopen zonder btw** | **Belastbare import** | **Belastbare import tegenrekenen** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|-------------|-------------------|-----------------------------|--------------------------------------|-----------------------|--------------------------|------------------------|--------------------|---------------------------|-------------|--------------------|
| Factuur     | 03                | 54                          | 46                                   | 83                    | 59                |     &nbsp;   | 83                 | 86                        | 59          | 55                 |
| Creditnota | 49                | 64                          | 48                                   | \-83 +85              | 63      |        &nbsp;            | \-83 +84           | \-86                      | 61          | 62                 |

In dit geval kunt u de volgende instellingen voor toepassingsspecifieke parameters hebben.

| Zoekresultaat  | Label  | Regel | Belastingcode  | Transactieclassificatie |
|----------------|--------|------|-----------|------------------------|
| 03_SalesStandardRate   | 03/54 Transacties waarvoor het tarief van 21% geldt  | 1    | Capital21 | Sales  |
| 49_SalesStandardRateCreditNote | 49/64 Uitgegeven creditnota's voor transacties waarvoor het tarief van 21% geldt [03] | 2    | Capital21 | SalesCreditNote   |
| 46_EUSales | 46 Intracommunautaire leveringen vrijgesteld in België en ABC-verkoop  | 3    | Capital21 | SalesExempt  |
| 48_EUSalesCreditNoteCorr  | 48 Uitgegeven creditnota's en negatieve correcties met betrekking tot vrijgestelde intracommunautaire leveringen in België en ABC-verkoop [46] | 4    | Capital21 | SalesExemptCreditNote  |
| 83_PurchasesCapitalGoods  | 83/59 Aankopen van kapitaalgoederen (voor belastingbasis - rekening houdend met de ontvangen creditnota's en andere correcties) | 5  | Capital21 | Inkoop  |
| 8385_PurchasesCapitalGoodsCreditNote| \-83 +85/63 Ontvangen creditnota's en negatieve correcties  | 6    | Capital21 | PurchaseCreditNote   |
| 8683_EUPurchasesCapitalGoodsUseTax   | 86/83 55/59 Intracommunautaire verwervingen van kapitaalgoederen die zijn uitgevoerd in België en ABC-verkoop - gebruiksbelasting  | 7  | Capital21 | Gebruiksbelasting   |
| 868384_EUPurchasesCapitalGoodsCreditNoteUseTax | \-86/83 +84/61/62 Ontvangen creditnota's en negatieve correcties met betrekking tot aankopen van kapitaalgoederen - gebruiksbelasting  | 8  | Capital21 | UseTaxCreditNote  |

### <a name="special-services"></a>Speciale diensten

Bijvoorbeeld voor de volgende btw-code:

| Btw-code | Percentage | Opmerking                                                         |
|----------------|------------|-----------------------------------------------------------------|
| SpecServ       | 0          | Speciale diensten, waarbij de btw wordt betaald door de ontvanger |

U hebt de volgende instellingen voor aangiftecodes.

| **Transactie**   | **Belastbare verkoop** | **Te betalen btw** | **Verkoop zonder btw (ICS)** | **Belastbare inkopen** | **Te ontvangen btw** | **Inkopen zonder btw** | **Belastbare import** | **Belastbare import tegenrekenen** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|-------------|-------------------|-----------------------|--------------------------|-----------------------|--------------------------|------------------------|--------------------|---------------------------|-------------|--------------------|
| Factuur     |     &nbsp;               |       &nbsp;                 | 45         |   &nbsp;     |     &nbsp;        |      &nbsp;     | 82                 | 87                        |   &nbsp;  |     &nbsp;    |
| Creditnota |    &nbsp;       |    &nbsp;      | 49           |      &nbsp;     |      &nbsp;    |      &nbsp;       | \-82 +85           | \-87             |   &nbsp;    |    &nbsp;     |

In dit geval kunt u de volgende instellingen voor toepassingsspecifieke parameters hebben.

| Zoekresultaat   | Label   | Regel | Belastingcode  | Transactieclassificatie |
|-----------------|---------|------|-----------|------------------------|
| 46_EUSales   | 46 Intracommunautaire leveringen vrijgesteld in België en ABC-verkoop  | 3    | Capital21 | SalesExempt    |
| 48_EUSalesCreditNoteCorr  | 48 Uitgegeven creditnota's en negatieve correcties met betrekking tot vrijgestelde intracommunautaire leveringen in België en ABC-verkoop [46]  | 4    | Capital21 | SalesExemptCreditNote  |
| 8782_OtherPurchasesDomesticReverseChargeMiscUseTax     | 87/82 56/59 Overige aankopen van diverse goederen waarvoor btw verschuldigd is door de declarant (binnenlandse omgekeerde toeslag) - gebruiksbelasting    | 7    | Capital21 | Gebruiksbelasting  |
| 878285_OtherPurchasesDomesticReverseChargeMiscCNUseTax | \-87/82 +85/61/62 Ontvangen creditnota's en negatieve correcties met betrekking tot andere aankopen van diverse goederen waarvoor de declarant btw verschuldigd is (binnenlandse omgekeerde toeslag) - gebruiksbelasting | 8    | Capital21 | UseTaxCreditNote  |


## <a name="examples-of-posting-and-reporting"></a>Voorbeelden van boeken en aangeven

De voorbeelden in deze sectie zijn bedoeld voor het configureren van toepassingsspecifieke parameters voor de sectie [Commerciële goederen en diensten tegen een standaardtarief](#commercial-goods-and-services-at-a-standard-rate) eerder in dit artikel.

### <a name="example-1-sale-in-belgium"></a>Voorbeeld 1: Verkoop in België

Dit voorbeeld toont een verkoop in België, waar het nettobedrag van de factuur 1000 EUR plus 21 procent btw is.

**Boeking**

| Rekening            | Debet    | Credit   |
|--------------------|----------|----------|
| Klant           | 1,210.00 |  &nbsp;         |
| Verkoop               |    &nbsp;       | 1,000.00 |
| Uitgaande btw |   &nbsp;        | 210.00   |

**Rapportage**

| Veld in btw-aangifte | Bedrag   |
|---------------------------|----------|
| Veld 03                  | 1,000.00 |
| Veld 54                  | 210.00   |

### <a name="example-2-credit-note-for-a-sale-in-belgium"></a>Voorbeeld 2: Creditnota voor een verkoop in België

Dit voorbeeld toont een creditnota voor een verkoop in België, waarbij het nettobedrag van de creditnota 1000 EUR plus 21 procent btw is.

**Boeking**

| Rekening            | Debet    | Credit   |
|--------------------|----------|----------|
| Klant           |   &nbsp;        | 1,210.00 |
| Verkoop               | 1,000.00 |   &nbsp;        |
| Uitgaande btw | 210.00   |    &nbsp;       |

**Rapportage**

| Veld in btw-aangifte | Bedrag   |
|---------------------------|----------|
| Veld 49                  | 1,000.00 |
| Veld 64                  | 210.00   |

### <a name="example-3-purchase-in-belgium"></a>Voorbeeld 3: Inkoop in België

Dit voorbeeld toont een inkoop in België, waar het nettobedrag van de factuur 1000 EUR plus 21 procent btw is.

**Boeking**

| Rekening            | Debet    | Credit   |
|--------------------|----------|----------|
| Leverancier             |  &nbsp;         | 1,210.00 |
| Kosten               | 1,000.00 |  &nbsp;         |
| Binnenkomende btw | 210.00   |    &nbsp;       |

**Rapportage**

| Veld in btw-aangifte | Bedrag   |
|---------------------------|----------|
| Veld 81                  | 1,000.00 |
| Veld 59                  | 210.00   |

### <a name="example-4-credit-note-for-a-purchase-in-belgium"></a>Voorbeeld 4: Creditnota voor een inkoop in België

Dit voorbeeld toont een creditnota voor een inkoop in België, waarbij het nettobedrag van de creditnota 1000 EUR plus 21 procent btw is.

**Boeking**

| Rekening            | Debet    | Credit   |
|--------------------|----------|----------|
| Leverancier             | 1,210.00 |  &nbsp;         |
| Kosten               |  &nbsp;         | 1,000.00 |
| Binnenkomende btw |   &nbsp;        | 210.00   |

**Rapportage**

| Veld in btw-aangifte | Bedrag     |
|---------------------------|------------|
| Veld 81                  | \-1,000.00 |
| Veld 85                  | 1,000.00   |
| Veld 63                  | 210.00     |

### <a name="example-5-intra-community-acquisition"></a>Voorbeeld 5: Intracommunautaire verwerving

Dit voorbeeld toont een intracommunautaire verwerving (een verwerving van een leverancier in de EU, maar buiten België), waarbij het nettobedrag van de factuur 1000 EUR is. De Belgische btw van 21 procent moet zelf worden verantwoord.

**Boeking**

| Rekening                                  | Debet    | Credit   |
|------------------------------------------|----------|----------|
| Leverancier                                   |   &nbsp;        | 1,000.00 |
| Kosten                                     | 1,000.00 |   &nbsp;        |
| Btw voor import (zelf verantwoord)        | 210.00   |   &nbsp;        |
| Tegenrekening van btw voor import (zelf verantwoord) |  &nbsp;         | 210.00   |

**Rapportage**

| Veld in btw-aangifte | Bedrag   |
|---------------------------|----------|
| Veld 81                  | 1,000.00 |
| Veld 86                  | 1,000.00 |
| Veld 59                  | 210.00   |
| Veld 55                  | 210.00   |

### <a name="example-6-credit-note-for-an-intra-community-acquisition"></a>Voorbeeld 6: Creditnota voor een intracommunautaire verwerving

Dit voorbeeld toont een creditnota voor een intracommunautaire verwerving (een verwerving van een leverancier in de EU, maar buiten België), waarbij het nettobedrag van de creditnota 1000 EUR is. De Belgische btw van 21 procent moet zelf worden verantwoord.

**Boeking**

| Rekening                                   | Debet    | Credit   |
|-------------------------------------------|----------|----------|
| Leverancier                                    | 1,000.00 | &nbsp;          |
| Kosten                                      | &nbsp;          | 1,000.00 |
| Btw voor import (zelf verantwoord)         |   &nbsp;        | 210.00   |
| Compensatie van btw voor import (zelf verantwoord) | 210.00   |     &nbsp;      |

**Rapportage**

| Veld in btw-aangifte | Bedrag     |
|---------------------------|------------|
| Veld 81                  | \-1,000.00 |
| Veld 86                  | \-1,000.00 |
| Veld 84                  | 1,000.00   |
| Veld 61                  | 210.00     |
| Veld 62                  | 210.00     |

### <a name="example-7-intra-community-supply"></a>Voorbeeld 7: Intracommunautaire levering

Dit voorbeeld toont een intracommunautaire levering (levering aan een klant in een ander EU-land met een btw-registratienummer in die lidstaat), waarbij het nettobedrag van de factuur 1000 EUR is en belastingvrij is.

**Boeking**

| Rekening  | Debet    | Credit   |
|----------|----------|----------|
| Klant | 1,000.00 | &nbsp;          |
| Verkoop     |   &nbsp;        | 1,000.00 |

**Rapportage**

| Veld in btw-aangifte | Bedrag   |
|---------------------------|----------|
| Veld 46                  | 1,000.00 |

### <a name="example-8-credit-note-for-intra-community-supply"></a>Voorbeeld 8: Creditnota voor intracommunautaire levering

Dit voorbeeld toont een creditnota voor een intracommunautaire levering (levering aan een klant in een ander EU-land met een btw-registratienummer in die lidstaat), waarbij het nettobedrag van de creditnota 1000 EUR is en belastingvrij is.

**Rapportage**

| Veld in btw-aangifte | Bedrag   |
|---------------------------|----------|
| Veld 48                  | 1,000.00 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
