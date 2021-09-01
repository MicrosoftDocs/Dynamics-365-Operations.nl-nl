---
title: Planning met onbeperkte capaciteit
description: Dit onderwerp biedt informatie over onbeperkte capaciteitsplanning voor Planningsoptimalisatie. Het bevat ook een beschrijving van huidige functiebeperkingen.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc40dc2bcf1969e4c566b624a9425638e69ab2a17892f035aeabb74068aadd14
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718967"
---
# <a name="scheduling-with-infinite-capacity"></a>Planning met onbeperkte capaciteit

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Met de functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* wordt planning op basis van routegegevens geïntroduceerd. Hiermee kunt u taken plannen op basis van een groot aantal route-instellingen. Bij het plannen voor Planningsoptimalisatie wordt gebruikgemaakt van vaak gehanteerde route-instellingen, waaronder de routebewerkingsvolgorde of vereisten voor bronnen voor routebewerkingen.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>De functie voor planning van onbeperkte capaciteit inschakelen

Als uw systeem nog niet is uitgerust met de functie die in dit onderwerp wordt beschreven, opent u het werkgebied [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* in.

## <a name="added-functionality"></a>Toegevoegde functionaliteit

Met de functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* wordt taakplanning op basis van routegegevens mogelijk. Daarom kan een route-instelling worden gebruikt voor het plannen van productieprocessen. Hoewel deze functie beperkingen heeft die de ingebouwde hoofdplanning niet heeft, ondersteunt deze de meest algemene functionaliteit die is vereist voor productiescenario's.

Er wordt rekening met zowel *eenvoudige routes* als *routenetwerken*. Door het veld **Volgende** te bewerken in een routebewerking, kunt u complexe routes instellen met meerdere beginpunten en meerdere bewerkingen die parallel worden uitgevoerd. Bij het plannen wordt rekening houden met complexe routestructuren van dit type.

Daarnaast ondersteunt de functie *parallelle bewerkingen* in routes. Door de opties *Primair* en *Secundair* te gebruiken in het veld **Prioriteit** voor routebewerkingen, kunt u een routestructuur definiëren waarbij de ene routebewerking de primaire bewerking is en een andere routebewerking de secundaire. In dit geval wordt in het systeem rekening gehouden met de routestructuur tijdens het plannen.

Tijdens het planningsproces wordt ook rekening gehouden met de *resourcevereisten* die voor een bewerking zijn opgegeven. Het systeem gebruikt resourcevereisten om te bepalen welke resources vereist zijn om de bewerking uit te voeren. Momenteel ondersteunt de functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* de volgende typen resourcevereisten:

- Resourcetype
- Bron
- Resourcegroep
- Mogelijkheid

> [!NOTE]
> Vereisten met betrekking tot Human Resources, zoals vaardigheden of certificaatvereisten, worden nog niet ondersteund.

De functie ondersteunt ook de operationele eigenschappen **Insteltijd** en **Uitvoeringstijd**. Wanneer u deze eigenschappen instelt voor een routebewerking, worden tijdens het planningsproces de juiste instellings- en uitvoeringstaken uitgevoerd.

In het kort ondersteunt planning voor Planningsoptimalisatie de meest gebruikte scenario's. U kunt de route maken, primaire en secundaire bewerkingen toevoegen, de volgende bewerkingen definiëren, resourcevereisten toevoegen en de insteltijd en uitvoeringstijd toevoegen. Deze informatie wordt dan tijdens het plannen door het systeem in overweging genomen.

## <a name="limitations"></a>Beperkingen

Bij het gebruik van planning voor Planningsoptimalisatie gelden de volgende beperkingen:

- De functie ondersteunt alleen taakplanning. Instellingen die betrekking hebben op bewerkingsplanning worden tijdens de planning niet in aanmerking genomen, ongeacht de planningsmethode in hoofdplannen.
- De functie ondersteunt alleen onbeperkte capaciteit.
- De functie ondersteunt geen functionaliteit voor belasting van resources.
- De functie houdt geen rekening met route-uitval.
- De functie ondersteunt alleen *Duur* als selectie van de primaire resource.

De functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* wordt continu verbeterd. Microsoft verwacht in toekomstige versies ondersteuning te introduceren voor extra planningsinstellingen.
