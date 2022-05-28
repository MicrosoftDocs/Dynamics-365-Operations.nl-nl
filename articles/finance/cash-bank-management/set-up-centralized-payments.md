---
title: Gecentraliseerde betalingen instellen
description: Voer de volgende stappen uit ter voorbereiding van het verwerken van betalingen in een rechtspersoon namens andere rechtspersonen in uw organisatie.
author: kweekley
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03dcef5ae8d5afb21b802fae92934eadc778070d
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725396"
---
# <a name="set-up-centralized-payments"></a>Gecentraliseerde betalingen instellen

[!include [banner](../includes/banner.md)]

Voer de volgende stappen uit ter voorbereiding van het verwerken van betalingen in een rechtspersoon namens andere rechtspersonen in uw organisatie. Voordat u begint, moeten de volgende instellingen zijn geconfigureerd:

-   Maak rechtspersonen.
-   Stel de parameters en rekeningschema's van het grootboek in.
-   Stel de parameters voor leveranciers en de parameters voor klanten in (afhankelijk van de modules waarin gecentraliseerde betalingen worden gebruikt).
-   Stel intercompany-boekhouding in.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Een organisatiehiërarchie instellen voor gecentraliseerde betalingen
U moet een organisatiehiërarchie instellen voor gecentraliseerde betalingen. Dezelfde organisatiehiërarchie wordt gebruikt voor het verwerken van gecentraliseerde leveranciersbetalingen en gecentraliseerde klantenbetalingen. **Opmerking:** de structuur van de hiërarchie is niet van belang voor gecentraliseerde betalingen. Elke rechtspersoon in de hiërarchie kan betalingen verwerken namens elke andere rechtspersoon in de hiërarchie. Op de pagina **Organisatiehiërarchieën** kunt u een nieuwe organisatiehiërarchie maken. Selecteer in het veld **Doel** **Gecentraliseerde betalingen**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Een intercompany-boekhouding instellen voor gecentraliseerde betalingen
Wanneer betalingstransacties in de huidige rechtspersoon worden vereffend met facturen in andere rechtspersonen, worden de toepasselijke transacties voor betaling aan en betaling van voor elke rechtspersoon gemaakt. U moet de rechtspersoon opgeven waar alle van toepassing zijnde contantkortingen en eventuele winst- of verliesbedragen worden geboekt. Voordat u begint, moet u vaststellen welke rechtspersoon u gaat gebruiken om leveranciers- en klantbetalingen te verwerken. Als één rechtspersoon leveranciersbetalingen verwerkt, maar een andere rechtspersoon klantbetalingen verwerkt, moet u naar elke rechtspersoon overschakelen. Selecteer op de pagina **Intercompany-boekhouding** een intercompany-relatierecord voor een rechtspersoon namens welke u betalingen verwerkt. 

Op het tabblad **Gecentraliseerde betalingen** selecteert u of contantkortingen moeten worden geboekt naar de rechtspersoon van de betaling (of een andere transactie die het saldo van de leverancierrekening reduceert), of naar de rechtspersoon van de factuur (of een andere transactie die het saldo van de leverancierrekening vergroot). Deze selectie werkt samen met het veld **Administratie voor contantkorting** op de pagina's **Parameters van module Leveranciers** en **Parameters van module Klanten**. Voor overbetalingen en afrondingsverschillen wordt de instelling in de rechtspersoon van de betaling gebruikt. Voor onderbetalingen en afrondingsverschillen wordt de instelling in de rechtspersoon van de factuur gebruikt.

## <a name="map-vendor-accounts-across-legal-entities"></a>Leverancierrekeningen tussen rechtspersonen toewijzen
Als u een leverancier betaalt vanuit de ene rechtspersoon en wilt facturen voor die leverancier selecteren in andere rechtspersonen, moet u ervoor zorgen dat alle desbetreffende leveranciersrekeningen in elke rechtspersoon allemaal dezelfde adresboek-ID gebruiken. Als u een betaling ontvangt van een klant die facturen betaalt in meerdere rechtspersonen, moet u ervoor zorgen dat alle bijbehorende klantrekeningen in elke rechtspersoon alle dezelfde adresboek-ID gebruiken.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Boekingsprofielen configureren voor gecentraliseerde betalingen
Als u een betaling maakt in een rechtspersoon die facturen in andere rechtspersonen vereffent, moeten de ID's van de boekingsprofielen in beide rechtspersonen gelijk zijn. Om er zeker van te zijn dat betalingen correct worden gemaakt, stelt u in elke rechtspersoon van de factuur een boekingsprofiel in dat overeenkomt met de boekingsprofielen die worden gebruikt in de rechtspersoon van de betaling. Schakel over naar de eerste rechtspersoon van de factuur en vervolgens kunt u op de pagina **Boekingsprofielen van leverancier** een nieuw boekingsprofiel maken of een bestaand boekingsprofiel bewerken. De selecties die u maakt voor het boekingsprofiel in de te betalen rechtspersoon, hoeven niet overeen te komen met de instellingen van het boekingsprofiel in de te factureren rechtspersoon.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Betalingsmethoden instellen voor gecentraliseerde betalingen
Als u een betaling maakt in een rechtspersoon die facturen in andere rechtspersonen vereffent, moeten de ID's van de betalingsmethoden in beide rechtspersonen gelijk zijn. Om er zeker van te zijn dat betalingen correct worden gemaakt, stelt u in elke rechtspersoon van de factuur een betalingsmethode in die overeenkomt met de betalingsmethoden die worden gebruikt in de rechtspersoon van de betaling. Schakel over naar de eerste rechtspersoon van de factuur en vervolgens kunt u op de pagina **Betalingsmethoden** een nieuwe betalingsmethode maken of een bestaande betalingsmethode bewerken. De selecties die u maakt voor de betalingsmethode in de rechtspersoon van de factuur, hoeven niet overeen te komen met de manier waarop de betalingsmethode is ingesteld in de rechtspersoon van de betaling.

## <a name="set-up-default-descriptions"></a>Standaardbeschrijvingen opzetten
U kunt standaardbeschrijvingen definiëren voor intercompany-vereffeningsboekstukken. De standaardbeschrijving wordt opgenomen in de bedoeld-voor en afkomstig-van transacties tijdens het cross-company vereffeningsproces. Op de pagina **Standaardomschrijvingen** kunt u nieuwe omschrijvingen voor zowel **Intercompany-vereffening van klant** als voor **Intercompany-vereffening van leverancier** maken door een taal te selecteren en vervolgens tekst in te voeren.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
