---
title: Een kanbanregel maken met een kanbanregelgebeurtenis
description: Met deze procedure wordt een kanbanregel gemaakt door de instelling voor kanbanregelgebeurtenissen te gebruiken om pull van een procesactiviteit te activeren.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7aaf959db0f0a136fc615f9a57ec787ef6cf2ad
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579155"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Een kanbanregel maken met een kanbanregelgebeurtenis

[!include [banner](../../includes/banner.md)]

Met deze procedure wordt een kanbanregel gemaakt door de instelling voor kanbanregelgebeurtenissen te gebruiken om pull van een procesactiviteit te activeren. De kanbanregel wordt geactiveerd door een activiteit van het kanbanproces, met een hoeveelheid die gelijk is aan of hoger is dan 25 elk. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze taak is bedoeld voor de procestechnicus of de waardestroombeheerder bij het voorbereiden van de productie van een nieuw of gewijzigd product in een lean-omgeving.


## <a name="create-a-kanban-rule"></a>Een kanbanregel maken
1. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
2. Klik op Nieuw.
3. Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.
    * Hiermee worden rechtstreeks vanuit de vraag kanbans gemaakt. Hiermee worden regels ingesteld voor het definiëren van een maken op bestelling-scenario.  
4. Typ of selecteer een waarde in het veld Eerste planactiviteit.
    * Typ of selecteer SpeakerAssemblyAndPolish. De eerste activiteit van een kanbanregel voor productie is een verwerkingsactiviteit in de productiestroom. Wanneer u de activiteit selecteert, worden de geldigheidsdatums van de activiteit gekopieerd naar de geldigheidsdatums van de kanbanregel.  
5. Vouw de sectie Details uit.
6. Typ 'L0001' in het veld Product.
7. Vouw de sectie Gebeurtenissen uit.
8. Selecteer 'Automatisch' in het veld Kanbanregelgebeurtenis.
    * Hiermee worden gebeurteniskanbans op aanvraag gegenereerd.  Dit veldt wordt gebruikt voor het configureren van kanbanregels die materiaal aanvullen dat nodig is voor een downstream procesactiviteit. Wanneer u Automatisch selecteert, worden de gebeurteniskanbans gemaakt bij de aanvraag. Deze instelling wordt aangeraden als u verwacht op dezelfde dag productie te zullen uitvoeren.  
9. Stel Minimale gebeurtenishoeveelheid in op '25'.
    * Gebeurteniskanbans worden gegenereerd wanneer de vraaghoeveelheid gelijk is aan of groter is dan dit veld. Dit is handig als u een bestelhoeveelheid wilt produceren die kleiner is dan dit veld op de ene machine en meer dan dit veld op een andere machine.  
10. Klik op Opslaan.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Verkooporder maken en kanbanketen activeren
1. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Klantrekening.
    * Selecteer klantrekening US-003, Forest Wholesales.  
4. Klik op OK.
5. Typ in het veld Artikelnummer de waarde 'L0001'.
    * L0001 is het artikel waarvoor u de kanbanregel hebt gemaakt.  
6. Stel Hoeveelheid in op '27'.
    * Omdat 27 hoger is dan de minimumhoeveelheid van 25 op de kanbanregel, wordt hiermee een gebeurteniskanban geactiveerd.  
7. Typ '1' in het veld Locatie.
8. Typ of selecteer een waarde in het veld Magazijn.
    * Selecteer magazijn 13.  
9. Klik op Opslaan.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>De kanban weergeven die door de kanbanregel wordt gegenereerd
1. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
2. Zoek en selecteer de gewenste record in de lijst.
3. Vouw de sectie Kanbans uit.
    * Merk op dat een kanban voor 27 is gemaakt om de activiteit te verwerken die is gebaseerd op de gemaakte kanbanregel.  
    * Dit is de laatste stap.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]