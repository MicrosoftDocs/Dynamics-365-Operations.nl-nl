---
title: Bron voor bedrijfsactiviteiten maken
description: Een bron voor bedrijfsactiviteiten voert de activiteiten van een project of een productieproces uit.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9d8f13e29ea813eb9721ddca795b67837e2aa5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "350062"
---
# <a name="create-an-operations-resource"></a>Bron voor bedrijfsactiviteiten maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Een bron voor bedrijfsactiviteiten voert de activiteiten van een project of een productieproces uit. Deze procedure toont u hoe u een bron voor bedrijfsactiviteiten definieert. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.

1. Ga naar Resources.
2. Klik op Nieuw.
3. Typ een waarde in het veld Bron.
4. Typ een waarde in het veld Omschrijving.

## <a name="define-capacity-and-consumption-parameters"></a>Parameters voor capaciteit en verbruik definiëren
1. Vouw de sectie Bewerking uit.
2. Voer in het veld Uitvalpercentage een getal in.
3. Typ of selecteer een waarde in het veld Instelcategorie.
    * Geef de kostencategorie op die bepaalt hoe de kosten van de voorbereidingstijd moeten worden verantwoord.  
4. Typ of selecteer een waarde in het veld Uitvoeringstijdcategorie.
    * Geef de kostencategorie op die bepaalt hoe de kosten van de uitvoeringstijd moeten worden verantwoord.  
5. Typ of selecteer een waarde in het veld Hoeveelheidscategorie.
    * Geef de kostencategorie op die bepaalt hoe de resourcekosten op basis van de uitvoerhoeveelheid moeten worden verantwoord.  
6. Selecteer een optie in het veld Capaciteitseenheid.
    * Geef de eenheid op waarin de capaciteit van de bron voor bedrijfsactiviteiten wordt uitgedrukt.  
7. Voer een nummer in het veld Capaciteit in.
8. U moet een getal invoeren in het veld Efficiëntiepercentage.
    * Geef de efficiëntie op die u van de bron voor bedrijfsactiviteiten verwacht. Het efficiëntiepercentage past de doorvoercapaciteit van de bron voor bedrijfsactiviteiten aan en beïnvloedt de tijd die voor de bron is gereserveerd.  
9. Voer in het veld Percentage bewerkingsplanning een getal in.
    * Geef het maximumpercentage van de capaciteit van de bron voor bedrijfsactiviteiten op die u in bewerkingsplanning wilt gebruiken.  
10. Selecteer Ja in het veld Eindige capaciteit.
    * Stel deze optie in op Ja als de bron voor bedrijfsactiviteiten moet worden gepland op basis van de werkelijke capaciteit die beschikbaar is, en als de bestaande capaciteitsreserveringen in aanmerking moeten worden genomen. Als deze optie is ingesteld op Nee, wordt aangenomen dat de bron voor bedrijfsactiviteiten oneindige capaciteit heeft, en kan bron worden overboekt.  
11. Selecteer Ja in het veld Bottleneck resource.

## <a name="define-working-times"></a>Werktijden definiëren
1. Vouw de sectie Kalenders uit.
2. Klik op Toevoegen.
3. Typ of selecteer een waarde in het veld Kalender.
    * Geef de werktijdkalender op die de capaciteit (in uren) van de resource definieert.  
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="define-resource-capabilities"></a>Bronmogelijkheden definiëren
1. Vouw de sectie Mogelijkheden uit.
2. Klik op Toevoegen.
    * Een capaciteit is de mogelijkheid van een bron voor bedrijfsactiviteiten om een bepaalde activiteit uit te voeren. De planningsengine wijst bronnen toe door de bronbehoeften van elke activiteit te vergelijken met de mogelijkheden van de beschikbare bronnen voor bedrijfsactiviteiten.  
3. Typ of selecteer een waarde in het veld Mogelijkheid.
4. Voer een nummer in het veld Niveau in.
    * Geef het vaardigheidsniveau op waarop de bron de capaciteit verwerkt.  
5. Voer een getal in het veld Prioriteit in.
    * Geef de prioriteit van de bron voor bedrijfsactiviteiten met betrekking tot de capaciteit op. Bij planning met prioriteit, wordt de bron voor bedrijfsactiviteiten met de hoogste prioriteit (de laagste numerieke waarde) als eerste geselecteerd.  

## <a name="assign-resource-to-resource-group"></a>Resource toewijzen aan resourcegroep
1. Vouw de sectie Resourcegroepen uit.
2. Klik op Toevoegen.
    * De resourcegroep definieert de locatie, productie-eenheid en magazijncontext voor bronnen voor bedrijfsactiviteiten. De bron voor bedrijfsactiviteiten kan alleen worden gepland indien toegewezen aan een resourcegroep, en alleen op de locatie waar de resourcegroep zich bevindt.  
3. Typ of selecteer een waarde in het veld Resourcegroep.
4. Typ of selecteer een waarde in het veld Invoerlocatie.
    * Geef de magazijnlocatie op van waar de bron voor bedrijfsactiviteiten materialen verbruikt.  

