---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (8 oktober 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40898ca7f54089337180def964b8942e8653663b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529475"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (8 oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

De wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2542. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Verwijdering van open inschrijving voor voordelen uit openbare preview

In combinatie met onze mededeling in het blogbericht [Strategische investeringen Core HR dragen bij tot uitmuntendheid](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) verwijdert Microsoft de functie Open inschrijving voor voordelen uit de openbare preview-versie op 18 oktober 2019. In plaats daarvan wordt in de toekomst nieuwe functionaliteit uitgebracht. Productiegebruik van de functie open inschrijving voor voordelen die momenteel in openbare preview is, wordt niet ondersteund. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Integratie met Common Data Service is nu standaard uitgeschakeld voor nieuwe inrichtingen (343675)
 
Wanneer nieuwe omgevingen worden ingericht, is de integratie met Common Data Service nu uitgeschakeld. Meer informatie vindt u in [Common Data Service-integratie configureren](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Gestroomlijnde invoer en navigatie voor werknemers

Functionaliteit voor navigatie en de invoer van werknemers is nu beschikbaar in alle omgevingen. Als u deze functie wilt inschakelen, gaat naar **Systeembeheer \> Koppelingen \> Instellen \> Systeemparameters \> Preview-functie** en selecteert u **Verbeterd medewerkersformulier en navigatie**. De functie wordt vervolgens voor alle gebruikers ingeschakeld. U kunt deze optie op elk gewenst moment uitschakelen.

Zie voor meer informatie [Gestroomlijnde invoer van werknemersgegevens](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) in het Dynamics 365: releasewave 2-plan van 2019.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Met Aantrekken en Onboarden worden inactieve werknemers gemaakt in Core HR (380517)

Met de release van deze week wordt een probleem gecorrigeerd waarbij met Aantrekken en Onboarden inactieve werknemers worden gemaakt in Core HR.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>De werkstroom mislukt als de manager tijdens het beëindigen van de aanstelling van een werknemer is aangemeld bij een ander bedrijf (346852)

De werkstroom mislukt niet meer op basis van de rechtspersoon waarbij de manager is aangemeld.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Ontbrekende informatie over HcmOnboardingWorkerChecklistTaskEntity (349591)

Deze release bevat aanvullende informatie over **HcmOnboardingWorkerChecklistTaskEntity**. Hieronder vindt u enkele voorbeelden:

- **Groepsnaam** wanneer het toegewezen type **groep** is
- **Werknemersnaam** wanneer het toegewezen type **werknemer** is
- **Managernaam** wanneer het toegewezen type **manager** is

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Entiteiten worden niet in alfabetische volgorde weergegeven in Common Data Service-beheer (377414)

Entiteiten worden nu in alfabetische volgorde weergegeven op de pagina **CDS-beheer**.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Als het type dienstverband wordt gewijzigd met een datum in de toekomst, is toewijzing van een positie niet toegestaan (339958)

Met deze wijziging zijn positietoewijzingen mogelijk wanneer medewerkerstypen worden gewijzigd (bijvoorbeeld van werknemer in contractant).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Wanneer de transactie-entiteit Bank verlaten van Common Data Service wordt bijgewerkt, wordt er een nieuwe record gemaakt in Talent (352938)

De transactie Verlaten wordt nu bijgewerkt wanneer Common Data Service wordt bijgewerkt voor Bank verlaten-transacties.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>De titel van bijlagen voor feedbackitems bevat de feedbackbeschrijving (343765)

De feedbackbeschrijving wordt niet meer weergegeven in de titel van de bijlage.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Het veld Opmerkingen bij werkstroomcompensatie bevat onjuiste inhoud (339297)

Deze wijziging toont de inhoud van het veld **%HcmActionState.HcmWorkerActionComment.Comments%**.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity en WorkCalendarDayEntity worden niet weergegeven via OData (376329)

In deze versie zijn **WorkCalendarEntity** en **WorkCalendarDayEntity** nu beschikbaar via OData (Open Data Protocol).

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity is traag wanneer OData wordt gebruikt (375221)

Wijzigingen verbeteren de prestaties van **HCMWorkerEntity** wanneer de ontwerper van Microsoft Excel-werkmappen wordt gebruikt.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>De boeking in journaal van managerprestaties geeft een fout weer nadat een prestatiejournaal is verwijderd en er een nieuw prestatiejournaal is gemaakt (336061)

Deze release corrigeert een probleem dat optreedt nadat een prestatiejournaal is verwijderd en direct daarna een nieuw wordt gemaakt. Deze correctie wijzigt het gedrag van de self-service voor managers.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="print-performance-reviews"></a>Prestatiebeoordelingen afdrukken

Zie [Beoordelingen van afdrukprestaties](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in het Dynamics 365: releasewave 2-plan van 2019.


[!INCLUDE[footer-include](../includes/footer-banner.md)]