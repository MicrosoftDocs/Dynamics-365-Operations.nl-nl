---
title: Verwijderde of afgeschafte functies in Dynamics 365 Finance
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: e6a391b10ddaef79e68f47afae7d77135a1c333a
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184120"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Verwijderde of afgeschafte functies in Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

> [!NOTE]
> Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](/dynamics/s-e/global/axtechrefrep_61). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Verwijderde of verouderde functies in versie 10.0.20 van Finance

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>Configuratie van de HU-indeling ('RTIR Query Invoice Data Request') voor elektronische rapportage (ER)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Uitgesloten van verwerking van elektronische berichten bij samenwerking met Hongaars online factureringssysteem |
| **Vervangen door een andere functie?**   | No |
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
