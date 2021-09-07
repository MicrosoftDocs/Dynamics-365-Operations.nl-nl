---
title: Vrijgaveproces en vrijgavegeschiedenis van Planningsoptimalisatie
description: Dit onderwerp geeft informatie over het vrijgaveproces en de vrijgavegeschiedenis voor Planningsoptimalisatie.
author: crytt
ms.date: 8/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fcd18341629afcf3092a457ae711e27b0bbfeb2a
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394409"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Vrijgaveproces en vrijgavegeschiedenis van Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

Microsoft werkt de Planningsoptimalisatie maandelijks bij. Op basis van bedrijfsbehoeften geven we af en toe aanvullende updates uit tussen de geplande versies.

Elke versie wordt gepubliceerd in de afzonderlijke regio's waar Planningsoptimalisatie beschikbaar is. Dit proces duurt doorgaans drie dagen.

Tijdens het bijwerken van Planningsoptimalisatie kan de hoofdplanning iets trager verlopen dan normaal.

Omgevingen waarin Planningsoptimalisatie wordt gebruikt, ontvangen automatisch de laatste versie. Er is geen gebruikersactie vereist: de service wordt automatisch bijgewerkt. Er worden echter nooit automatisch baanbrekende nieuwe wijzigingsfuncties naar omgevingen doorgevoerd. Wijzigingen die als baanbrekend worden beschouwd, worden standaard uitgeschakeld en moeten via [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) worden ingeschakeld. Deze wijzigingen worden daarom pas in omgevingen weergegeven wanneer u ervoor kiest om deze in te schakelen.

Omdat meldingen niet worden weergegeven wanneer Planningsoptimalisatie in uw omgeving wordt bijgewerkt, kunt u de releaseopmerkingen in de volgende tabel bekijken om te bepalen wanneer de wijzigingen zijn vrijgegeven en welke functies hiermee zijn geïntroduceerd. In deze tabel ziet u de wijzigingen die zijn vrijgegeven voor Planningsoptimalisatie, of deze wijzigingen zijn gekoppeld aan een functie uit Functiebeheer en de datum van de release.

| Wijzigingen | Informatie over Functiebeheer | Datum vrijgeven |
|---|---|---|
| <p>Het veld **Doorlooptijd** toegevoegd aan geplande orders.</p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit.</p> | Functiebeheer is niet vereist. | 16 augustus 2021 |
| <p>Vereisten voor resourcetypen voor onbeperkte capaciteitsplanning toegevoegd.</p><p>Efficiëntie van resources en kalender voor onbeperkte capaciteitsplanning verbeterd.</p><p>Raadpleeg [Plannen met onbeperkte capaciteit](infinite-capacity-planning.md) voor meer informatie. | <p>Beschikbaar in Functiebeheer vanaf versie 10.0.20.</p><p>Functienaam: *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie*</p> | 6 juli 2021 |
| Algemene kwaliteitsverbeteringen. | Functiebeheer is niet vereist. | 6 juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
