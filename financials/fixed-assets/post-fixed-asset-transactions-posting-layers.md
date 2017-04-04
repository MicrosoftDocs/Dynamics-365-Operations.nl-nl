---
title: Vaste-activatransacties naar boekingslagen boeken
description: Dit artikel geeft een overzicht van boekingslaagfunctionaliteit voor vaste-activatransacties.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 4b112eee303604149c7609972a60c2014d4be423
ms.lasthandoff: 03/31/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Vaste-activatransacties naar boekingslagen boeken

Dit artikel geeft een overzicht van boekingslaagfunctionaliteit voor vaste-activatransacties.

Vaste activa worden vaak op verschillende manieren en om verschillende redenen afgeschreven. De afschrijving voor de belasting wordt berekend conform de huidige belastingregels om de hoogst mogelijke afschrijving voor de belasting te kunnen krijgen, maar het afschrijven voor rapportagedoeleinden wordt berekend conform de regels en standaarden van de boekhouding. De diverse soorten afschrijvingen worden afzonderlijk in de boekingslagen berekend en geregistreerd.

Elk boek dat is gekoppeld aan vaste activa, is ingesteld voor een bepaalde boekingslaag met een algemeen afschrijvingsdoel. Er zijn tien boekingslagen: Huidig, Bewerkingen, Btw en zeven douanelagen. U kunt het boeken naar het algemene grootboek voor het boek ook uitschakelen door het veld Boeken naar grootboek in te stellen op Nee. Het veld Boekingslaag wordt dan automatisch ingesteld op Geen. Normaal gesproken worden boeken die niet naar het grootboek boeken gebruikt voor btw-aangifte. Deze benadering biedt u de extra flexibiliteit om historische transacties voor de vaste activa te verwijderen, omdat ze nog niet toegewezen aan het grootboek is.

Vaste-activajournalen worden bepaald door de pagina Journaalnamen in Grootboek > Journaalinstellingen > Journaalnamen. Elk journaal waarin u afschrijvingen kunt boeken, wordt voor slechts één boekingslaag door de journaalnaam gedefinieerd. De boekingslaag in het journaal kan niet worden gewijzigd. Deze beperking zorgt dat de transacties voor elke boekingslaag gescheiden blijven. Voor elke boekingslaag moet er minstens één journaalnaam worden gemaakt. Als u afschrijvingsboeken gebruikt die niet naar het grootboek boeken, moet u ook een journaal waarin de boekingslaag is ingesteld op geen.

U kunt grootboekrekeningen toewijzen voor vaste-activatransacties op de pagina Boekingsprofielen voor vaste activa. Voor elk boekingsprofiel moet u het relevante transactietype en boek selecteren, en vervolgens de grootboekrekeningen aangeven. Stel een boekingsprofielrecord in voor elk boek dat naar het grootboek wordt geboekt.

> [!NOTE] 
> Met behulp van afgeleide boeken, kunt u transacties naar verschillende boekingslagen boeken op hetzelfde moment. U maakt de transacties van het primaire boek in een journaal waarvan de boekingslaag overeenkomt met de boekingslaag van het boek. Tijdens het boeken worden de transacties van het afgeleide boek naar de respectieve boekingslagen geboekt.

Zie voor meer informatie, [afgeleid boeken](derived-books.md) en [boeken met afgeleide boeken](post-derived-value-models.md).


