---
title: Een locatie-instructie instellen voor wegzetten van inkooporder
description: Deze procedure laat zien hoe u een eenvoudige locatierichtlijn instelt.
author: ShylaThompson
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ca4b3c2598a268c065011daff31296521faa918
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "349073"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Een locatie-instructie instellen voor wegzetten van inkooporder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een eenvoudige locatierichtlijn instelt. Het voorbeeld dat wordt gegeven, maakt een locatierichtlijn die moet worden gebruikt om te bepalen waar artikelen worden weggezet die zijn ontvangen voor een inkooporder. U kunt deze taakbegeleiding afspelen met de gegevens van het demobedrijf USMF. Precondities: u moet een beschikkingscode maken. In deze procedure gebruiken we een beschikkingscode met de naam Opnieuw labelen. Als u een locatierichtlijn in uw eigen gegevens maakt, moet u geavanceerd magazijnbeheer voor uw magazijn en artikelen hebben ingesteld.  Deze procedure is bedoeld voor de magazijnbeheerder.

1. Ga naar Magazijnbeheer > Instellingen > Instructielocatie.
2. Selecteer 'Inkooporders' in het veld Werkordertype.

## <a name="create-a-location-directive-header"></a>Een locatierichtlijnkop maken
1. Klik op Nieuw.
2. Voer een getal in het veld Volgnummer in.
    * Dit is de volgorde waarin de locatierichtlijn voor het geselecteerde werktype wordt verwerkt. U kunt ook de volgorde wijzigen, als dat nodig is.  
3. Typ een waarde in het veld Naam.
    * Dit is de unieke identificatie voor deze richtlijn.  
4. Selecteer 'Wegzetten' in het veld Werktype.
    * Selecteer het type van werk dat moet worden verwerkt. Voor een richtlijn met het werkordertype Inkooporder is Wegzetten de enige ondersteunde waarde.  
5. Typ een waarde in het veld Locatie.
6. Typ een waarde in het veld Magazijn.
    * Laat de richtlijncode leeg.  Richtlijncodes worden gebruikt om een werkorderregel van het type Wegzetten te koppelen aan een specifieke richtlijn. Voor inkooporders wordt de locatie van de laatste werkorderregel van het type Wegzetten opgelost voordat de werksjabloon wordt bepaald. Daarom is het niet mogelijk om de laatste regel van een werksjabloon te koppelen aan een specifieke richtlijn.   
7. Typ een waarde in het veld Beschikkingscode.
    * De beschikkingscode beperkt het gebruik van de locatierichtlijn, zodat de locatierichtlijn alleen wordt gebruikt als de magazijnwerknemer deze specifieke waarde tijdens registratie van het artikel met een mobiel apparaat invoert.  
8. Klik op Opslaan.

## <a name="edit-the-query-for-directive"></a>De query voor een richtlijn bewerken
1. Klik op Query bewerken.
    * Het gebruik van deze richtlijn is al beperkt tot artikelen die zijn geregistreerd in het magazijn dat u hebt opgegeven, en met de beschikkingscode die u hebt opgegeven. U kunt andere beperkingen toevoegen met de query.  
2. Klik op OK.

## <a name="add-directive-lines"></a>Instructieregels toevoegen
1. Klik op Nieuw.
    * Dit is de volgorde waarin de locatierichtlijnregels worden verwerkt voor het geselecteerde werktype. U kunt ook de volgorde wijzigen, als dat nodig is.  
2. Voer een getal in het veld Vanaf hoeveelheid in.
    * Dit is de kleinste hoeveelheid waarvoor deze richtlijn geldig is.  
3. Voer een getal in het veld Tot hoeveelheid in.
4. Typ een waarde in het veld Eenheid.
    * De eenheid waarin de van- en de tot-hoeveelheid is uitgedrukt. Als u dit veld niet invult, wordt de voorraadeenheid voor het artikel gebruikt.  
5. Selecteer een optie in het veld Hoeveelheid plaatsen.
    * Geen of Nummerplaathoeveelheid: de hoeveelheid die op elke nummerplaat is geregistreerd. In eenheden omgezette hoeveelheid: de volledige hoeveelheid die is geregistreerd. Resterende hoeveelheid: de hoeveelheid die nog moeten worden geregistreerd vanaf de inkooporderregel. Verwachte hoeveelheid: de totale hoeveelheid die is opgegeven op de inkooporderregel.  
6. Schakel het selectievakje Beperken op eenheid in of uit.
    * Als u deze optie selecteert en de eenheid op de pagina Beperken op eenheid opgeeft, kunnen alleen artikelen met die maateenheid op de locatie worden geplaatst. Stel dat de maateenheid PL (pallets) is, dan kunnen alleen artikelen in pallets op een bepaalde locatie worden geplaatst.  
7. Schakel het selectievakje Splitsing toestaan in of uit.
    * Hierdoor kan de hoeveelheid over meerdere locaties worden gesplitst.  
8. Klik op Opslaan.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>De richtlijnregel beperken tot een specifieke eenheid
1. Klik op Beperken op eenheid.
    * Deze knop is alleen beschikbaar wanneer u op Opslaan drukt nadat u het selectievakje Beperken op eenheid hebt geselecteerd.  
2. Typ een waarde in het veld Eenheid.
3. Sluit de pagina.

## <a name="add-a-location-directive-action-line"></a>Een actieregel voor een locatierichtlijn toevoegen
1. Klik op Nieuw.
    * Dit is de volgorde waarin de locatierichtlijnactieregels worden verwerkt voor het geselecteerde werktype. U kunt ook de volgorde wijzigen, als dat nodig is.  
2. Typ een waarde in het veld Naam.
    * Dit is de unieke id voor deze richtlijnactie.  
3. Selecteer een optie in het veld Gebruik vaste locaties.
    * Vaste en niet-vaste locaties: alle niet-vaste locaties zijn geldig, evenals de eigen vaste locatie van het product, binnen het in de query opgegeven bereik.  Alleen vaste locaties voor het product: vaste locaties voor het product zijn geldig en alle productvarianten delen dezelfde set vaste locaties. Alleen vaste locaties voor de productvariant: alleen vaste locaties die zijn opgegeven voor elke productvariant, zijn geldig.  
4. Selecteer een optie in het veld Strategie.
    * Werkorders van het type Inkooporder ondersteunen de volgende strategieën: Geen: het artikel wordt geplaatst op de eerste locatie die wordt gevonden. Consolideren: het artikel wordt geplaatst op een locatie waar soortgelijke artikelen al beschikbaar zijn. Lege locatie zonder werk: het artikel wordt geplaatst op de eerste lege locatie die wordt gevonden. Een locatie wordt beschouwd als leeg als deze geen fysieke voorraad en geen verwacht inkomend werk heeft.  
5. Klik op Opslaan.

## <a name="edit-the-query-for-directive-action-line"></a>De query voor een richtlijnactieregel bewerken
1. Klik op Query bewerken.
2. Klik op Toevoegen.
3. Typ 'locatieprofiel-id' in het veld Veld.
    * In dit voorbeeld worden de mogelijke locaties beperkt met een locatieprofiel-id.  
4. Typ een waarde in het veld Criteria.
5. Klik op OK.
    * U kunt richtlijnregels en richtlijnacties blijven toevoegen totdat u alle mogelijke scenario's in uw magazijn hebt gehad.  

