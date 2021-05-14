---
title: Overzicht van technisch wijzigingsbeheer
description: Dit onderwerp biedt een overzicht van het beheer van technische wijzigingen, waarmee u productversies kunt plannen en beheren en productlevenscycli en technische wijzigingen kunt beheren.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947515"
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

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>De functies voor technisch wijzigingsbeheer en versiedimensiefuncties inschakelen voor uw systeem

Voordat u technisch wijzigingsbeheer gebruiken, moet u zowel de functie *Engineering Change Management* (beheer voor technische wijzigingen) als de bijbehorende configuratiesleutel inschakelen. Als u ook de versiedimensie van producten in transacties wilt bijhouden (optioneel), moet u ook de functie *Productdimensieversie* en de bijbehorende configuratiesleutel inschakelen.

Schakel eerst deze functies in door de volgende stappen uit te voeren.

1. Ga naar de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Controleer op updates.
1. Schakel de functie in met de naam **Technisch wijzigingsbeheer**.
1. Schakel ook de functie genaamd **Productdimensieversie** in als u deze wilt gebruiken.

Schakel vervolgens de configuratiesleutels in door de volgende stappen uit te voeren.

1. Plaats uw systeem in de onderhoudsmodus, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
1. Vouw het knooppunt **Handel** uit.
1. Schakel de configuratiesleutel voor de hoofdfunctie in door het selectievakje **Engineering Change Management** te selecteren. (Het is niet nodig om het knooppunt uit te vouwen, tenzij u ook een of beide subfuncties wilt uitschakelen.)
1. Als u ook de versiedimensie wilt gebruiken schakelt u het selectievakje **Productdimensie - Versie** in. (Dit selectievakje vindt u verder naar beneden in de lijst, niet genest onder het knooppunt **Engineering Change Management**.)
1. Schakel de onderhoudsmodus uit, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Vanaf april 2022 worden de licentiesleutels voor zowel **Engineering Change Management** als voor **Productdimensie - Versie** standaard ingeschakeld voor alle nieuwe installaties, maar u kunt ze zo nodig ook uitschakelen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
