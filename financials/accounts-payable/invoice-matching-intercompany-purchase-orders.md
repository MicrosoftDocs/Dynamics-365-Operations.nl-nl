---
title: Factuurvereffening en intercompany-inkooporders
description: De aankopende rechtspersoon die bij een intercompany-transactie betrokken is, kan worden ingesteld om factuurvereffening voor leveranciers te gebruiken. In dit geval moet aan de boekingsvereisten worden voldaan voor zowel intercompany-handel en factuurvereffening voor leveranciers voordat IC-leveranciersfacturen kunnen worden geboekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 07c101b886d33fa5fc9e8129230ca270f48c5217
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Factuurvereffening en intercompany-inkooporders

[!include[banner](../includes/banner.md)]


De aankopende rechtspersoon die bij een intercompany-transactie betrokken is, kan worden ingesteld om factuurvereffening voor leveranciers te gebruiken. In dit geval moet aan de boekingsvereisten worden voldaan voor zowel intercompany-handel en factuurvereffening voor leveranciers voordat IC-leveranciersfacturen kunnen worden geboekt.

Het voorbeeld in dit onderwerp gebruikt de volgende instellingen IC-handel:
-   Fabrikam Inkoop is de aankopende rechtspersoon.
-   Fabrikam Verkoop is de verkopende rechtspersoon.
-   Fabrikam Sales bevat klant 4020.
-   Fabrikam Purchase bevat leverancier 3024.
-   Intercompany-informatie wordt opgegeven in Fabrikam Purchase voor leverancier 3024. Fabrikam Sales wordt opgegeven als het klantbedrijf en klant 4020 wordt opgegeven als de klantrekening die met de rechtspersoon Fabrikam Purchase overeenkomt.
-   Intercompany-informatie wordt opgegeven in Fabrikam Sales voor klant 4020. Fabrikam Purchase wordt opgegeven als het leveranciersbedrijf en leverancier 3024 wordt opgegeven als de leveranciersrekening die met de rechtspersoon Fabrikam Sales overeenkomt.

Bij deze voorbeelden worden de volgende instellingen voor factuurmatching in leveranciers gebruikt voor Fabrikam Inkoop:
-   Op de pagina Parameters van module Leveranciers is de optie Factuurvereffeningsvalidatie inschakelen geselecteerd.
-   Op de pagina Parameters van module Leveranciers is het veld Factuur met verschillen boeken ingesteld op Goedkeuring vereist.
-   Het prijstolerantiepercentage voor de rechtspersoon bedraagt 2 procent.

## <a name="example-price-matching-and-intercompany-trade"></a>Voorbeeld: Prijsmatching en intercompany-handel
De nettobedragen voor de IC-leveranciersfactuur en de IC-klantfactuur moeten gelijk zijn. Deze vereiste vervangt eventuele van toepassing zijnde goedkeuringen voor factuurmatching of prijstolerantiepercentages. U volgt bijvoorbeeld deze stappen.
1.  Maak verkooporder SO888 voor klant 4020 in Fabrikam Purchase. De intercompany-inkooporder ICPO222 wordt automatisch gemaakt voor leverancier 3024 in Fabrikam Inkoop, en verkooporder ICSO888 wordt automatisch gemaakt in Fabrikam Verkoop.
2.  In Fabrikam Verkoop, registreert u dat de artikelen zijn ontvangen en boekt u een pakbon. De status van ICSO888 verandert in Geleverd. De status van ICPO222 verandert in Ontvangen.
3.  Voer in Fabrikam Verkoop een factuurupdate uit voor ICSO888. De eenheidsprijs is 0,45 en er worden 100 artikelen bijgewerkt.
4.  Maak in Fabrikam Inkoop een factuur voor ICPO222. U wijzigt de nettoprijs onopzettelijk van 45,00 naar 54,00. Er wordt een pictogram weergegeven om aan te geven dat de prijs hoger is dan de toegestane prijstolerantie van twee procent.
5.  Selecteer op de pagina Factuurvereffeningsgegevens de optie om de boeking met vereffeningsverschillen goed te keuren. Klik op de pagina Leveranciersfactuur op OK. Indien de leveranciersfactuur geen intercompany-leveranciersfactuur was, zou het boeken lukken. Het boeken is echter mislukt omdat u met een IC-leveranciersfactuur werkt. Voor IC-handel moeten de factuurtotalen voor de IC-verkooporder gelijk zijn aan de factuurtotalen voor de bijbehorende IC-inkooporder. Om dit probleem op te lossen, moet u de netto prijs op de factuur corrigeren door de netto prijs te wijzigen in de standaardhoeveelheid 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a>Voorbeeld: Hoeveelheidvereffening bij intercompany-handel
De aantallen op de IC-inkooporder en IC-verkooporder moeten gelijk zijn. Deze vereiste vervangt eventuele van toepassing zijnde goedkeuringen voor factuurmatching. Bij dit voorbeeld worden de volgende aanvullende instellingen voor intercompany-handel gebruikt:
-   In Fabrikam Inkoop wordt het inkooporder actiebeleid voor leverancier 3024 ingesteld om de oorspronkelijke klantfactuur en de IC-leveranciersfactuur automatisch te boeken.

Bij dit voorbeeld worden de volgende aanvullende instellingen voor factuurmatching in leveranciers gebruikt voor Fabrikam Inkoop:
-   Op de pagina Artikelmodelgroepen voor de modelgroep die wordt gebruikt door artikel B-R14, is de optie Ontvangstvereisten geselecteerd.
-   De voorhanden voorraad voor artikel B-R14 is 0 (nul).

U volgt bijvoorbeeld deze stappen.
1.  Maak verkooporder SO999 voor klant 4020 in Fabrikam Purchase. De order bevat één regelartikel: 100 batterijen (artikel B-R14) met een eenheidsprijs van 1,00 per stuk. De intercompany-inkooporder ICPO333 wordt automatisch gemaakt voor leverancier 3024 in Fabrikam Inkoop, en verkooporder ICSO999 wordt automatisch gemaakt in Fabrikam Verkoop.
2.  Voer in Fabrikam Verkoop een factuurupdate uit voor ICSO999. Boeken is mislukt, omdat het artikel niet op voorraad is en nog niet is ontvangen. Daarom kan de financiële informatie kan niet worden bijgewerkt.
3.  In Fabrikam Verkoop legt u vast dat de artikelen zijn ontvangen en boekt i een pakbon voor ICSO999. De productontvangst voor ICPO333 wordt automatisch geboekt in Fabrikam Inkoop. In Fabrikam Inkoop, verandert het ontvangen aantal voor artikel B-R14 naar 100.
4.  Voer in Fabrikam Verkoop een factuurupdate uit voor ICSO999. Boeking is voltooid in beide rechtspersonen. In Fabrikam Inkoop verandert het gekochte aantal voor artikel B-R14 naar 100.






