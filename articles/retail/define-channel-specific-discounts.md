---
title: "Kanaalspecifieke kortingen definiëren"
description: Detailhandelaren stellen vaak verschillende kortingen voor verschillende afzetkanalen in. In dit onderwerp komen de concepten aan bod die u moet kennen om een korting voor een bepaald afzetkanaal te maken.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: d40c37628f03a7605e04b95339072a67806f2fa1
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="define-channel-specific-discounts"></a>Kanaalspecifieke kortingen definiëren

[!include[banner](includes/banner.md)]


Detailhandelaren stellen vaak verschillende kortingen voor verschillende afzetkanalen in. In dit onderwerp komen de concepten aan bod die u moet kennen om een korting voor een bepaald afzetkanaal te maken. 

<a name="channel-specific-discounts"></a>Kanaalspecifieke kortingen
--------------------------

Detailhandelaren bieden vaak verschillende kortingen in verschillende afzetkanalen aan. Dit vindt mogelijk plaats om zich te richten op lokale marktvoorwaarden of de strijd aan te gaan met concurrerende detailhandelaren.

Microsoft Dynamics 365 for Retail gebruikt prijsgroepen om kanaalspecifieke kortingen te definiëren. De prijsgroepen kunnen aan een of meer van de volgende entiteiten worden toegewezen: kanalen, catalogi, aansluitingen, en loyaliteitsprogramma's. Dit artikel bespreekt kanalen, maar dezelfde concepten gelden voor cataloguskortingen, aansluitingskortingen, en loyaliteitskortingen.

## <a name="price-groups"></a>Prijsgroepen

[![Prijsgroepen](./media/price-groups-1024x608.png)](./media/price-groups.png)

Het bovenstaande diagram illustreert de relatie tussen entiteiten die mogelijk in een transactie aanwezig zijn (kanaal, catalogus, klant, klantenbindingskaart) en de verschillende kortingssoorten die kunnen worden geconfigureerd. Alle transacties vinden plaats in een kanaal. Het kanaal is dus gegarandeerd aanwezig in een transactie. De resterende entiteiten zijn optioneel. Op elke hoofdgegevenspagina is er een koppeling naar een bijbehorende prijsgroepenpagina waar u desgewenst prijsgroepen kunt weergeven en toevoegen. Een prijsgroep wordt gebruikt om vier verschillende typen entiteiten te verbinden met kortingen, prijscorrecties en handelsovereenkomsten. Het is raadzaam een strategie te plannen voor de wijze waarop u uw prijsgroepen benoemt om ze georganiseerd te houden. U kunt bijvoorbeeld voorvoegsel of achtervoegsel in de vorm van een letter of getal gebruiken om onderscheid te maken tussen de verschillende typen. Bijvoorbeeld: 1-xxxxx voor kanaalprijsgroepen en 2-xxxxx voor catalogusprijsgroepen. Er zijn vier querypagina's die zich op elk van de detailhandelsentiteiten richten en waaraan kortingen kunnen worden gekoppeld.

-   **Prijsgroepen detailhandelkanaal** - Deze pagina bevat een lijst van kanalen en kortingen samen voor elke prijsgroep.
-   **Catalogusprijsgroepen** - Deze pagina bevat een lijst van catalogi en kortingen samen voor elke prijsgroep.
-   **Loyaliteitsprijsgroepen** - Deze pagina bevat een lijst van loyaliteitsprogramma´s en kortingen samen voor elke prijsgroep.
-   **Prijsgroepen voor aansluitingen** - Deze pagina bevat een lijst van aansluitingen en kortingen samen voor elke prijsgroep.

## <a name="example-channel-discount-set-up"></a>Voorbeeld van kanaalkorting instellen
Het volgende voorbeeld illustreert de taken die bij het instellen van een kanaalkorting moeten worden uitgevoerd.

1.  Voor dit voorbeeld hebt u een kanaal genaamd **Houston** en gaat u een nieuwe korting maken genaamd **Terug-naar-school.**
2.  Omdat de prijs- en kortingsstrategie de mogelijkheid van kanaalkortingen omvat, maakt u altijd een kanaal-specifieke prijsgroep wanneer u een kanaal maakt.
3.  U hebt de prijsgroep **Houston-PG** en deze wordt toegewezen aan het **Houston**-kanaal.
4.  Nadat u de nieuwe korting **Terug-naar-school** hebt gemaakt, moet u op **Prijsgroepen** bovenaan de pagina **Korting** klikken. De pagina **Kortingsprijsgroepen** wordt geopend. Klik op **Nieuw** en selecteer de prijsgroep **Houston-PG**.
5.  U kunt nu de korting activeren en doorgeven aan het kanaal.

 

<a name="see-also"></a>Zie ook
--------

[Acties en kortingen](price-adjustments-discounts.md)



