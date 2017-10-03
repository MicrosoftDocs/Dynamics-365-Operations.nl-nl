---
title: Vaste-activatransacties boeken naar boekingslagen
description: Dit artikel geeft een overzicht van boekingslaagfunctionaliteit voor vaste-activatransacties.
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2d65dca16cf4ead60c8664066828240c82e58a4f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Vaste-activatransacties boeken naar boekingslagen

[!include[banner](../includes/banner.md)]


Dit artikel geeft een overzicht van boekingslaagfunctionaliteit voor vaste-activatransacties.

Vaste activa worden vaak op verschillende manieren en om verschillende redenen afgeschreven. De afschrijving voor de belasting wordt berekend conform de huidige belastingregels om de hoogst mogelijke afschrijving voor de belasting te kunnen krijgen, maar het afschrijven voor rapportagedoeleinden wordt berekend conform de regels en standaarden van de boekhouding. De diverse soorten afschrijvingen worden afzonderlijk in de boekingslagen berekend en geregistreerd.

Elk boek dat is gekoppeld aan vaste activa, is ingesteld voor een bepaalde boekingslaag met een algemeen afschrijvingsdoel. Er zijn tien boekingslagen: Huidig, Bewerkingen, Btw en zeven douanelagen. U kunt het boeken naar het algemene grootboek voor het boek ook uitschakelen door het veld Boeken naar grootboek in te stellen op Nee. Het veld Boekingslaag wordt dan automatisch ingesteld op Geen. De boeken die niet naar het grootboek boeken, worden gewoonlijk gebruikt voor belastingaangiftes. Deze aanpak geeft u meer flexibiliteit om historische transacties voor het activumboek te verwijderen, omdat ze niet in het grootboek zijn bevestigd.

Vaste-activajournalen worden bepaald door de pagina Journaalnamen in Grootboek > Journaalinstellingen > Journaalnamen. Elk journaal waarin u afschrijvingen kunt boeken, wordt voor slechts één boekingslaag door de journaalnaam gedefinieerd. De boekingslaag in het journaal kan niet worden gewijzigd. Deze beperking zorgt dat de transacties voor elke boekingslaag gescheiden blijven. Voor elke boekingslaag moet er minstens één journaalnaam worden gemaakt. Als u boeken gebruikt die niet naar het grootboek boeken, moet u ook een journaal maken waarin de boekingslaag is ingesteld op Geen.

U kunt grootboekrekeningen toewijzen voor vaste-activatransacties op de pagina Boekingsprofielen voor vaste activa. Voor elk boekingsprofiel moet u het relevante transactietype en boek selecteren, en vervolgens de grootboekrekeningen aangeven. Stel een boekingsprofielrecord in voor elk boek dat naar het grootboek wordt geboekt.

> [!NOTE] 
> Door afgeleide boeken te gebruiken, kunt u tegelijkertijd transacties naar verschillende boekingslagen boeken. U maakt de transacties van het primaire boek in een journaal waarvan de boekingslaag overeenkomt met de boekingslaag van het boek. Tijdens het boeken worden de transacties van het afgeleide boek naar de respectieve boekingslagen geboekt.

Zie voor meer informatie [Afgeleide boeken](derived-books.md) en [Boeken met afgeleide boeken](post-derived-value-models.md).



