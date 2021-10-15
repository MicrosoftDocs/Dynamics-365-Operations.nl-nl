---
title: Overzicht van technisch wijzigingsbeheer
description: Dit onderwerp biedt een overzicht van het beheer van technische wijzigingen, waarmee u productversies kunt plannen en beheren en productlevenscycli en technische wijzigingen kunt beheren.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 89a3eb584275e52910726ca5a9ed53f744f10b8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574684"
---
# <a name="engineering-change-management-overview"></a>Overzicht van technisch wijzigingsbeheer

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Functieoverzicht

De hedendaagse fabrikanten vereisen een krachtig productgegevensbeheer, versiebeheer en beheer van technische wijzigingen om in een wereld van constant kortere levenscycli van producten, verhoogde kwaliteit en betrouwbaarheid en toegenomen nadruk op productveiligheid te slagen.

Technisch wijzigingsbeheer brengt structuur en discipline in productgegevensbeheer en maakt het mogelijk dat producten kunnen worden gedefinieerd, vrijgegeven en gereviseerd op een gereguleerde manier die door werkstromen wordt ondersteund. Door middel van productversies en het beheer van technische veranderingen kunt u technische wijzigingen documenteren, de impact ervan beoordelen en toepassen gedurende de gehele levenscyclus van een product.

Het beheer van technische wijzigingen helpt u productversies te plannen en beheren en productlevenscycli en technische wijzigingen te beheren. Hier volgt een lijst met de belangrijkste kenmerken ervan:

- Versiebeheer voor producten
- Verbeterde functies voor productvrijgave waarmee u productmodelgegevens in één rechtspersoon (het technisch bedrijf) kunt onderhouden en het volledig geconfigureerde vrijgegeven product kunt publiceren naar andere rechtspersonen
- Regels voor het valideren of vereiste informatie is ingevoerd voordat een productversie wordt geactiveerd (gereedheidscontroles)
- Verbeterd beheer van de productlevenscyclus door middel van nauwkeurig beheer over wanneer een vrijgegeven product kan worden gebruikt in specifieke bedrijfsprocessen
- Aanvragen voor technische wijzigingen die worden ondersteund door werkstromen
- Orders voor technische wijzigingen die worden ondersteund door werkstromen

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

