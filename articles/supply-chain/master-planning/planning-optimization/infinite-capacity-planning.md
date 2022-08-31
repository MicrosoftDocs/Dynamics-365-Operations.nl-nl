---
title: Plannen met oneindige capaciteit
description: Dit artikel biedt informatie over onbeperkte capaciteitsplanning voor Planningsoptimalisatie. Het bevat ook een beschrijving van huidige functiebeperkingen.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c6e0190899abb544b559bb5f26ba974155989c3a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335310"
---
# <a name="scheduling-with-infinite-capacity"></a>Planning met onbeperkte capaciteit

[!include [banner](../../includes/banner.md)]

Met de functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* wordt planning op basis van routegegevens geïntroduceerd. Hiermee kunt u taken plannen op basis van een groot aantal route-instellingen. Bij het plannen voor Planningsoptimalisatie wordt gebruikgemaakt van vaak gehanteerde route-instellingen, waaronder de routebewerkingsvolgorde of vereisten voor bronnen voor routebewerkingen.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>De functie voor planning van onbeperkte capaciteit in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Oneindige capaciteitsplanning voor Planningsoptimalisatie* in de werkruimte [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Zie [Planning met bronselectie op basis van capaciteit](capability-based-scheduling.md) voor meer informatie over deze functie.

## <a name="added-functionality"></a>Toegevoegde functionaliteit

Met de functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* wordt taakplanning op basis van routegegevens mogelijk. Daarom kan een route-instelling worden gebruikt voor het plannen van productieprocessen. Hoewel deze functie beperkingen heeft die de ingebouwde hoofdplanning niet heeft, ondersteunt deze de meest algemene functionaliteit die is vereist voor productiescenario's.

Er wordt rekening met zowel *eenvoudige routes* als *routenetwerken*. Door het veld **Volgende** te bewerken in een routebewerking, kunt u complexe routes instellen met meerdere beginpunten en meerdere bewerkingen die parallel worden uitgevoerd. Bij het plannen wordt rekening houden met complexe routestructuren van dit type.

Daarnaast ondersteunt de functie *parallelle bewerkingen* in routes. Door de opties *Primair* en *Secundair* te gebruiken in het veld **Prioriteit** voor routebewerkingen, kunt u een routestructuur definiëren waarbij de ene routebewerking de primaire bewerking is en een andere routebewerking de secundaire. In dit geval wordt in het systeem rekening gehouden met de routestructuur tijdens het plannen.

Tijdens het planningsproces wordt ook rekening gehouden met de *resourcevereisten* die voor een bewerking zijn opgegeven. Het systeem gebruikt resourcevereisten om te bepalen welke resources vereist zijn om de bewerking uit te voeren. Momenteel ondersteunt de functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* de volgende typen resourcevereisten:

- Resourcetype
- Bron
- Resourcegroep
- Capaciteit (voor meer informatie zie [Planning met bronselectie op basis van capaciteit](capability-based-scheduling.md).)

> [!NOTE]
>
> - Als de resource en/of resourcegroep zijn ingesteld op onbeperkte capaciteit, worden ze door de hoofdplanning als onbeperkte capaciteit gezien.
> - Vereisten met betrekking tot Human Resources, zoals vaardigheden of certificaatvereisten, worden nog niet ondersteund.

De functie ondersteunt ook de operationele eigenschappen **Insteltijd** en **Uitvoeringstijd**. Wanneer u deze eigenschappen instelt voor een routebewerking, worden tijdens het planningsproces de juiste instellings- en uitvoeringstaken uitgevoerd.

In het kort ondersteunt planning voor Planningsoptimalisatie de meest gebruikte scenario's. U kunt de route maken, primaire en secundaire bewerkingen toevoegen, de volgende bewerkingen definiëren, resourcevereisten toevoegen en de insteltijd en uitvoeringstijd toevoegen. Deze informatie wordt dan tijdens het plannen door het systeem in overweging genomen.

## <a name="limitations"></a>Beperkingen

Bij het gebruik van planning voor Planningsoptimalisatie gelden de volgende beperkingen:

- De functie ondersteunt alleen onbeperkte capaciteit.
- De functie ondersteunt geen functionaliteit voor belasting van resources.
- De functie houdt geen rekening met route-uitval.
- De functie ondersteunt alleen *Duur* als selectie van de primaire resource.

De functie *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* wordt continu verbeterd. Microsoft verwacht in toekomstige versies ondersteuning te introduceren voor extra planningsinstellingen.
