---
title: De productieorderstatus omkeren
description: In dit onderwerp wordt beschreven hoe de productieorderstatus kan worden omgekeerd.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmStatusDecrease, ProdSetupStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7529e6c2bd7cb6b8386565c9f19075e56a65d3c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425428"
---
# <a name="reverse-the-production-order-status"></a>De productieorderstatus omkeren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe de productieorderstatus kan worden omgekeerd. 

Als u de status van een productieorder omkeert, gaan de productieorder zelf en alle bewerkingen die aan de routes zijn gekoppeld een stap terug in de levensloop van de productieorder. Stel dat een productieorder een status heeft van **Gepland** en u de status terug wijzigt naar **Gemaakt**. In dit geval, moet het systeem eerst de status wijzigen in **Geraamd**. Dit is de status die direct voorafgaat aan **Gepland**. Vervolgens kan de status worden gewijzigd in de status die u wilt, namelijk **Gemaakt**. **Opmerking:** Als uw order de status **Gereedmelden** heeft bereikt, kunt u deze nog steeds terugzetten naar een eerdere status. U moet echter wel een nieuwe raming en planning van bewerkingen of taakplanning of beide uitvoeren om de informatie over de order bij te werken. Deze stap is vereist omdat eventuele reserveringen van resterend artikelverbruik en resourceverbruik eveneens opnieuw moeten worden ingesteld. In de rest van dit artikel wordt uitgelegd wat er gebeurt wanneer u de status van een productieorder op de volgende manieren terugzet:

-   Van **Geraamd** naar **Gemaakt**
-   Van **Gepland** naar **Geraamd**
-   Van **Vrijgegeven** naar **Gepland**
-   Van **Begonnen** naar **Vrijgegeven**

## <a name="from-estimated-to-created"></a>Van Geraamd naar Gemaakt
Wanneer u de status van een productieorder omkeert van **Geraamd** naar **Gemaakt**, wordt het artikelverbruik dat is berekend voor de artikelen in de stuklijst verwijderd. Voorraadtransacties op de productieregel worden verwijderd en het veld **Status van rest** op stuklijstregels van de productieorder wordt opnieuw ingesteld op **Beëindigd**. Als de opties **Afgeleide inkopen** en **Afgeleide productie** worden geselecteerd, worden eventuele onderliggende inkooporders of productieorders verwijderd. Als u de kosten van de productieorder hebt geraamd of handmatig artikelen hebt gereserveerd voor gebruik in de productie, worden deze transacties verwijderd.

## <a name="from-scheduled-to-estimated"></a>Van Gepland naar Geraamd
Wanneer u de status van een productieorder terugzet van **Gepland** naar **Geraamd**, worden de geplande begin- en einddatums en -tijden verwijderd. Capaciteitsreserveringen en taken die tijdens de planning zijn gemaakt, worden verwijderd. Alle gegevens die over bewerkingsplanning en taakplanning zijn geregistreerd op de pagina **Details van productieorder** worden opnieuw ingesteld.

## <a name="from-released-to-scheduled"></a>Van Vrijgegeven naar Gepland
Wanneer u de status van een productieorder terugzet van **Vrijgegeven** naar **Gepland**, wordt alleen de waarde in het statusveld gewijzigd.

## <a name="from-started-to-released"></a>Van Begonnen naar Vrijgegeven
Wanneer u de status van een productieorder omkeert van **Begonnen** naar **Vrijgegeven**, worden alle artikelen die zijn gereedgemeld teruggeplaatst. Als er materiaal is opgenomen of als er inkomende of uitgaande leveringen zijn gedaan, worden deze instellingen eveneens teruggezet. Het veld **Status van rest** op de stuklijstregels van de productieorder wordt gewijzigd van **Beëindigd** in **Materiaalverbruik**. Als tijd is geregistreerd of als hoeveelheden zijn gereedgemeld voor de bewerkingen in de productieroute, worden deze instellingen ongedaan gemaakt. Het veld **Status van rest** wordt gewijzigd van **Beëindigd** in **Routeverbruik** in de productieroute. De instellingen voor alle artikelen die zijn geboekt in het proces of onderhanden werk, worden omgekeerd. Op de pagina **Details van productieorder** worden velden die een hoeveelheid weergeven die is gestart of gereedgemeld opnieuw ingesteld. De datums voor deze transacties worden eveneens opnieuw ingesteld.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]