De voorgaande video ([Mogelijkheden voor wijzigingsbeheer in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is opgenomen in de [Finance and Operations speellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) beschikbaar op YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>De functies voor het beheer van technische wijzigingen voor uw systeem inschakelen

Voordat u het beheer van technische wijzigingen kunt gebruiken, moet u zowel de functie *Engineering Change Management* (beheer voor technische wijzigingen) als de bijbehorende configuratiesleutel inschakelen. Als u ook de versiedimensie van producten in transacties wilt bijhouden (optioneel), moet u ook de functie *Productdimensieversie* en de bijbehorende configuratiesleutel inschakelen. Wanneer die vereiste opties zijn ingesteld, kunt u aanvullende optionele functies voor het beheer van technische wijzigingen inschakelen.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>De basisfuncties voor het beheer van technische wijzigingen inschakelen

Schakel eerst deze functies in door de volgende stappen uit te voeren.

1. Ga naar de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Controleer op updates.
1. Schakel de functie in met de naam *Technisch wijzigingsbeheer*.
1. Schakel ook de functie genaamd *Productdimensieversie* in als u deze wilt gebruiken.

### <a name="turn-on-the-required-configuration-keys"></a>De vereiste configuratiesleutels inschakelen

Schakel vervolgens de configuratiesleutels in door de volgende stappen uit te voeren.

1. Plaats uw systeem in de onderhoudsmodus, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
1. Vouw het knooppunt **Handel** uit.
1. Schakel de configuratiesleutel voor de hoofdfunctie in door het selectievakje **Technisch wijzigingsbeheer** in te schakelen.
1. Vouw het knooppunt **Technisch wijzigingsbeheer** uit en schakel waar nodig de volgende selectievakjes in of uit (afhankelijk van de functies die u wilt gebruiken):

    - **Kenmerk zoeken**: schakel dit selectievakje in om de [functie voor het zoeken naar kenmerken](engineering-attributes-and-search.md) in te schakelen. U wordt aangeraden deze functie in te schakelen, maar u kunt dit selectievakje uitschakelen als u het niet wilt gebruiken.
    - **Wijzigingsbeheer voor procesproductie**: schakel dit selectievakje in als u de functies voor technisch wijzigingsbeheer wilt gebruiken om wijzigingen in formules voor procesproductie te beheren. Als u geen formules hoeft te beheren, kunt u dit selectievakje uitschakelen. Zie [Wijzigingen in formules en de ingrediënten ervan beheren](manage-formula-changes.md) voor meer informatie.

1. Als u ook de versiedimensie wilt gebruiken schakelt u het selectievakje **Productdimensie - versie** in. (Dit selectievakje vindt u verder naar beneden in de lijst, niet genest onder het knooppunt **Technisch wijzigingsbeheer**.)
1. Schakel de onderhoudsmodus uit, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Vanaf april 2022 worden de licentiesleutels voor zowel **Engineering Change Management** als voor **Productdimensie - Versie** standaard ingeschakeld voor alle nieuwe installaties, maar u kunt ze zo nodig ook uitschakelen.

### <a name="turn-on-additional-engineering-change-management-features"></a>De basisfuncties voor het beheer van technische wijzigingen inschakelen

Wanneer u de basisfuncties voor het beheer van technische wijzigingen hebt ingeschakeld en de bijbehorende configuratiesleutels hebt inschakelt, worden er een aantal extra en optionele functies voor het beheer van technische wijzigingen aan Functiebeheer toegevoegd. Elk van deze functies wordt weergegeven onder de module **Beheer van technische wijzigingen**. In de volgende tabel wordt elke optionele functie beschreven en worden koppelingen weergegeven voor meer informatie.

| Functienaam in Functiebeheer | Beschrijving |
|---|---|
| Wijzigingsbeheer voor bestaande producten inschakelen | <p>Met deze functie kunt u bestaande producten converteren naar technische producten, zodat u ze kunt beheren via het beheer van technische wijzigingen.</p><p>Zie [Beheer van wijzigingen voor bestaande producten inschakelen](change-management-existing-products.md) voor meer informatie.</p> |
| Technische meldingen voor productie | <p>Wanneer een product technisch wordt gewijzigd, is het mogelijk belangrijk om de productie op de hoogte te brengen van die wijzigingen. Op die manier kunnen productiemedewerkers de juiste actie ondernemen, zoals de vervanging van onderdelen, van de stuklijst of van de route. Met deze functie kunt u de productieafdeling op de hoogte brengen van wijzigingen aan producten die worden geproduceerd.</p><p>Zie [Wijzigingen in technische producten beheren](engineering-change-management.md) voor meer informatie.</p> |
| Verbeterde overname van kenmerken voor Beheer voor technische wijzigingen | <p>Met deze functie kunnen kenmerken voor eindproducten of halffabricaten eenvoudiger worden beheerd. Wanneer deze functie is ingeschakeld, kunt u eenvoudiger alle kenmerken van een artikel identificeren en de kenmerken selecteren die moeten worden doorgegeven van dat artikel naar het hoofdartikel. Deze functie is handig wanneer bijvoorbeeld één onderdeel van een voltooid artikel breekbaar, giftig of ontvlambaar is, omdat u gemakkelijk de kenmerken breekbaar, giftig of ontvlambaar kunt identificeren en deze kunt doorvoeren naar het eindproduct.</p><p>Zie [Technische kenmerken en zoeken naar technische kenmerken](engineering-attributes-and-search.md) voor meer informatie.</p> |
| Controles op productgereedheid | <p>Met deze functie kunt u gereedheidscontroles instellen voor standaardproducten (niet-technisch). Gebruik controles voor productgereedheid om ervoor te zorgen dat elk product volledig is gedefinieerd en alle vereiste beleidsregels zijn geconfigureerd voordat het product beschikbaar wordt gemaakt en in transacties wordt gebruikt. Als u deze functie uitschakelt nadat u deze een tijdlang hebt gebruikt, worden alle bestaande controles op gereedheid voor standaardproducten verwijderd.</p><p>Zie voor meer informatie [Productgereedheid](product-readiness.md).</p> |
| Wijzigingen in formules en hun ingrediënten beheren | <p>Met deze functie kunt u wijzigingen in formulebestanddelen, coproducten en bijproducten bijhouden.</p><p>Zie [Wijzigingen in formules en de bestanddelen ervan beheren](manage-formula-changes.md) voor meer informatie.</p> |
| Varianten genereren voor technische producten | <p>Met deze functie kunt u varianten voor technische producten genereren op basis van beschikbare dimensiewaarden.</p><p>Zie [Varianten voor technische producten genereren](engineering-variants.md) voor meer informatie.</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
