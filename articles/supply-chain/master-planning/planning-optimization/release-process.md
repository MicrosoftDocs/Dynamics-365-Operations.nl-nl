---
title: Vrijgaveproces en vrijgavegeschiedenis van Planningsoptimalisatie
description: Dit artikel geeft informatie over het vrijgaveproces en de vrijgavegeschiedenis voor Planningsoptimalisatie.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682555"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Vrijgaveproces en vrijgavegeschiedenis van Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

Microsoft werkt de Planningsoptimalisatie maandelijks bij. Op basis van bedrijfsbehoeften geven we af en toe aanvullende updates uit tussen de geplande versies.

Elke versie wordt gepubliceerd in de afzonderlijke regio's waar Planningsoptimalisatie beschikbaar is. Dit proces duurt doorgaans drie dagen.

Tijdens het bijwerken van Planningsoptimalisatie kan de hoofdplanning iets trager verlopen dan normaal.

Omgevingen waarin Planningsoptimalisatie wordt gebruikt, ontvangen automatisch de laatste versie. Er is geen gebruikersactie vereist: de service wordt automatisch bijgewerkt. Er worden echter nooit automatisch baanbrekende nieuwe wijzigingsfuncties naar omgevingen doorgevoerd. Wijzigingen die als baanbrekend worden beschouwd, worden standaard uitgeschakeld en moeten via [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) worden ingeschakeld. Deze wijzigingen worden daarom pas in omgevingen weergegeven wanneer u ervoor kiest om deze in te schakelen.

Omdat meldingen niet worden weergegeven wanneer Planningsoptimalisatie in uw omgeving wordt bijgewerkt, kunt u de releaseopmerkingen in de volgende tabel bekijken om te bepalen wanneer de wijzigingen zijn vrijgegeven en welke functies hiermee zijn geïntroduceerd. In deze tabel ziet u de wijzigingen die zijn vrijgegeven voor Planningsoptimalisatie, of deze wijzigingen zijn gekoppeld aan een functie uit Functiebeheer en de datum van de release.

| Wijzigingen | Informatie over Functiebeheer | Vrijgavedatum |
|---|---|---|
| <p>[Batchbeschikkingscodes](../../inventory/batch-disposition-codes.md)</p><p>Parameters voor voorhanden voorraad en voorraadtransacties opnemen in hoofdplannen</p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit</p> | Functiebeheer is niet vereist | 10-14 oktober 2022 |
| <p>[Resourceplanning met eindige capaciteit](finite-capacity.md)</p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit</p> | Functiebeheer is niet vereist | 19-23 september 2022 |
| Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit | Functiebeheer is niet vereist | 29 augustus - 3 september 2022 |
| <p>[Gecentraliseerd onderhoud van kalenders](../supply-chain-calendars-master-planning.md)</p><p>[Suggesties om bestaande voorraad te optimaliseren](../action-messages.md)</p><p>[Ondersteuning voor uitbesteding](../../production-control/manage-subcontract-work-production.md)</p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit</p> | Functiebeheer is niet vereist | 7-11 maart 2022 |
| Planningsprioriteitsondersteuning voor productieorders | Beschikbaar in versie 10.0.25 als onderdeel van de functie met de naam *Prioriteitsgestuurde MRP-ondersteuning voor planningsoptimalisatie*. | 12-18 november 2021 |
| Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit | Functiebeheer is niet vereist | 12-18 november 2021 |
| <p>Ondersteuning voor formules voor de berekening van procestijd, productieroute met overlapping en productiebewerkingsnummer van behoeftetransacties</p><p>Verbeterde foutberichten voor productieplanning met betrekking tot time-out, capaciteit kan niet worden gevonden en cyclische route</p><p>Verbeterde consistentie bij het berekenen van ontvangst- en uitgiftedatums op zowel geplande orders als gefiatteerde orders</p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit</p> | Functienaam: *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* | 22-27 oktober 2021 |
| <p>Ondersteuning voor het overwegen van uitvalpercentage bij de berekening van de verwerkingstijd</p><p>Ondersteuning voor bewerkingsnummer en materiaalverbruik tijdens de planning</p> | Functienaam: *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* | 5-7 oktober 2021 |
| <p>Ondersteuning voor taaktypen voor productieroute: **Wachtrij vóór**, **Wachtrij na** en **Transporttijd**</p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit</p> | Functienaam: *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* | 25-30 september 2021 |
| <p>Ondersteuning voor hoofdplannen waarbij **Planningsmethode** is ingesteld op *Bewerkingsplanning*</p><p>Houd op de pagina **Routegroepen** rekening met de instellingen voor de selectievakjes **Activering**, **Werktijd** en **Capaciteit** voor rijen met een **Type route/taak** van *Instellingen* of *Proces* </p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit</p> | <p>Bewerkingsplanning is beschikbaar in Functiebeheer vanaf versie 10.0.20</p><p>Functienaam: *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie*</p> | 9-17 september 2021 |
| Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit | Functiebeheer is niet vereist | 25 - 30 augustus 2021 |
| <p>Het veld **Doorlooptijd** toegevoegd aan geplande orders.</p><p>Verbeteringen in de algemene prestaties, kwaliteit en stabiliteit.</p> | Functiebeheer is niet vereist | 12 - 17 augustus 2021 |
| <p>Vereisten voor resourcetypen voor onbeperkte capaciteitsplanning toegevoegd</p><p>Efficiëntie van resources en kalender voor onbeperkte capaciteitsplanning verbeterd</p><p>Raadpleeg [Plannen met onbeperkte capaciteit](infinite-capacity-planning.md) voor meer informatie</p> | <p>Beschikbaar in Functiebeheer vanaf versie 10.0.20</p><p>Functienaam: *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie*</p> | 6 - 12 juli 2021 |
| Algemene kwaliteitsverbeteringen | Functiebeheer is niet vereist | 6 - 12 juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
