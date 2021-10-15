---
title: Een intercompany-verkooporder voor een externe klant maken en factureren
description: In dit onderwerp wordt uitgelegd hoe u een intercompany-verkooporder voor een externe klant maakt en factureert
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72273a125da2e6c4a2fc16b449cd5077f3d767df
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548188"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Een intercompany-verkooporder voor een externe klant maken en factureren

[!include [banner](../../includes/banner.md)]

U kunt intercompany-handel gebruiken om de verkoop van een product van een rechtspersoon aan een andere rechtspersoon in dezelfde organisatie vast te leggen.

Wanneer u de originele verkooporder maakt, kunt u automatisch een intercompany-inkooporder maken voor de intercompany-leverancier. Een intercompany-verkooporder wordt automatisch gemaakt in de rechtspersoon van de intercompany-leverancier.

De volgende afbeelding toont de stroom van de transacties wanneer u een verkooporder maakt voor een externe klant, maar het product moet van een andere rechtspersoon in uw organisatie worden besteld voordat u het product aan de klant kunt leveren. In dit geval wordt een intercompany-inkooporder gemaakt voor de leveranciersrekening die de andere rechtspersoon vertegenwoordigt. Vervolgens wordt een intercompany-verkooporder gemaakt in de andere rechtspersoon voor de klantrekening die uw rechtspersoon vertegenwoordigt. Wanneer de factuur van een intercompany-inkooporder wordt gemaakt, wordt de factuur voor de oorspronkelijke verkooporder automatisch geboekt als er sprake is van een rechtstreekse levering.

![Extern intercompany-verkoopproces](media/intercompanyexternalsalesprocess.png)

Als u rechtstreekse levering gebruikt en u **Pakbon** selecteert in het veld **Hoeveelheid** op de pagina **Factuur wordt geboekt**, wordt de intercompany-leveranciersfactuur gebaseerd op de intercompany-productontvangstbon die eerder is geboekt.

## <a name="prerequisites"></a>Vereisten

Voordat u begint, moet u ervoor zorgen dat aan de volgende vereisten wordt voldaan om de intercompany-facturen automatisch te boeken en af te drukken.

1. Ga naar **Verkoop en marketing \> Klanten \> Alle klanten**.
1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Intercompany**.
1. Ga naar **Inkoop en sourcing \> Leveranciers \> Alle leveranciers**.
1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Intercompany**.
1. Schakel op de pagina **Intercompany** voor de leverancier of de klant in het gebied **Inkooporderbeleid** in de veldgroep **Intercompany-inkooporder (rechtstreekse levering)** het selectievakje **Factuur automatisch boeken** in.
1. Schakel in het gebied **Inkooporderbeleid** in de veldgroep **Oorspronkelijke verkooporder (rechtstreekse levering)** het selectievakje **Factuur automatisch boeken** in. Schakel dit selectievakje in als u wilt dat de factuur voor de oorspronkelijke verkooporder automatisch wordt afgedrukt tijdens het boeken van de intercompany-leveranciersfactuur.

> [!NOTE]
> De afdrukinstellingen voor de factuur worden bepaald door de instelling voor de module, het document of de transactie op de pagina **Instelling afdrukbeheer**.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Een oorspronkelijke verkooporder voor een externe klant maken

Voer deze stappen uit in rechtspersoon A. Deze procedure komt overeen met het vak met label 1 in de afbeelding.

1. Ga naar **Klanten \> Verkooporders \> Alle verkooporders**.
1. Maak op de lijstpagina **Ale verkooporders** de oorspronkelijke verkooporder. De veldwaarden worden van de klantrekening naar de verkooporder gekopieerd.
1. Selecteer in het actiepaneel op het tabblad **Verkooporder** de optie **Weergave kopteksten**.
1. Schakel op het sneltabvenster **Intercompany-instellingen** het selectievakje **Intercompany-orders automatisch maken** in.
1. Als u het artikel rechtstreeks door de intercompany-leverancier bij de externe klant wilt laten afleveren, schakelt u het selectievakje **Rechtstreekse levering** in.
1. Wanneer u klaar bent met het invoeren van de verkooporder, sluit u de pagina **Verkooporder**.

De intercompany-inkooporder wordt automatisch gemaakt voor alle artikelen die aan een intercompany-leverancier zijn toegewezen en vervolgens wordt de intercompany-verkooporder gemaakt. In een informatief bericht wordt u op de hoogte gesteld dat er een intercompany-inkooporder en een intercompany-verkooporder zijn gemaakt. Het bericht bevat ook koppelingen naar die orders. Als een artikel niet wordt gevonden, wordt er een rode waarschuwing weergegeven. Dit betekent dat het proces van het maken van een order niet is voltooid.

> [!NOTE]
> Als u verschillende orders in meerdere rechtspersonen maakt en in een van die rechtspersonen zijn de artikelen niet gevonden, worden er geen orders gemaakt, ook niet voor de rechtspersonen die de artikelen voor hun orders kunnen leveren.

## <a name="invoice-an-intercompany-sales-order"></a>Een intercompany-verkooporder facturen

Wanneer een intercompany-verkooporder wordt gefactureerd, wordt de overeenkomende intercompany-inkooporder automatisch gefactureerd. Als de oorspronkelijke verkooporder een order voor een rechtstreekse levering is, wordt de oorspronkelijke verkooporder automatisch gefactureerd.

Voer deze stappen uit in rechtspersoon B. Deze procedure komt overeen met het vak met label 2 in de afbeelding.

1. Ga naar **Klanten \> Verkooporders \> Alle verkooporders**.
1. Selecteer op de lijstpagina **Alle verkooporders** de intercompany-verkooporder.
1. Selecteer in het actievenster het tabblad **Factuur** en selecteer vervolgens **Factuur**.
1. Schakel het selectievakje **Boeking** in.
1. Selecteer de verkooporder en selecteer **OK**.

De klantfactuur voor de intercompany-verkooporder wordt automatisch geboekt in rechtspersoon B. De intercompany-leveranciersfactuur wordt vervolgens automatisch gemaakt en geboekt in rechtspersoon A. Als de oorspronkelijke verkooporder is ingesteld als een rechtstreekse levering, wordt de klantfactuur gemaakt voor de oorspronkelijke verkooporder in rechtspersoon A.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
