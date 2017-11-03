---
title: Hybride klantorders
description: Een hybride klantorder is een enkele order, die producten bevat die door de klant vanuit de winkel kunnen worden getransporteerd, alsmede de producten die later worden opgehaald of verzonden.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3b330b64c1427517866b17b62ac441a4a8bed2f0
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="hybrid-customer-orders"></a>Hybride klantorders

[!include[banner](includes/banner.md)]


Een hybride klantorder is een enkele order, die producten bevat die door de klant vanuit de winkel kunnen worden getransporteerd, alsmede de producten die later worden opgehaald of verzonden.

In Microsoft Dynamics 365 for Retail kunt u aangeven dat u alle producten of geselecteerde producten voor een klantorder wilt uitvoeren. De productregels die zijn gemarkeerd om te worden uitgevoerd, worden automatisch gefactureerd nadat de order is gemaakt. Dit geldt ook voor een order die moet worden opgehaald nadat de order is gemaakt. Het verschuldigde bedrag op hybride orders wordt bepaald door het aanbetalingspercentage op productregels voor verzamelen en verzenden met het volledige bedrag van de uitvoerregels. Voor hybride orders wordt als volgt geschakeld tussen de klantordermodus en de cash-and-carry-modus:

-   Als alle producten in de winkelwagen zijn ingesteld op **Leveringsmethode uitvoeren**, wordt de order verwerkt als een contante transactie.
-   Als sommige of alle regels in de winkelwagen worden ingesteld op **Verzamelen** of **Levering verzenden**, wordt de order verwerkt als een klantordertransactie.

Als een winkelwagenregel is geselecteerd en **Selectie kiezen**, **Selectie verzenden** of **Selectie uitvoeren** is ingeschakeld, wordt alleen de specifieke winkelwagenregel ingesteld met die leveringsmethode. In dat geval blijft de downstreamflow van de bewerking doorgaan zoals gebruikelijk. Echter als **Selectie kiezen**, **Selectie verzenden** of **Selectie uitvoeren** is geselecteerd zonder dat een winkelwagenregel wordt geselecteerd, wordt een nieuwe pagina geopend waarin alle regels van de winkelwagenregels worden weergegeven. Op dat scherm kunt u meerdere regels tegelijk selecteren voor het instellen van de leveringsmethode. Wanneer u die methode gebruikt voor het selecteren van regels, worden eventuele vorige leveringsmethoden, die zijn toegewezen aan de regel, overschreven.

<a name="see-also"></a>Zie ook
--------

[Overzicht van klantbestellingen](customer-orders-overview.md)




