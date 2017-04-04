---
title: "Kanaalspecifieke kortingen definiëren"
description: Detailhandelaren stellen vaak verschillende kortingen voor verschillende afzetkanalen in. In dit onderwerp komen de concepten aan bod die u moet kennen om een korting voor een bepaald afzetkanaal te maken.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Kanaalspecifieke kortingen definiëren

Detailhandelaren stellen vaak verschillende kortingen voor verschillende afzetkanalen in. In dit onderwerp komen de concepten aan bod die u moet kennen om een korting voor een bepaald afzetkanaal te maken. 

<a name="channel-specific-discounts"></a>Kanaalspecifieke kortingen
--------------------------

Detailhandelaren kortingspercentages vaak verschillende in verschillende kanalen. Dit is mogelijk worden gedaan op lokale markt-voorwaarden adres of omgaan met concurrerende detailhandelaren.

Detailhandel en commerce in Microsoft Dynamics 365 voor bewerkingen gebruikt prijsgroepen kanaal specifieke kortingen. De prijsgroepen kunnen aan een of meer van de volgende entiteiten worden toegewezen: kanalen, catalogi, aansluitingen, en loyaliteitsprogramma's. Dit artikel bespreekt kanalen, maar dezelfde concepten gelden voor cataloguskortingen, aansluitingskortingen, en loyaliteitskortingen.

## <a name="price-groups"></a>Prijsgroepen
\[Bijschrift-id = "bijlage\_256084 ' uitlijnen 'alignnone' breedte = '640' =\][![prijsgroepen](./media/price-groups-1024x608.png)](./media/price-groups.png) groep koppelingen prijs for Retail\[/bijschrift\]

De bovenstaande afbeelding illustreert de relatie tussen entiteiten die mogelijk op een transactie (kanaal, catalogus, aansluiting, klant, loyaliteitskaart) en de verschillende kortingssoorten die kunnen worden geconfigureerd. Alle transacties plaatsvinden in een kanaal, zodat het kanaal is gegarandeerd aanwezig in een transactie. De resterende entiteiten zijn optioneel. Op elke hoofdgegevenspagina is er een koppeling naar een bijbehorende prijsgroepenpagina waar u desgewenst prijsgroepen kunt weergeven en toevoegen. Een prijsgroep wordt gebruikt om te relateren van vier verschillende typen entiteiten aan kortingen, prijscorrecties en handelsovereenkomsten. Het is raadzaam dat u van plan een strategie bent voor hoe u uw prijsgroepen bewaring ingedeeld wordt naam. Gebruik een letter of voorvoegsel of achtervoegsel onderscheid maken tussen de verschillende typen wordt één optie. Bijvoorbeeld: 1-xxxxx voor prijsgroepen en 2-xxxxx voor catalogus prijsgroepen. Er zijn vier querypagina's die zich op elk van de detailhandelsentiteiten richten en waaraan kortingen kunnen worden gekoppeld.

-   **Prijsgroepen detailhandelkanaal **- Deze pagina bevat een lijst van kanalen en kortingen samen voor elke prijsgroep.
-   **Catalogusprijsgroepen **- Deze pagina bevat een lijst van catalogi en kortingen samen voor elke prijsgroep.
-   **Loyaliteitsprijsgroepen **- Deze pagina bevat een lijst van loyaliteitsprogramma´s en kortingen samen voor elke prijsgroep.
-   **Prijsgroepen voor aansluitingen **- Deze pagina bevat een lijst van aansluitingen en kortingen samen voor elke prijsgroep.

## <a name="example-channel-discount-set-up"></a>Voorbeeld van kanaalkorting instellen
Het volgende voorbeeld illustreert de taken die bij het instellen van een kanaalkorting moeten worden uitgevoerd.

1.  Voor dit voorbeeld hebt u een kanaal genaamd **Houston** en gaat u een nieuwe korting maken genaamd **Terug-naar-school.**
2.  Omdat de prijs- en kortingsstrategie de mogelijkheid van kanaalkortingen omvat, maakt u altijd een kanaal-specifieke prijsgroep wanneer u een kanaal maakt.
3.  U hebt de prijsgroep **Houston-PG** en deze wordt toegewezen aan het **Houston**-kanaal.
4.  Nadat u de nieuwe korting **Terug-naar-school** hebt gemaakt, moet u op **Prijsgroepen** bovenaan de pagina **Korting** klikken. De pagina **Kortingsprijsgroepen** wordt geopend. Klik op **Nieuw** en selecteer de prijsgroep **Houston-PG**.
5.  U kunt nu de korting activeren en doorgeven aan het kanaal.

 

<a name="see-also"></a>Zie ook
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


