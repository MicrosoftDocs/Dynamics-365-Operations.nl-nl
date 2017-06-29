---
title: Productieorders als voltooid melden
description: Gereedmelden is een productiefase. In deze fase wordt een eindproduct gemeld en van de productieorder verplaatst naar de voorraad.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 52607d645c6eaf4ff97d2c4bf8abc6ec1374fd7e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="report-production-orders-as-finished"></a>Productieorders als voltooid melden

[!include[banner](../includes/banner.md)]


Gereedmelden is een productiefase. In deze fase wordt een eindproduct gemeld en van de productieorder verplaatst naar de voorraad.

Wanneer een hoeveelheid van de eindproducten wordt gereedgemeld op een productieorder, wordt dit in de voorraad bijgewerkt als voorhanden. Gedeeltelijke hoeveelheden van de oorspronkelijk geplande orderhoeveelheid kunnen worden gereedgemeld. Het is ook mogelijk om fouthoeveelheden met een bijbehorende foutreden te rapporteren bij het gereedmelden van hoeveelheden. Wanneer de productieorder de fase Gereedgemeld bereikt, geeft deze aan dat er geen hoeveelheid meer zal worden gerapporteerd op de productieorder.
De volgende kenmerken worden ook gekoppeld aan het proces **Gereedmelden**:
-   Het is mogelijk om verbruik van grondstoffen en tijd in te stellen die in verhouding zijn met de gerapporteerde hoeveelheid (wisprincipe)
-   Weggezet werk kan worden gegenereerd voor artikelen die voor magazijnprocessen zijn ingeschakeld.
-   U kunt instellen dat de geplande of standaard kostprijs van de afgewerkte goederen moet worden gerapporteerd op grootboekrekeningen.
-   U kunt een kwaliteitsorder maken voor de gerapporteerde hoeveelheid op basis van de instellingen van een kwaliteitskoppeling.

De hoeveelheid wordt gerapporteerd aan de uitvoerlocatie. Magazijnwerk wordt dan gegenereerd om de hoeveelheid van de uitvoerlocatie te verplaatsen naar de definitieve bestemming die is gedefinieerd door de locatierichtlijn voor het weggezette werk.

-   U kunt een kwaliteitsorder maken wanneer een productieorder wordt gereedgemeld als een kwaliteitskoppeling is ingesteld.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Een productieorder instellen op Gereedgemeld
U kunt een productieorder instellen op **Gereedgemeld** via de standaardfunctie voor het bijwerken van productieorders of via de route- en taakkaartjournalen of via het journaal **Gereedmelden**. U kunt de fase ook bijwerken naar **Gereedgemeld** via de pagina's Taakkaartterminal en Apparaat voor taakkaarten, wanneer u over de laatste taak van de productieorder rapporteert. Tenslotte kunt u de optie **Gereedmelden** inschakelen als een proces voor de oplossing met handbediende magazijnapparaten.  




