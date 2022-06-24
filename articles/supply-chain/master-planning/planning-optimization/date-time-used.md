---
title: Parameters voor datum en tijd die door Planningsoptimalisatie worden gebruikt
description: Dit artikel biedt informatie over de parameters voor datum en tijd die tijdens de bewerking door Planningsoptimalisatie worden gebruikt .
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 807834bf5cd062ed24e5e3f3512d8389717a2d39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885894"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Parameters voor datum en tijd die door Planningsoptimalisatie worden gebruikt

[!include [banner](../../includes/banner.md)]

Dit artikel biedt informatie over de parameters voor datum en tijd die tijdens de bewerking door Planningsoptimalisatie worden gebruikt .

Terwijl in de ingebouwde hoofdplanningsengine transactiedatums in alle berekeningen gebruikt, werkt Planningsoptimalisatie met datum- en tijdwaarden die naar datums zijn geconverteerd. Dit verschil in gedrag kan leiden tot situaties waarin bijvoorbeeld prognosetransacties die zijn gemaakt om middernacht op de dag waarop de hoofdplanning wordt uitgevoerd, niet zijn opgenomen, omdat Planningsoptimalisatie er rekening mee houdt dat ze vóór de huidige datum zijn gemaakt.

## <a name="parameters-for-issue-and-demand-transactions"></a>Parameters voor uitgifte- en vraagtransacties

In de volgende tabel worden de parameters vermeld die door Planningsoptimalisatie worden gebruikt bij het verwerken van uitgifte- en vraagtransacties.

| Parameter | Parameternaam in Planningsoptimalisatie | Omschrijving | Equivalent veld in Microsoft Dynamics 365 Supply Chain Management (in de ReqTrans-tabel) |
|---|---|---|---|
| Geplande uitgiftetijd | `PlannedIssueTime` | De datum waarop de uitgifte momenteel is gepland. | **Einddatum** (`FuturesDate`) en **Vertraagd tot-tijd** (`FuturesTime`) |
| Aangevraagde uitgiftetijd | `RequestedIssueTime` | De uitgiftedatum die is aangevraagd door de gebruiker en die is ingesteld in Supply Chain Management. Deze parameter is alleen van toepassing op vrijgegeven of goedgekeurde geplande orders. Voor geplande orders is deze standaard leeg. | **Gevraagde datum** (`ReqDateDlvOrig`) |
| Vereiste uitgiftetijd | `RequiredIssueTime` | De vereiste uitgiftedatum die is aangepast door Planningsoptimalisatie. Als de aangevraagde uitgiftetijd in het verleden ligt op het moment dat Planningsoptimalisatie wordt uitgevoerd, wordt de vereiste uitgiftetijd gecorrigeerd naar de eerste open dag die niet voor de datum van vandaag ligt. Als de aangevraagde uitgiftetijd is gemarkeerd als geblokkeerd in de kalender, wordt de vereiste uitgiftetijd gecorrigeerd naar de eerste open dag vóór die datum. | **Behoeftedatum** (`ReqDate`) en **Tijd voor vereiste** (`ReqTime`) |
| Vertraging van uitgiftetijd | `IssueTimeDelay` | Het tijdsverschil tussen de geplande uitgiftetijd en de aangevraagde uitgiftetijd voor goedgekeurde en vrijgegeven orders of de vereiste uitgiftetijd. | **Vertraging (in dagen)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Parameters voor ontvangst- en leveringstransacties

In de volgende tabel worden de parameters vermeld die door Planningsoptimalisatie worden gebruikt bij het verwerken van ontvangst- en leveringstransacties.

| Parameter | Parameternaam in Planningsoptimalisatie | Omschrijving | Equivalent veld in Supply Chain Management (in de tabel ReqTrans of ReqPO) |
|---|---|---|---|
| Geplande beschikbaarheidstijd | `PlannedAvailabilityTime` | De datum waarop de ontvangst is gepland voor beschikbaarheid. | **Behoeftedatum** (`ReqDate`) en **Tijd voor vereiste** (`ReqTime`) |
| Geplande ontvangsttijd | `PlannedReceiptTime` | De datum waarop de ontvangst op de locatie aankomt. | **Einddatum** (`FuturesDate`), **Uitgesteld tot tijd** (`FuturesTime`) en **Leveringsdatum** (`ReqDateDlv`) of **Gevraagde datum** (`ReqDateDlvOrig`) als de order nog niet is vrijgegeven. |
| Vereiste beschikbaarheidstijd | `RequiredAvailabilityTime` | De vereiste beschikbaarheidsdatum die is aangepast door Planningsoptimalisatie. | **Behoeftedatum** (`ReqDate`) en **Tijd voor vereiste** (`ReqTime`) |
| Verwachte ontvangsttijd | `ExpectedReceiptTime` | De verwachte ontvangstdatum voor een vrijgegeven ontvangst. De waarde wordt ingesteld door de gebruiker in Supply Chain Management en wordt niet aangepast door Planningsoptimalisatie. Deze parameter is alleen van toepassing op vrijgegeven ontvangsten. | **Gevraagde datum** (`ReqDateDlvOrig`) |
| Vereiste ontvangsttijd | `RequiredReceiptTime` | De vereiste ontvangstdatum die is aangepast door Planningsoptimalisatie. | **Behoeftedatum** (`ReqDate`) en **Tijd voor vereiste** (`ReqTime`) |
| Geplande ordertijd | `PlannedOrderingTime` | De orderdatum die is berekend door Planningsoptimalisatie. | **Orderdatum** (`ReqDateOrder`) en **Ordertijd** (`ReqTimeOrder`) |
| Begintijd geplande activiteit | `PlannedActivityStartTime` | De datum waarop de activiteit voor deze ontvangst moet beginnen. | **Begindatum** (`SchedFromDate`) |
| Vertraging ontvangsttijd | `ReceiptTimeDelay` | Het tijdsverschil tussen de geplande ontvangsttijd en de vereiste ontvangsttijd. | **Vertraging (dagen)** (`FuturesDays`) en **Vertraagd tot-tijd** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Voorbeelden van het gebruik van datumparameters door Planningsoptimalisatie

