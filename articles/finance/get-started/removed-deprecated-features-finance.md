---
title: Verwijderde of afgeschafte functies in Dynamics 365 Finance
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175103"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Verwijderde of afgeschafte functies in Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Finance.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

> [!NOTE]
> Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Verwijderde of verouderde functies in versie 10.0.12 van Finance

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Poolse SSRS-rapporten: Btw-register voor verkoop, Btw-register voor inkoop, Btw-register EU-overzicht – functieverwijzing PL-00014

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Niet wettelijk vereist.  |
| **Vervangen door een andere functie?**   | Ja (Excel-indeling voor standaardauditbestand met btw-aangifte - JPK_VDEK) |
| **Betrokken productgebieden**         | Aanvraag |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 juli 2021 worden de SSRS-rapporten niet meer ondersteund: **Btw-register voor verkoop, Btw-register voor inkoop, Btw-register EU-overzicht – functieverwijzing PL-00014**. In plaats daarvan wordt een voorbeeld van een Excel-indeling geïntroduceerd voor het standaardauditbestand met btw-aangifte (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Verwijderde of verouderde functies in versie 10.0.11 van Finance

### <a name="norwegian-standard-main-accounts"></a>Standaard hoofdrekeningen Noors

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Nieuw ontwerp  |
| **Vervangen door een andere functie?**   | Ja (vervangen door specifieke aanvraagparameters voor ER-indeling) |
| **Betrokken productgebieden**         | Aanvraag |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 april 2021 wordt de functionaliteit die is gerelateerd aan standaard hoofdrekeningen niet meer ondersteund: verwijzingsveld, gerelateerde tabel, gegevensentiteit. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Verwijderde of verouderde functies in versie 10.0.7 van Finance

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialoogvenster Wijziging in werkstroom aanvragen bevat niet langer een vervolgkeuzelijst voor gebruikersselectie
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Gewijzigd in de functie met selectie van rekeninggroepen.  |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Workflow |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: op 1 december 2020 worden Chinese boekingstypen niet meer ondersteund zonder dat rekeninggroepen zijn geselecteerd. Meer informatie over het nieuwe ontwerp is te vinden in [Nieuwe functies in 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies
Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.
