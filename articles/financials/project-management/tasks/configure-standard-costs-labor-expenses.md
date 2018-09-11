--- 
title: Standaardkosten voor arbeid en onkosten configureren
description: In deze procedure wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.
author: KimANelson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 432b5b195b29fb03786cb0560e277735b531b7d7
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Standaardkosten voor arbeid en onkosten configureren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In deze procedure wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt. In deze taak wordt de gegevensset van USSI gebruikt.

1. Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Kostprijs (uur).
2. Klik op Nieuw.
3. Voer een datum in het veld Begindatum in.
4. Voer in het veld Kostprijs een getal in.
    * U kunt een standaardkostprijs voor de projectcategorie instellen of u kunt een kostprijs instellen per werknemernummer, projectnummer, categorie, datum of elke combinatie van deze factoren. De kostprijs met het hoogste detailniveau wordt toegepast.  
5. Klik op Opslaan.
6. Sluit de pagina.
7. Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Verkoopprijs (uur).
8. Klik op Nieuw.
9. Voer een datum in het veld Begindatum in.
10. Selecteer een optie in het veld Geldig voor.
11. Voer in het veld Prijscalculatie een getal in.
    * U kunt een standaardverkoopprijs definiëren voor uurtransacties of voor een projectcategorie. U kunt ook verkoopprijzen instellen per werknemernummer, projectnummer, categorie, transactiedatum of een combinatie van deze. De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het Urenjournaal, is de verkoopprijs met het hoogste detailniveau. Als er bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs is gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.  
12. Klik op Opslaan.
13. Sluit de pagina.
14. Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Kostprijs (onkosten).
15. Klik op Nieuw.
16. Voer een datum in het veld Begindatum in.
17. Voer in het veld Kostprijs een getal in.
    * Meerdere velden kunnen worden ingevuld, maar dit is het minimum wat nodig is om de record te kunnen opslaan.  
18. Klik op Opslaan.
19. Sluit de pagina.
20. Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Verkoopprijs (onkosten).
21. Klik op Nieuw.
22. Voer een datum in het veld Begindatum in.
23. Selecteer een optie in het veld Geldig voor.
24. Voer in het veld Prijscalculatie een getal in.
    * De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de meest gedetailleerde verkoopprijs. Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.  
25. Klik op Opslaan.


