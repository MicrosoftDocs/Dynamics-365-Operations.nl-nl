---
title: Verwijderde of afgeschafte functies in Dynamics 365 Finance
description: In dit artikel worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.
author: kfend
ms.date: 10/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 516b2b6091fa620b21eebba25f56ff55aa282ffc
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643789"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Verwijderde of afgeschafte functies in Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

In dit artikel worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

> [!NOTE]
> Gedetailleerde informatie over objecten in apps voor financiën en bedrijfsactiviteiten is te vinden in de [Rapporten met technische naslaginformatie](/dynamics/s-e/global/axtechrefrep_61). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van apps voor financiën en bedrijfsactiviteiten.

## <a name="features-removed-or-deprecated-in-the-finance-10031-release"></a>Verwijderde of verouderde functies in versie 10.0.31 van Finance

### <a name="edifact-paymul-at-configuration-under-payment-model"></a>EDIFACT PAYMUL (AT)-configuratie onder Betalingsmodel

| &nbsp;  | &nbsp;  |
|---|---|
| **Reden voor afschaffing/verwijdering** | Vervangen door een nieuwe indeling die is gebaseerd op ISO 20022 pain.001.001.09. | 
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: banken in Oostenrijk zullen EDICFACT-PAYMUL voor grensoverschrijdende betalingen tegen november 2022 hebben afgeschreven en deze hebben vervangen door XML-versie pain.001.001.09N. Er is een nieuwe configuratie toegevoegd onder de Algemene configuratieopslagplaats die gebruikers in staat stelt om de aanvraag voor grensoverschrijdende betaling te voltooien. |

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Verwijderde of verouderde functies in versie 10.0.30 van Finance

### <a name="revenue-recognition"></a>Opbrengsttoerekening

