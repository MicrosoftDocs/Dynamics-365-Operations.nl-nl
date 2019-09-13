---
title: Standaardkosten voor arbeid en onkosten configureren
description: In dit onderwerp wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867721"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Standaardkosten voor arbeid en onkosten configureren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt. In deze taak wordt de gegevensset van USSI gebruikt.

1. Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Kostprijs (uur)**.
2. Selecteer **Nieuw**.
3. Voer een datum in het veld **Begindatum** in.
4. Voer in het veld **Kostprijs** een getal in. U kunt een standaardkostprijs voor de projectcategorie instellen of u kunt een kostprijs instellen per werknemernummer, projectnummer, categorie, datum of elke combinatie van deze factoren. De kostprijs met het hoogste detailniveau wordt toegepast.  
5. Selecteer **Opslaan**.
6. Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Verkoopprijs (uur)**.
7. Selecteer **Nieuw**.
8. Voer een datum in het veld **Begindatum** in.
9. Selecteer een optie in het veld **Geldig voor**.
10. Voer in het veld **Prijscalculatie** een getal in. U kunt een standaardverkoopprijs definiëren voor uurtransacties of voor een projectcategorie. U kunt ook verkoopprijzen instellen per werknemernummer, projectnummer, categorie, transactiedatum of een combinatie van deze. De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het Urenjournaal, is de verkoopprijs met het hoogste detailniveau. Als er bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs is gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.  
11. Selecteer **Opslaan**.
12. Sluit de pagina.
13. Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Kostprijs (onkosten)**.
14. Selecteer **Nieuw**.
15. Voer een datum in het veld **Begindatum** in.
16. Voer in het veld **Kostprijs** een getal in. Meerdere velden kunnen worden ingevuld, maar dit is het minimum wat nodig is om de record te kunnen opslaan.  
17. Selecteer **Opslaan**.
18. Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Verkoopprijs (onkosten)**.
19. Selecteer **Nieuw**.
20. Voer een datum in het veld **Begindatum** in.
21. Selecteer een optie in het veld **Geldig voor**.
22. Voer in het veld **Prijscalculatie** een getal in. De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de meest gedetailleerde verkoopprijs. Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.  
23. Selecteer **Opslaan**.

