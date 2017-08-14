---
title: Werkgebied Beheer van vaste activa
description: Dit onderwerp bevat informatie over het werkgebied Beheer van vaste activa. Dit werkgebied bevat informatie die betrekking heeft op de vaste activa die zijn ingevoerd in het systeem. Het bevat een overzichtsweergave en een analyseweergave.
author: saraschi
manager: AnnBe
ms.date: 06/06/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 69f728c5b5897d7210941643d2c7d0d7abf054fa
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="fixed-asset-management-workspace"></a>Werkgebied Beheer van vaste activa

[!include[banner](../includes/banner.md)]

Het werkgebied **Beheer van vaste activa** bevat informatie die betrekking heeft op de vaste activa die zijn ingevoerd in het systeem. Dit werkgebied bevat een overzichtsweergave en een analyseweergave. Het tabblad **Mijn werk** bevat overzichtstegels, vaste-activadetails en gerelateerde informatie over vaste activa in het huidige bedrijf. U kunt ook rechtstreeks in het werkgebied analyses toevoegen aan de sectie Power BI-analyses. Op het tabblad **Analyses - alle bedrijven** worden mogelijkheden van Microsoft Power BI gebruikt om visuele elementen weer te geven die zijn gerelateerd aan vaste activa in alle bedrijven.

## <a name="my-work"></a>Mijn werk

### <a name="summary"></a>Overzicht

De tegels in de sectie **Overzicht** bevatten een overzicht van uw vaste activa. De informatie bevat metrische gegevens over activa die nog niet zijn verworven, activa die gedurende het huidige jaar zijn verworven en activa die zijn afgestoten tijdens het huidige jaar. De sectie **Overzicht** heeft ook een snelle navigatie naar de lijstpagina **Vaste activa**, het batchafschrijvingsvoorstel en het vaste-activajournaal.

### <a name="find-fixed-assets"></a>Vaste activa zoeken

Met de sectie **Vaste activa zoeken** kunt u snel naar activa zoeken door het vaste-activanummer, de groep, de naam, de locatie of de verantwoordelijke persoon op te geven. Alle activa die overeenkomen met de zoekcriteria worden weergegeven in de lijst.

In de lijst kunt u de volgende pagina's weergeven:

 - Pagina **Details** voor de vaste activa
 - Pagina **Boeken** voor alle boeken die zijn gekoppeld aan de vaste activa
 - Pagina **Vaste-activawaarderingen**

### <a name="valuations"></a>Waarderingen

Op de pagina **Vaste-activawaarderingen** kunt u op één pagina de belangrijkste informatie over vaste activa zien, en ook details voor alle boeken die zijn gekoppeld aan het vaste activum. De optie **Saldi** linksboven op de pagina toont de huidige waardering voor elk boek dat is gekoppeld aan het vaste activum. U kunt inzoomen vanuit de waarden om de gedetailleerde transacties te zien waaruit de overzichtswaarde bestaat. De optie **Profiel** linksboven op de pagina toont het huidige afschrijvingsschema voor elk boek dat is gekoppeld aan het vaste activum.

U hebt toegang tot de pagina **Vaste-activawaarderingen** via het werkgebied **Beheer van vaste activa** of de lijstpagina **Vaste activum**.

### <a name="related-information"></a>Verwante informatie

U kunt rechtstreeks naar de pagina **Boeken instellen**, pagina **Query vaste-activatransactie** en diverse rapporten gaan met behulp van de koppelingen in de sectie **Verwante informatie** van het werkgebied.

### <a name="analytics--all-companies"></a>Analyses - alle bedrijven

De pagina **Analyses** bevat belangrijke metrische gegevens over vaste activa in alle rechtspersonen in het systeem. Toegang tot dit tabblad wordt beheerd door de beveiligingsbevoegdheid Analyse van vaste activa voor alle bedrijven weergeven.

In de volgende tabel ziet u de visualisaties die op elke rapportpagina beschikbaar zijn.

| Rapportpagina            | Visualisatie        |
|------------------------|----------------------|
| Vaste-activawaarderingen | Totale nettoboekwaarde |
| Vaste-activawaarderingen | Nettoboekwaarden per vaste-activagroep |
| Vaste-activawaarderingen | Aanschafwaarden |
| Vaste-activawaarderingen | Afstotingswaarden |
| Vaste-activawaarderingen | Gegevens voor vaste activa |
| Waarderingstoewijzingen        | Totale nettoboekwaarde |
| Waarderingstoewijzingen        | Locaties vaste activa |
| Waarderingstoewijzingen        | Gegevens voor vaste activa |

Als u de analyses met gegevens wilt weergeven, moet u eerst de samengevoegde meting AssetTransactionMeasure vernieuwen op de pagina **Entiteitsopslag**.

