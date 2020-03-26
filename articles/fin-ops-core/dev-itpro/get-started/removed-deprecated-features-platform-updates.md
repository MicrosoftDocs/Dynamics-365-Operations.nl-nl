---
title: Verwijderde of afgeschafte Platform-functies
description: In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van Finance and Operations-apps.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095769"
---
# <a name="removed-or-deprecated-platform-features"></a>Verwijderde of afgeschafte Platform-functies

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van Finance and Operations-apps.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

> [!NOTE]
> Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="platform-update-32"></a>Platformupdate 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialoogvenster Wijziging in werkstroom aanvragen bevat niet langer een vervolgkeuzelijst voor gebruikersselectie
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dit was een beveiligingsprobleem omdat de aanvraag voor wijziging naar een onbedoelde gebruiker kon worden verzonden. Dit was ook een bruikbaarheidsprobleem omdat de gebruiker werd gedwongen te bepalen bij wie de werkstroom oorspronkelijk vandaan kwam en deze handmatig te selecteren.  |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Werkstroom |
| **Implementatieoptie**              | Alle |
| **Status**                         | De vervolgkeuzelijst voor gebruikersselectie werd in Platform update 32 verwijderd uit het dialoogvenster Wijziging in werkstroom aanvragen. Aanvragen voor verzoeken om wijzigingen worden automatisch naar de persoon verzonden bij wie de werkstroom oorspronkelijk vandaan kwam, zoals bedoeld. Zie [Acties in goedkeuringsprocessen voor werkstroom](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change) voor meer informatie over deze functionaliteit. |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Ingesloten drillthrough-koppelingen worden niet meer ondersteund in gepagineerde documenten die worden weergegeven door de cloudgehoste service 
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Navigatie-URL's die zijn ingesloten in documenten die door de service worden weergegeven, kunnen gevoelige bedrijfsgegevens bevatten. De ondersteuning voor ingesloten drillthrough-koppelingen in documenten wordt verwijderd als een beveiligingsmaatregel om de gegevens van klanten beter te beschermen. Gebruikers profiteren ook van betere prestaties en kunnen interactief documenten genereren als gevolg van deze wijziging.  |
| **Vervangen door een andere functie?**   | No |
| **Betrokken productgebieden**         | Rapportage |
| **Implementatieoptie**              | Alle |
| **Status**                         | Deze functie wordt actief uit de service verwijderd.<br><br>De moderne client biedt talloze opties voor het produceren van weergaven die automatisch gegenereerde koppelingen bevatten om te helpen bij het navigeren door de toepassing. Gepagineerde documenten die door de service worden weergegeven, worden aanbevolen voor externe communicatie die per e-mail wordt verzonden, gearchiveerd en afgedrukt voor ontvangers. We hebben de ervaring verbeterd voor het direct bekijken van documenten in de browser, die rechtstreeks toegang biedt tot lokale printers. Zie [PDF-documenten bekijken met een ingesloten viewer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents) voor meer informatie. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies
Zie [Verwijderde of afgeschafte functies in eerdere versies](../migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.

