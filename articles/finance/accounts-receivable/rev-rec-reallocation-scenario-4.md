---
title: Hertoewijzing van opbrengsttoerekening - Scenario 4
description: In dit onderwerp wordt een hertoewijzingsscenario besproken waarin een regel wordt verwijderd uit een bestaande, gedeeltelijk gefactureerde verkooporder. In dit scenario wordt hetzelfde resultaat geproduceerd, ongeacht of de regel uit de verkooporder wordt verwijderd of wordt ingesteld op de status Geannuleerd.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 50a2d0d2ca28d9b62713502700f2c4bd2e42751e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238299"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Hertoewijzing van opbrengsttoerekening - Scenario 4

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een hertoewijzingsscenario besproken waarin een regel wordt verwijderd uit een bestaande, gedeeltelijk gefactureerde verkooporder. In dit scenario wordt hetzelfde resultaat geproduceerd, ongeacht of de regel uit de verkooporder wordt verwijderd of wordt ingesteld op de status Geannuleerd.

Voor dit scenario is de optie **Factuurcorrecties boeken naar Klanten** ingesteld op **Nee** op het tabblad **Opbrengsttoerekening** van de pagina **Grootboekparameters** (**Opbrengsttoerekening \> Instellen \> Grootboekparameters**).

[![De optie Factuurcorrecties boeken naar Klanten is ingesteld op Nee](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Er wordt een verkooporder gemaakt voor de klant US\_SI\_0003. De klant koopt een laptop (artikelnummer S0012), installatieservices (artikelnummer S0001) en een ondersteuningsplan voor de laptop (artikelnummer S0008, Doorlopende technische service). De opbrengst voor de laptop en installatieservices wordt onmiddellijk toegerekend. De opbrengst voor het ondersteuningsplan wordt uitgesteld en over 12 maanden toegerekend, zoals gedefinieerd door het datumbereik in het contract.

[![Verkooporderregels voor de laptop, installatieservices en het ondersteuningsplan](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

De verkooporder wordt bevestigd. Aangezien voor alle drie de artikelen toewijzing van de opbrengstprijs is ingesteld, wordt de opbrengstprijs berekend wanneer de verkooporder wordt bevestigd. U kunt de toegekende opbrengst weergeven op de pagina **Opbrengstprijstoewijzing** (selecteer **Opbrengstprijstoewijzing** op de pagina **Verkooporder** in het actievenster op het tabblad **Beheren** in de groep **Opbrengsttoerekening**). De opbrengst voor de laptop wordt als bedrag van $ 995,84 naar de opbrengstrekening geboekt. De opbrengst voor de installatieservices wordt als bedrag van $ 314,47 naar de opbrengstrekening geboekt. De opbrengst voor het ondersteuningsplan wordt als bedrag van $ 188,69 naar een rekening voor uitgestelde opbrengst geboekt. Het totaal van de opbrengstprijzen moet gelijk zijn aan het totaal van de regels die zijn ingesteld om de opbrengstprijstoewijzing vast te leggen ($ 1499,00).

[![De pagina Opbrengstprijstoewijzing](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

De klant wordt gefactureerd voor de laptop en het ondersteuningsplan, maar niet voor de installatieservices. In de volgende afbeelding wordt de journaalregel weergegeven die voor de factuur is geboekt.

[![journaalregel voor de gefactureerde verkooporder](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Met de journaalregel wordt $ 1276,94 naar Klanten geboekt. Omdat deze factuur een gedeeltelijke factuur is, komt de opbrengst of uitgestelde opbrengst plus btw niet overeen met het bedrag in Klanten. Het verschil van $ 14,47 wordt geboekt naar de vereffeningsrekening voor gedeeltelijke factuuropbrengst.

Het schema voor opbrengsttoerekening wordt ook gemaakt.

[![De pagina Opbrengsttoerekeningsschema voor de gedeeltelijke factuur](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Later besluit de klant om geen installatieservices aan te schaffen. Daarom wordt deze regel uit de verkooporder verwijderd. De verkooporder kan niet opnieuw worden bevestigd omdat alleen gefactureerde regels in de verkooporder blijven staan.

[![Verkooporder nadat de regel voor installatieservices is verwijderd](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Hoewel de verkooporder niet kan worden bevestigd, kan deze wel opnieuw worden toegewezen. Selecteer in de verkooporder de optie **Prijs opnieuw toewijzen met nieuwe orderregels** om de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** te openen. Selecteer de twee overgebleven verkooporderregels en selecteer vervolgens **Hertoewijzing bijwerken**. In de kolom **Opnieuw toegewezen bedrag** wordt de nieuwe opbrengstprijs voor de overgebleven verkooporderregels weergegeven.

[![Nieuwe opbrengstprijzen op de pagina Prijs opnieuw toewijzen met nieuwe orderregels](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Selecteer vervolgens **Verwacht boekstuk** om de journaalregels weer te geven.

[![Journaalregels op de pagina Verwacht boekstuk](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

Op de pagina **Verwacht boekstuk** wordt in de laatste vijf regels de oorspronkelijke journaalregel uit de geboekte factuur teruggeboekt. De eerste vier regels zijn de nieuwe journaalregels die zijn geboekt voor de factuur. Het is belangrijk dat u begrijpt dat er geen nieuwe factuur wordt weergegeven voor de klant. Na de hertoewijzing moet de klant nog steeds $ 1276,94 betalen. Dit is het bedrag dat in de nieuwe journaalregel naar Klanten moet worden geboekt. De nieuwe opbrengst of uitgestelde opbrengst plus btw is $ 1276,94. U hoeft dus niet te boeken naar de vereffeningsrekening voor gedeeltelijke factuuropbrengst.

Selecteer **Verwerken** om de hertoewijzing te voltooien. Er wordt een boekingsdatum ingevoerd. Nadat de hertoewijzing is voltooid, wordt op de pagina **Opbrengstprijstoewijzing** de prijshertoewijzing voor de twee overgebleven artikelen weergegeven.

[![Prijshertoewijzing voor de overgebleven artikelen op de pagina Opbrengstprijstoewijzing](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Het schema voor opbrengsttoerekening is bijgewerkt op basis van de nieuwe prijs van opbrengsthertoewijzing. Open de pagina **Opbrengstherkenningsschema** vanuit de verkooporder. Eerder waren er 13 regels voor artikel S0008 (een schema van twaalf maanden is toegewezen aan dit artikel). Er zijn nu 39 regels: de 13 oorspronkelijke schemaregels, 13 schemaregels voor terugboeking en 13 regels die zijn gebaseerd op de nieuwe opbrengstprijs.

[![Bijgewerkte pagina Opbrengsttoerekeningsschema met 39 regels voor artikel S0008](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Wanneer u **Boekstuk** selecteert, wordt in het factuurjournaal de oorspronkelijke journaalregel weergegeven. Als u de stornopost en de nieuwe journaalregel uit de verkooporder wilt weergeven, selecteert u **Opbrengstcorrecties** in het actievenster en vervolgens **Boekstuk**.

Open de pagina **Alle klanten** (**Klanten \> Klanten \> Alle klanten**), selecteer de klant **US\_SI\_0003** en selecteer **Transacties**. Op de pagina **Klanttransacties** wordt alleen de oorspronkelijke factuur (000008) weergegeven, samen met de oorspronkelijke journaalregel. Omdat de optie **Factuurcorrecties boeken naar Klanten** is ingesteld op **Nee** op de pagina **Grootboekparameters**, wordt alleen Grootboek bijgewerkt. Daarom worden de stornoposten en bijgewerkte boekhoudingsposten niet weergegeven. De opbrengstcorrectietransacties die zijn gemaakt in [scenario 3](rev-rec-reallocation-scenario-3.md) worden wel weergegeven.

[![Oorspronkelijke journaalregel op de pagina Klanttransacties](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]