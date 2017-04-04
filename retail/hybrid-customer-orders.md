---
title: Hybride klantorders
description: Een klantorder hybride is een enkele order, waarin producten die door de klant uit de winkel kunnen worden getransporteerd, alsmede de producten die worden opgehaald of later worden verzonden.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybride klantorders

Een klantorder hybride is een enkele order, waarin producten die door de klant uit de winkel kunnen worden getransporteerd, alsmede de producten die worden opgehaald of later worden verzonden.

In Microsoft Dynamics 365 voor bewerkingen: een leverancier, u kunt beide voert u alle producten of geselecteerde producten voor een klantorder verrichten. De product-regels die zijn gemarkeerd als verrichten automatisch gemaakt worden nadat de order wordt gemaakt, op dezelfde manier dit is hetzelfde voor een order die moet worden gepickt tot nadat de order wordt gemaakt. Het verschuldigde bedrag op hybride orders wordt bepaald door het percentage van storting op verzamelen toevoegen en product van verzendregels met het volledige bedrag van de regels uitvoeren. Voor orders van hybride schakelt u tussen klant order en Cash-and-carry-modus als volgt:

-   Als alle producten in de winkelwagen zijn ingesteld op **verrichten levering**, de volgorde worden verwerkt als een Cash and Carry-transactie.
-   Als sommige of alle regels in de winkelwagen worden ingesteld op **verzamelen** of **levering verzenden**, de volgorde worden verwerkt als een order klanttransactie.

Als een winkelwagen-regel is ingeschakeld en **selectie kiezen**, **schip geselecteerd**, of **verrichten geselecteerde** is ingeschakeld, alleen de specifieke winkelwagen-regel is ingesteld met deze leveringsmethode. In dat geval blijft de downstream stroom van de bewerking zoals gebruikelijk. Echter, als **selectie kiezen**, **schip geselecteerd**, of **verrichten geselecteerde** zonder een regel van het winkelwagentje wordt geselecteerd, een nieuwe pagina geopend waarin alle regels in de winkelwagen is geselecteerd. Op dit scherm kunt u meerdere regels tegelijk voor het instellen van de leveringsmethode. Wanneer u die methode voor het selecteren van regels, worden eventuele vorige leveringsmethode die is toegewezen aan de regel overschreven.

<a name="see-also"></a>Zie ook
--------

[Orders van klanten-overzicht](customer-orders-overview.md)


