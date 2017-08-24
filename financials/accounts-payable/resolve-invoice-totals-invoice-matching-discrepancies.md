---
title: Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 8ccc1af0e1bd7909b7810d359a916849ecc1a709
ms.contentlocale: nl-nl
ms.lasthandoff: 08/09/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen

[!include[banner](../includes/banner.md)]




Een type factuurvereffeningsvalidatie is de factuurtotalenvereffening. Om op te geven dat het systeem factuurvereffening voor totalen moet uitvoeren, stelt u op de pagina **Parameters van module Leveranciers** op het tabblad **Factuurvalidatie** u de optie **Factuurtotalen vereffenen** in op **Ja**. 

U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil. Er worden zes totalen vergeleken op de **Totale factuurvereffeningsgegevens** pagina. Indien een van de totalen afwijkt van het verwachte corresponderende inkoopordertotaal, wordt een matchingverschil gemarkeerd. 

Om de factuur met verschillende totalen in te zien, klikt u in de werkruimte op in de **Leveranciersfactuurregistratie** op de regel **Facturen in behandeling**. Klik vervolgens in het actievenster op het tabblad **Controleren** op **Vereffeningsgegevens**. Als vereffeningsverschillen zijn gevonden, worden waarschuwende pictogrammen naast het factuurbedrag weergegeven. U kunt meer details over de totalen weergeven door de vergelijkingsgegevens van de factuurtotalen te bekijken. 

Nadat u het verschil hebt aangegeven, kunt u contact opnemen met de leverancier als u denkt dat de informatie op de factuur niet klopt. Afhankelijk van de uitkomst van dat gesprek kan de leverancier een van de volgende dingen doen:

-   Accepteer het prijsverschil en boek de factuur die matchingverschillen bevat. Uw systeem kan worden ingesteld om goedkeuring te vereisen voordat kan worden geboekt als er vereffeningsverschillen zijn. In dit geval moet u het vereffeningverschil goedkeuren en kunt u desgewenst een goedkeuringopmerking invoeren. U kunt vervolgens de factuur boeken.
-   Het factuurbedrag met het juiste bedrag corrigeren en de factuur boeken.
-   Een volledig credit aan de leverancier vragen en om een nieuwe, gecorrigeerde factuur verzoeken.

Zie voor meer informatie [Uitzonderingen onderzoeken of oplossen](tasks/research-resolve-exceptions.md).



