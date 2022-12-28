---
title: Problemen met de afstemming van gegevens van een Z-rapport
description: In dit artikel worden de problemen beschreven die gebruikers kunnen ondervinden met de gegevensafstemming van een Z-rapport in Commerce Headquarters. Het beschrijft ook mogelijke basisoorzaken en oplossingen die kunnen helpen toekomstige voorvallen te voorkomen.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832122"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Problemen met de afstemming van gegevens van een Z-rapport

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor het oplossen van problemen die kunnen helpen bij het afstemmen van gegevens van een Z-rapport in Microsoft Dynamics 365 Commerce Headquarters. Het beschrijft problemen die gebruikers kunnen ondervinden met de gegevensafstemming, mogelijke hoofdoorzaken en tevens oplossingen die kunnen helpen toekomstige gebeurtenissen te voorkomen.

## <a name="description"></a>Description

- De bedragen in het Z-rapport en de totalen die op het berekende overzicht worden weergegeven, komen niet overeen.
- De transactie in Headquarters heeft een onjuist aantal regelartikelen of het regeltotaal en het totaal van de transactie komen niet overeen.
- Het aantal transacties dat in een ploeg in Headquarters wordt weergegeven, is kleiner dan het aantal transacties in het Z-rapport.
- De boeking van het overzicht is mislukt om een van de voorgaande redenen.

### <a name="root-cause"></a>Hoofdoorzaak

De meest voorkomende hoofdoorzaak van de eerder beschreven symptomen is het genereren van dubbele transactie-id's in de kanaaldatabase. Dubbele transactie-id's kunnen om de volgende redenen niet worden gegenereerd:

- De lokale databaseopslag van Modern Point of Sale (MPOS) is beschadigd.
- MPOS heeft enkele transacties in offlinemodus en wordt opnieuw geactiveerd door een account te gebruiken dat geen toegang heeft tot de offlinedatabase.
- Er is een probleem met aanpassing dat is gerelateerd aan het genereren van transactie-id's.

## <a name="resolution"></a>Oplossing

Commerce baseert zich meestal op een nummerreeks om opeenvolgende transactie-id's te genereren. Als het systeem niet kan bepalen dat om welke reden dan ook een nummerreeks is gebruikt, wordt een dubbele transactie-id gegenereerd. 

Om het probleem met dubbele transactie-id's op te lossen, maakt u een ondersteuningsticket om na te gaan of de transactiegegevens kunnen worden gecorrigeerd. In sommige gevallen, zoals bij geen gegevensverlies in Headquarters, is het niet mogelijk om vereiste gegevens te repareren.

Om dit probleem in de toekomst te voorkomen, schakelt u de functie **Nieuwe transactie-id inschakelen om dubbele transactie-id's te voorkomen** in Headquarters in. Deze functie is geïntroduceerd Commerce versie 10.0.19. U kunt hiermee voorkomen dat opeenvolgende transactie-id's worden gemaakt door ervoor te zorgen dat voor elke transactie een unieke transactie-id wordt gemaakt. Zie [Dubbele transactie-id's voorkomen](../channel-setup-retail.md#ensure-unique-transaction-ids) voor meer informatie over deze functie.