[Opbrengsttoerekening](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Reden voor afschaffing/verwijdering** |Vervangen door verbeterde functionaliteit, [facturering van abonnementen](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden** | Toepassing |
| **Implementatieoptie** | Alle |
| **Status** | Afgeschaft: na april 2023 wordt de functie voor opbrengstherkenning in Dynamics 365 Finance niet meer ondersteund voor het oplossen van fouten. Klanten zal worden gevraagd de verbeterde functionaliteit [Facturering van abonnementen](../../finance/accounts-receivable/subscription-billing-summary.md) te gebruiken. In oktober 2023 is de functie voor opbrengstherkenning niet langer beschikbaar. Klanten zal worden gevraagd over te stappen naar de verbeterde functionaliteit Facturering van abonnementen. Voor de functie voor bundelen als onderdeel van opbrengsttoerekening is er op dit moment geen vervangende functionaliteit gepland.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Verwijderde of verouderde functies in versie 10.0.29 van Finance

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Voorraadtransferorders met belasting op de transferprijs

[Voorraadtransferorders met belasting op de transferprijs](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Reden voor afschaffing/verwijdering** | Vervangen door verbeterde functionaliteit [voorraadtransferorders voor India](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden** | Toepassing |
| **Implementatieoptie** | Alle |
| **Status** | Afgeschaft: na april 2023 wordt de functionaliteit **voorraadtransferorders met belasting op de transferprijs** niet langer ondersteund met correcties voor fouten en beveiligingsfixes. Klanten zal worden gevraagd de verbeterde functionaliteit [Voorraadtransferorders voor India](../../finance/localizations/apac-ind-stock-transfer.md) te gebruiken. Na oktober 2023 is de functionaliteit **voorraadtransferorders met belasting op de transferprijs** niet langer beschikbaar en wordt klanten gevraagd de verbeterde functionaliteit te gebruiken. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Bankafschrift importeren en exporteren van positief salarisbestand

| &nbsp;  | &nbsp;  |
|---|---|
| **Reden voor afschaffing/verwijdering** |Vervangen door verbeterde functionaliteit, bankafschriften importeren en positieve salarisbestanden exporteren.| 
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: de XSLT-functionaliteit voor het importeren en exporteren van bestanden wordt niet langer ondersteund met bugfixes en beveiligingsfixes. Klanten wordt gevraagd de verbeterde functionaliteit te gebruiken: [Positieve betalingsbestanden instellen met behulp van Elektronische rapportage](../../finance/accounts-payable/set-up-positive-pay-er.md) en [Importeren van geavanceerde bankafstemming instellen via Elektronische rapportage](../../finance/accounts-payable/import-bai2-er.md). Na september 2022 is de XSLT-functionaliteit niet meer beschikbaar en krijgen klanten de vraag of ze naar de verbeterde functionaliteit willen overstappen.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Verwijderde of verouderde functies in versie 10.0.26 van Finance

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Btw-rapport voor Finland (ontwerp op basis van aangiftecodes)

[Btw-rapport voor Finland](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een nieuw ontwerp voor btw-aangifte [Btw-aangifte voor Finland](../localizations/emea-fin-vat-declaration.md). |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 maart 2023 willen we geen ondersteuning meer bieden voor het btw-rapport voor Finland (Finse rapportindeling). In plaats daarvan worden onder het model **Belastingaangifte** de nieuwe ER-indelingen **TXT voor btw-aangifte (FI)** en **Btw-aangifte Excel (FI)** beschikbaar gesteld. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Verwijderde of verouderde functies in versie 10.0.24 van Finance

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Btw-rapport voor Zweden (ontwerp op basis van aangiftecodes)

[Btw-rapport voor Zweden](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een nieuw ontwerp voor btw-aangifte [Btw-aangifte voor Zweden](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 december 2022 willen we geen ondersteuning meer bieden voor het btw-rapport voor Zweden (Zweedse rapportindeling). In plaats daarvan worden onder het model **Belastingaangifte** de nieuwe ER-indelingen **XML voor btw-aangifte (SE**) en **Btw-aangifte Excel (SE)** beschikbaar gesteld. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Btw-overzicht voor Oostenrijk (ontwerp op basis van aangiftecodes)

[Details btw-overzicht voor Oostenrijk](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een nieuw ontwerp voor btw-aangifte [Btw-aangifte voor Oostenrijk](../localizations/emea-aut-vat-declaration-austria.md) |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 december 2022 willen we geen ondersteuning meer bieden voor de ER-indeling **Btw-aangifte (AT)** onder **Btw-aangiftemodel**. In plaats daarvan worden onder het model **Belastingaangifte** de nieuwe indelingen **XML voor btw-aangifte (AT)** en **Btw-aangifte Excel (AT)** beschikbaar gesteld. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ELSTER-aangifte voor Duitsland (ontwerp op basis van aangiftecodes)

[Btw-overzicht](../localizations/emea-de-vat-declaration.md)</br>
[Elektronische belastingaangifte voor Duitsland instellen](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[Elektronische transmissie van btw-aangifte (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een nieuw ontwerp voor btw-aangifte [Btw-aangifte voor Duitsland](../localizations/emea-deu-vat-declaration-germany.md) |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 december 2022 willen we geen ondersteuning meer bieden voor de ER-indelingen **Elster (DE)** en **Elster-model**. In plaats daarvan worden onder het model **Belastingaangifte** de nieuwe indelingen **XML voor btw-aangifte (DE)** en **Btw-aangifte Excel (DE)** beschikbaar gesteld. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>OB-aangifte voor Nederland (ontwerp op basis van aangiftecodes)

[OB-aangifte](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een nieuw ontwerp voor btw-aangifte [Btw-aangifte voor Nederland](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 december 2022 willen we geen ondersteuning meer bieden voor de ER-indelingen **OB-aangifte (NL)** en **OB-aangiftemodel**. In plaats daarvan worden onder het model **Belastingaangifte** de nieuwe indelingen **XML voor btw-aangifte (NL)** en **Btw-aangifte Excel (NL)** beschikbaar gesteld. |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Verwijderde of verouderde functies in versie 10.0.20 van Finance

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>Configuratie van de HU-indeling ('RTIR Query Invoice Data Request') voor elektronische rapportage (ER)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Uitgesloten van verwerking van elektronische berichten bij samenwerking met Hongaars online factureringssysteem |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Sollicitatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: Uiterlijk op 15 april 2022 zal de indelingsconfiguratie "RTIR Query Invoice Data Request (HU)" niet langer worden ondersteund. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>'Frans FEC-auditbestand' met indeling voor elektronische rapportage (ER) voor Frankrijk onder 'uitvoer van Duits auditfile'-indeling

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door nieuwe 'Frans FEC-auditbestand (FR)'-indeling |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Sollicitatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: per 1 mei 2022 zijn we van plan om niet langer het 'Frans FEC-auditbestand' met indeling voor elektronische rapportage (ER) voor Frankrijk onder 'uitvoer van Duits auditfile'-indeling te ondersteunen. In plaats daarvan wordt de nieuwe 'Frans FEC-auditbestand (FR)'-indeling geïntroduceerd onder het 'Gegevensexportmodel'. |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Verwijderde of verouderde functies in versie 10.0.17 van Finance

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-opslagplaats als een opslagoptie voor configuraties voor elektronische rapportage

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door de nieuwe algemene opslagplaats voor Regulatory Configuration Service (RCS) |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Dynamics 365 Finance-, Supply Chain Management- en Project Operations-producten|
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: tegen 1 april 2022 willen we opslagplaats voor Microsoft Dynamics Lifecycle Services (LCS) niet langer ondersteunen als opslagoptie voor ER-configuraties (Elektronische rapportage). Nieuwe Microsoft ER-configuraties worden gepubliceerd om exclusief te downloaden uit de algemene opslagplaats. De algemene opslagplaats kan worden gebruikt vanuit de Dynamics 365-producten en RCS. Zie [ER-configuraties importeren vanuit RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) en [Afschaffing Regulatory Configuration Service - Lifecycle Services Storage](../localizations/rcs-lcs-repo-dep-faq.md) voor meer informatie. |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Verwijderde of verouderde functies in versie 10.0.16 van Finance

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Indelingen Btw-aangifte (CZ) en Export van controleoverzicht (CZ) voor elektronische aangifte voor Tsjechië

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door nieuwe indelingen |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Sollicitatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: tegen 22 januari 2022 zetten we de ondersteuning voor de indelingen Btw-aangifte (CZ) en Export van controleoverzicht (CZ) voor elektronische aangifte stop. In plaats daarvan worden onder het model Belastingaangifte een nieuwe XML voor btw-aangifte (CZ), een nieuw Excel-bestand voor btw-aangifte (CZ) en een nieuwe XML voor het btw-controleoverzicht beschikbaar gesteld. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Exportindeling voor grootboektransacties (BE)" elektronische rapporteringsindeling en het bijbehorende model "Exporteren van grootboektransacties (BE)" voor België

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen met nieuwe ER-indeling onder het model "Standaard auditfile (SAF-T)".  |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Sollicitatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: op 1 december 2021, zullen we de electronische rapportageindeling 'Exportindeling voor grootboektransacties (BE)' en het bijbehorende model 'Exporteren van grootboektransacties (BE)' niet meer ondersteunen. In plaats daarvan introduceren we een nieuwe indeling 'Grootboekgegevens exporteren (BE)' met 'Modeltoewijzing van grootboekgegevens' in plaats van het model 'Standaard auditfile (SAF-T)'. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>Het rapport 'VAT 100' voor het Verenigd Koninkrijk in SSRS-indeling

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door nieuwe ER-indeling - 'VAT-aangifte Excel (VK)'-indeling onder 'Belastingaangiftemodel'.  |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Sollicitatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: op 1 december 2021, wordt het rapport 'VAT 100' in SSRS-indeling niet meer ondersteund. Een nieuwe indeling 'VAT-aangifte Excel (VK)' onder het 'Belastingaangiftemodel' is ingevoerd in de [MTD VAT-functie](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Verwijderde of verouderde functies in versie 10.0.15 van Finance

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-ondersteuning voor Dynamics 365 is afgeschaft

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met ingang van december 2020 wordt Microsoft Internet Explorer 11-ondersteuning voor alle Dynamics 365-producten afgeschaft en wordt Internet Explorer 11 na augustus 2021 niet meer ondersteund.<br><br>Dit heeft invloed op klanten die Dynamics 365-producten gebruiken die zijn ontworpen om via een Internet Explorer 11-interface te worden gebruikt. Na augustus 2021 wordt Internet Explorer 11 niet ondersteund voor dergelijke Dynamics 365-producten. |
| **Vervangen door een andere functie?**   | Wij raden klanten aan om overstappen op Microsoft Edge.|
| **Betrokken productgebieden**         | Alle Dynamics 365-producten |
| **Implementatieoptie**              | Alles|
| **Status**                         | Afgeschaft. Internet Explorer 11 wordt na augustus 2021 niet ondersteund.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Verwijderde of verouderde functies in versie 10.0.12 van Finance

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Niet afgeschaft: Poolse SSRS-rapporten: Btw-register voor verkoop, btw-register voor inkoop, btw-register EU-overzicht – functieverwijzing PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Niet wettelijk vereist.  |
| **Vervangen door een andere functie?**   | Ja (Excel-indeling voor standaardauditbestand met btw-aangifte - JPK_VDEK) |
| **Betrokken productgebieden**         | Sollicitatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Niet afgeschaft: Vanaf 27 april 2021 zijn wij van plan om de SSRS-rapporten te blijven ondersteunen: **Btw-register voor verkoop, btw-register voor inkoop, btw-register EU-overzicht – functieverwijzing PL-00014**. Er wordt tevens een voorbeeld van een Excel-indeling geïntroduceerd voor het standaardauditbestand met btw-aangifte (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Verwijderde of verouderde functies in versie 10.0.11 van Finance

### <a name="norwegian-standard-main-accounts"></a>Standaard hoofdrekeningen Noors

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Nieuw ontwerp  |
| **Vervangen door een andere functie?**   | Ja (vervangen door specifieke aanvraagparameters voor ER-indeling) |
| **Betrokken productgebieden**         | Aanvraag |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 april 2021 wordt de functionaliteit die is gerelateerd aan standaard hoofdrekeningen niet meer ondersteund: verwijzingsveld, gerelateerde tabel, gegevensentiteit. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Verwijderde of verouderde functies in versie 10.0.7 van Finance

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialoogvenster Wijziging in werkstroom aanvragen bevat niet langer een vervolgkeuzelijst voor gebruikersselectie

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Gewijzigd in de functie met selectie van rekeninggroepen.  |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Workflow |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: op 1 december 2020 worden Chinese boekingstypen niet meer ondersteund zonder dat rekeninggroepen zijn geselecteerd. Meer informatie over het nieuwe ontwerp is te vinden in [Nieuwe functies in 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies
Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

