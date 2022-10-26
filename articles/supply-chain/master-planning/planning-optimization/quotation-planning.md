---
title: Plannen op basis van offertes en offerteaanvragen
description: In dit artikel wordt beschreven hoe u de hoofdplanning instelt om rekening te houden met offertes en offerteaanvragen wanneer geplande orders worden gegenereerd.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690079"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Plannen op basis van offertes en offerteaanvragen

[!include [banner](../../includes/banner.md)]

Offertes en offerteaanvragen vertegenwoordigen mogelijke of zelfs waarschijnlijke toekomstige orders. Het is daarom verstandig om er rekening mee te houden tijdens de hoofdplanning, zodat extra aanbod kan worden gepland op basis van bestaande offerteaanvragen en de kans dat een offerte een werkelijke order wordt. In dit artikel wordt beschreven hoe u de hoofdplanning instelt om rekening te houden met offertes en offerteaanvragen wanneer geplande orders worden gegenereerd.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Hoofdplanning instellen om rekening te houden met verkoopoffertes en/of offerteaanvragen

Met de volgende procedure kunt u de hoofdplanning instellen om rekening te houden met verkoopoffertes en/of offerteaanvragen.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een bestaand plan in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuw plan te maken.
1. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Verkoopoffertes opnemen**: stel deze optie in op *Ja* als u rekening wilt houden met verkoopoffertes wanneer het huidige plan wordt uitgevoerd. Stel *Nee* in als u deze wilt negeren.
    - **Waarschijnlijkheidspercentage**: stel het minimale vertrouwensniveau in dat nodig is om een offerte in de hoofdplanning op te nemen. De berekening van de hoofdplanning bevat alle offertes die zijn gemaakt op basis van verkoopkansen die dit waarschijnlijkheidspercentage of hoger hebben. Stel dit veld in op *0* (nul) als u alle offertes wilt opnemen, inclusief offertes waaraan geen waarschijnlijkheid of verkoopkans is gekoppeld. Zie het volgende gedeelte voor meer informatie over waarschijnlijkheden voor offertes.
    - **Offerteaanvragen opnemen**: stel deze optie in op *Ja* als u rekening wilt houden met offerteaanvragen wanneer het huidige plan wordt uitgevoerd. Stel *Nee* in als u deze wilt negeren. Als u ervoor kiest om offerteaanvragen te overwegen, worden er geplande inkooporders voor gemaakt, maar wordt de leverancier pas opgegeven als de offerteaanvraag is omgezet. Geplande inkooporders die voor de offerteaanvragen worden gemaakt, kunnen van invloed zijn op de hoeveelheden van andere geplande orders.

1. Ga op de gebruikelijke wijze door met het instellen van het hoofdplan.

## <a name="assign-and-view-probabilities-for-quotations"></a>Waarschijnlijkheden voor offertes toewijzen en weergeven

Zoals aangegeven in de vorige sectie wordt bij een hoofdplan alleen rekening met offertes gemaakt die voldoen aan of hoger zijn dan de waarschijnlijkheidsdrempel die voor het plan is gedefinieerd (als er een drempel is gedefinieerd). De waarschijnlijkheid wordt echter niet rechtstreeks in elke offerte ingesteld. In plaats daarvan wordt deze overgenomen van de verkoopkans die is gebruikt om de offerte te genereren. Daarom wordt aan offertes (of aan de bijbehorende verkoopkans) die rechtstreeks op de pagina **Alle offertes** worden gemaakt, geen waarschijnlijkheid toegewezen en wordt er nooit rekening mee gehouden in de hoofdplanning (tenzij het veld **Waarschijnlijkheidspercentage** is ingesteld op *0*\[nul\]). Om een waarschijnlijkheid toegewezen te krijgen, moet een offerte worden gegenereerd op basis van een kans.

### <a name="create-a-quotation-from-an-opportunity"></a>Een offerte op basis van een verkoopkans maken

Met de volgende procedure kunt u een waarschijnlijkheid toewijzen aan een verkoopkans en vervolgens een offerte maken op basis van die kans.

1. Ga naar **Verkoop en marketing \> Relaties \> Verkoopkansen \> Alle verkoopkansen**.
1. Selecteer een bestaande verkoopkans of de optie **Nieuw** in het actievenster om een nieuwe verkoopkans te maken.
1. Vul de pagina Verkoopkans in om de beste verkoopkans te identificeren. Stel het veld **Waarschijnlijkheid** in op de juiste waarde. Alleen voor hoofdplannen die zijn ingesteld op het zoeken naar waarschijnlijkheden van deze waarde of hoger wordt rekening gehouden met offertes die op basis van deze verkoopkans worden gegenereerd.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster op het tabblad **Verkoopkans** in de groep **Nieuw** de optie **Verkoopofferte** of **Projectofferte**, afhankelijk van het type offerte dat u wilt maken.
1. Stel in het dialoogvenster **Offerte maken** de velden naar wens in en selecteer **OK**.
1. Een nieuwe offerte wordt gemaakt en geopend. Gebruik op het sneltabblad **Regels** de werkbalk om naar wens verkoop- of projectregels toe te voegen om de inhoud van de offerte te definiëren.
1. Selecteer **Opslaan** in het actievenster. Sluit de offerte vervolgens.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>De waarschijnlijkheid weergeven die aan een offerte is toegewezen

De enige manier om de waarschijnlijkheid weer te geven die aan een offerte is toegewezen, is door de verkoopkans te openen waarmee de offerte is gemaakt, zoals wordt beschreven in de volgende procedure

1. Ga naar **Verkoop en marketing \> Verkoopoffertes \> Alle offertes**.
1. Als de kolom **Verkoopkans-id** niet wordt weergegeven (deze is verborgen in een standaardinstallatie), volgt u deze stappen om de verkoopkans tijdelijk weer te geven. (Als u de kolom **Verkoopkans-id** beschikbaar wilt houden, maakt u een [opgeslagen weergave](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) waarin deze is opgenomen.)

    1. Selecteer de kolom en houd deze vast (of klik met de rechtermuisknop) in het raster en selecteer **Kolommen invoegen**.
    1. Zoek in het dialoogvenster **Kolommen invoegen** de rij waarin het veld **Veld** is ingesteld op *Verkoopkans* en schakel het selectievakje **Selecteren** voor die rij in.
    1. Selecteer **Bijwerken** om de geselecteerde kolom toe te voegen aan de pagina **Alle offertes**.

1. Zoek in het raster de rij voor de relevante offerte. Selecteer vervolgens de waarde voor die rij in de kolom **Verkoopkans-id**.

    > [!NOTE]
    > Als u naar een projectofferte zoekt, moet u mogelijk de kolomkop **Offertetype** selecteren en het filter verwijderen. In een standaardinstallatie wordt dit filter zo ingesteld dat alleen verkoopoffertes worden weergegeven.

1. De bijbehorende verkoopkans wordt geopend. U kunt nu de waarde voor **Waarschijnlijkheid** nu weergeven en bewerken.
