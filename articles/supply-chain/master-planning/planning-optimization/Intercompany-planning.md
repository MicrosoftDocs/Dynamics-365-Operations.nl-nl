---
title: Intercompany-planning
description: In dit onderwerp wordt intercompany-planning beschreven en wordt uitgelegd hoe u intercompany-planning configureert met Planningsoptimalisatie in Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0958ebccba345aa13a95f1fdf03946546cbbb714
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983589"
---
# <a name="intercompany-planning"></a>Intercompany-planning

[!include [banner](../../includes/banner.md)]

Voor sommige organisaties zijn logistieke activiteiten afhankelijk van andere rechtspersonen (bedrijven) in de organisatie. Deze activiteiten worden verwerkt met behulp van intercompany-verkopen en -inkopen, omdat elke rechtspersoon een afzonderlijk rekeningschema heeft.

In dit onderwerp wordt intercompany-planning beschreven en wordt uitgelegd hoe u intercompany-planning configureert met Planningsoptimalisatie in Microsoft Dynamics 365 Supply Chain Management.

In dit onderwerp worden de volgende belangrijke intercompany-termen gebruikt:

- **Upstream**: een relatieve verwijzing in een bedrijf of toeleveringsketen. Het duidt verplaatsing in de richting van de leverancier van grondstoffen aan.
- **Downstream**: een relatieve verwijzing in een bedrijf of toeleveringsketen. Het duidt verplaatsing in de richting van de klant aan.
- **Geplande intercompany-vraag**: geplande vraag naar een product in een bedrijf, op basis van de geplande vraag naar het product van een downstream-bedrijf.

In de hoofdplanning kan een plan in het ene bedrijf geplande intercompany-vraag bevatten die is gerelateerd aan geplande orders uit een plan in een ander bedrijf. Deze mogelijkheid is nuttig omdat de geplande orders in alle bedrijven volledig zichtbaar zijn. Het zorgt er ook voor dat alle verplichte geplande aanbodorders worden gemaakt, maar zonder dat geplande orders hoeven te worden gefiatteerd voor de intercompany-vraag.

Als u hoofdplanning uitvoert vanuit een hoofdplan dat geplande downstreamvraag omvat, worden geplande inkooporders van de gerelateerde intercompany-leveranciers in het plan opgenomen als vraag.

## <a name="required-setup"></a>Vereiste instellingen

Als u intercompany-planning wilt gebruiken, moet u het systeem op de volgende manier voorbereiden:

1. De relevante producten moeten in alle betrokken bedrijven worden vrijgegeven. Zie voor meer informatie [Intercompany-handel configureren en gebruiken in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) op Microsoft Learn.
1. Downstreamvraag moet worden gedekt door inkopen van een leverancier die een intercompany-relatie heeft met het upstreambedrijf en relevante standaardvoorraaddimensies (locatie en magazijn) voor de klant. Zie voor meer informatie [Intercompany-handel configureren en gebruiken in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) op Microsoft Learn.
1. Het hoofdplan in het upstream-bedrijf moet geplande downstreamvraag bevatten en het relevante bedrijf en hoofdplan moeten worden opgegeven in de downstreamplannen.

## <a name="include-planned-downstream-demand"></a>Geplande downstream vraag opnemen

Voer de volgende stappen uit om uw hoofdplan zo te configureren dat het geplande downstreamvraag bevat.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer of maak een hoofdplan.
1. Stel op het sneltabblad **Intercompany-planning** de volgende velden in:

    - **Geplande downstreamvraag opnemen**: stel deze optie in op *Ja* om intercompany-planning in te schakelen voor het hoofdplan.
    - **Downstreamplannen**: als u de optie **Geplande downstreamvraag opnemen** instelt op *Ja*, gebruikt u de werkbalk en het raster om de gewenste hoofdplannen van andere bedrijven toe te voegen.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>De behoefte tussen bedrijven traceren met de optie voor tracering van de behoefte op meerdere niveaus

Bij tracering van de behoefte op meerdere niveaus kunt u de behoefte tussen bedrijven bekijken om de eerste bron van de vraag te bekijken die wordt gedekt door een aanbod.

Voer de volgende stappen uit om informatie over tracering van de behoefte op meerdere niveaus weer te geven.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Geplande orders**.
1. Selecteer of open een geplande verkooporder.
1. Selecteer in het actievenster op het tabblad **Weergeven** in de groep **Vereisten** de optie **Tracering van de behoefte op meer niveaus**.

### <a name="intercompany-example-that-involves-two-companies"></a>Intercompany-voorbeeld met twee bedrijven

Voor dit voorbeeld wordt een geplande productieorder gemaakt in het bedrijf USMF om een verkooporder in het bedrijf DEMF te dekken. In USMF is de directe vraag geplande intercompany-vraag. Om deze vraag weer te geven in USMF, wordt hoofdplanning eerst uitgevoerd in DEMF en vervolgens in USMF.

In de volgende afbeelding ziet u hoe dit voorbeeld op de pagina **Tracering van de behoefte op meer niveaus** kan worden weergegeven voor de geplande productieorder.

![Intercompany-voorbeeld met twee bedrijven](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Intercompany-voorbeeld met drie bedrijven

Voor dit voorbeeld wordt een geplande inkooporder gemaakt in het bedrijf USMF om een verkooporder in het bedrijf FRRT te dekken. In de bedrijven DEMF en USMF is de directe vraag geplande intercompany-vraag. Om deze vraag weer te geven in USMF, wordt hoofdplanning eerst uitgevoerd in FRRT, vervolgens in DEMF en tot slot in USMF.

In de volgende afbeelding ziet u hoe dit voorbeeld op de pagina **Tracering van de behoefte op meer niveaus** kan worden weergegeven voor de geplande productieorder.

![Intercompany-voorbeeld met drie bedrijven](media/IntercompanyPlanning2.png)