De plannen in de volgende afbeeldingen zijn op dagniveau, maar Planningsoptimalisatie wordt op een gedetailleerder niveau uitgevoerd. Omdat marges bijvoorbeeld in uren kunnen worden gebruikt, kan de geplande ordertijd 22 januari 2021 om 11:35 zijn enzovoort.

### <a name="example-1-simple-scenario"></a>Voorbeeld 1: eenvoudig scenario

Eén verkooporder met een aangevraagde uitgiftetijd op 22 januari, wordt gedekt door één inkooporder. De volgende instellingen worden gebruikt:

- Geen doorlooptijd
- Geen kalenders (Alle dagen zijn open.)
- Geen marges

In de volgende afbeelding wordt dit scenario getoond. (Selecteer de afbeelding om een grotere versie te openen.)

[![Voorbeeldscenario.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Voorbeeld 2: doorlooptijdscenario

Eén verkooporder met een aangevraagde uitgiftetijd op 22 januari, wordt gedekt door één inkooporder. De volgende instellingen worden gebruikt:

- Drie dagen doorlooptijd
- Geen kalenders (Alle dagen zijn open.)
- Geen marges

In de volgende afbeelding wordt dit scenario getoond. (Selecteer de afbeelding om een grotere versie te openen.)

[![Doorlooptijdscenario.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Voorbeeld 3: margescenario

Eén verkooporder met een aangevraagde uitgiftetijd op 22 januari, wordt gedekt door één inkooporder. De volgende instellingen worden gebruikt:

- Drie dagen doorlooptijd
- Ordermarge van vier dagen
- Beschikbaarheidsmarge van vijf dagen
- Geen kalenders (Alle dagen zijn open.)

In de volgende afbeelding wordt dit scenario getoond. (Selecteer de afbeelding om een grotere versie te openen.)

[![Margescenario.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Voorbeeld 4: vertragingsscenario

Eén verkooporder met een aangevraagde uitgiftetijd op 22 januari, wordt gedekt door één inkooporder. In dit voorbeeld worden dezelfde instellingen gebruikt als in voorbeeld 3, maar de planningsdatum is verplaatst naar 15 januari. Achterwaarts plannen (rode markeringen) mislukt omdat de geplande ordertijd vóór de datum van vandaag moet liggen. De hoofdplanning moet daarom voorwaarts worden gepland en er treden vertragingen op.

In de volgende afbeelding wordt dit scenario getoond. (Selecteer de afbeelding om een grotere versie te openen.)

[![Vertragingsscenario.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Voorbeeld 5: overboekingsscenario

Eén verkooporder in magazijn 1 met een aangevraagde uitgiftetijd op 22 januari, wordt gedekt door één transferorder uit magazijn 2 die wordt gedekt door een geplande inkooporder. De volgende instellingen worden gebruikt:

- Drie dagen doorlooptijd voor verplaatsing (magazijn 1)
- Twee dagen doorlooptijd voor aankoop (magazijn 2)
- Geen kalenders (Alle dagen zijn open.)

In de volgende afbeelding wordt dit scenario getoond. (Selecteer de afbeelding om een grotere versie te openen.)

[![Overboekingsscenario.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Voorbeeld 6: doorlooptijd met kalenderscenario

Eén verkooporder met een aangevraagde uitgiftetijd op 22 januari, wordt gedekt door één inkooporder. De volgende instellingen worden gebruikt:

- Drie dagen doorlooptijd
- Uitgiftekalender (gesloten op vrijdag)
- Beschikbaarheidskalender (gesloten op donderdag en vrijdag)
- Ontvangstkalender (gesloten op dinsdag, woensdag en zondag)
- Doorlooptijdkalender (gesloten op donderdag en vrijdag)
- Orderkalender (open op maandag en zaterdag)

In de volgende afbeelding wordt dit scenario getoond. (Selecteer de afbeelding om een grotere versie te openen.)

[![Doorlooptijd met kalenderscenario.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Voorbeeld 7: vertraging met kalenderscenario

Eén verkooporder met een aangevraagde uitgiftetijd op 22 januari, wordt gedekt door één inkooporder. In dit voorbeeld worden dezelfde instellingen gebruikt als in voorbeeld 6, maar de planningsdatum is verplaatst naar 13 januari. Achterwaarts plannen (rode markeringen) mislukt omdat de geplande ordertijd vóór de datum van vandaag moet liggen. De hoofdplanning moet daarom voorwaarts worden gepland en er treden vertragingen op.

In de volgende afbeelding wordt dit scenario getoond. (Selecteer de afbeelding om een grotere versie te openen.)

[![Vertraging met kalenderscenario.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
