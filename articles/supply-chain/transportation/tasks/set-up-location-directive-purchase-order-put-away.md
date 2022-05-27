---
title: Een locatie-instructie instellen voor wegzetten van inkooporders
description: In dit onderwerp wordt beschreven hoe u een eenvoudige locatie-instructie instelt.
author: Weijiesa
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2275b2fd70e246955054930b13f29a6c0b287363
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674133"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Een locatie-instructie instellen voor wegzetten van inkooporders

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een eenvoudige locatie-instructie instelt. Het voorbeeld dat wordt gegeven, maakt een locatierichtlijn die moet worden gebruikt om te bepalen waar artikelen worden weggezet die zijn ontvangen voor een inkooporder. U kunt deze taakbegeleider afspelen met de gegevens van het demobedrijf USMF. Precondities: u moet een beschikkingscode maken. In deze procedure gebruiken we een beschikkingscode met de naam Opnieuw labelen. Als u een locatierichtlijn in uw eigen gegevens maakt, moet u geavanceerd magazijnbeheer voor uw magazijn en artikelen hebben ingesteld. Deze procedure is bedoeld voor de magazijnbeheerder.

1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellingen > Locatie-instructie**.
2. Selecteer **Inkooporders** in het veld **Werkordertype**.

## <a name="create-a-location-directive-header"></a>Een locatierichtlijnkop maken
1. Selecteer **Nieuw**.
2. Typ een getal in het veld **Volgnummer**. Dit is de volgorde waarin de locatierichtlijn voor het geselecteerde werktype wordt verwerkt. U kunt ook de volgorde wijzigen, als dat nodig is.  
3. Typ een waarde in het veld **Naam**. Dit is de unieke identificatie voor deze richtlijn.  
4. Selecteer **Wegzetten** in het veld **Werktype**. Selecteer het type van werk dat moet worden verwerkt. Voor een richtlijn met het werkordertype Inkooporder is **Wegzetten** de enige ondersteunde waarde.  
5. Typ een waarde in het veld **Locatie**.
6. Typ een waarde in het veld **Magazijn**. Laat de richtlijncode leeg.  Richtlijncodes worden gebruikt om een werkorderregel van het type Wegzetten te koppelen aan een specifieke richtlijn. Voor inkooporders wordt de locatie van de laatste werkorderregel van het type Wegzetten opgelost voordat de werksjabloon wordt bepaald. Daarom is het niet mogelijk om de laatste regel van een werksjabloon te koppelen aan een specifieke richtlijn.   
7. Typ een waarde in het veld **Beschikkingscode**. De beschikkingscode beperkt het gebruik van de locatierichtlijn, zodat de locatierichtlijn alleen wordt gebruikt als de magazijnwerknemer deze specifieke waarde tijdens registratie van het artikel met een mobiel apparaat invoert.  
8. Selecteer **Opslaan**.

## <a name="edit-the-query-for-directive"></a>De query voor een richtlijn bewerken
1. Selecteer **Query bewerken**. Het gebruik van deze richtlijn is al beperkt tot artikelen die zijn geregistreerd in het magazijn dat u hebt opgegeven, en met de beschikkingscode die u hebt opgegeven. U kunt andere beperkingen toevoegen met de query.  
2. Selecteer **OK**.

## <a name="add-directive-lines"></a>Instructieregels toevoegen
1. Selecteer **Nieuw**. Dit is de volgorde waarin de locatierichtlijnregels worden verwerkt voor het geselecteerde werktype. U kunt ook de volgorde wijzigen, als dat nodig is.  
2. Voer een getal in het veld **Vanaf hoeveelheid** in. Dit is de kleinste hoeveelheid waarvoor deze richtlijn geldig is.  
3. Voer een getal in het veld **Tot hoeveelheid** in.
4. Typ een waarde in het veld **Eenheid**. De eenheid waarin de van- en de tot-hoeveelheid is uitgedrukt. Als u dit veld niet invult, wordt de voorraadeenheid voor het artikel gebruikt.  
5. Selecteer een optie in het veld **Hoeveelheid plaatsen**.
    - Geen of Nummerplaathoeveelheid: de hoeveelheid die op elke nummerplaat is geregistreerd.  
    - In eenheden omgezette hoeveelheid: de volledige hoeveelheid die is geregistreerd.  
    - Resterende hoeveelheid: de hoeveelheid die nog moeten worden geregistreerd vanaf de inkooporderregel.  
    - Verwachte hoeveelheid: de totale hoeveelheid die is opgegeven op de inkooporderregel.  
6. Schakel het selectievakje **Beperken op eenheid** in of uit. Als u deze optie selecteert en de eenheid op de pagina **Beperken op eenheid** opgeeft, kunnen alleen artikelen met die maateenheid op de locatie worden geplaatst. Stel dat de maateenheid PL (pallets) is, dan kunnen alleen artikelen in pallets op een bepaalde locatie worden geplaatst.  
7. Schakel het selectievakje **Splitsing toestaan** in of uit. Hierdoor kan de hoeveelheid over meerdere locaties worden gesplitst.  
8. Selecteer **Opslaan**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>De richtlijnregel beperken tot een specifieke eenheid
1. Selecteer **Beperken op eenheid**. Deze knop is alleen beschikbaar wanneer u op **Opslaan** drukt nadat u het selectievakje **Beperken op eenheid** hebt geselecteerd.  
2. Typ een waarde in het veld **Eenheid**.
3. Sluit de pagina.

## <a name="add-a-location-directive-action-line"></a>Een actieregel voor een locatierichtlijn toevoegen
1. Selecteer **Nieuw**. Dit is de volgorde waarin de locatierichtlijnactieregels worden verwerkt voor het geselecteerde werktype. U kunt ook de volgorde wijzigen, als dat nodig is.  
2. Typ een waarde in het veld **Naam**. Dit is de unieke id voor deze richtlijnactie.  
3. Selecteer een optie in het veld **Gebruik vaste locaties**.
    - Vaste en niet-vaste locaties: alle niet-vaste locaties zijn geldig, evenals de eigen vaste locatie van het product, binnen het in de query opgegeven bereik.  
    - Alleen vaste locaties voor het product: vaste locaties voor het product zijn geldig en alle productvarianten delen dezelfde set vaste locaties.  
    - Alleen vaste locaties voor de productvariant: alleen vaste locaties die zijn opgegeven voor elke productvariant, zijn geldig.  
4. Selecteer een optie in het veld **Strategie**. Werkorders van het type Inkooporder ondersteunen de volgende strategieën: 
    - Geen: het artikel wordt op de eerste locatie geplaatst die wordt gevonden.  
    - Consolideren: het artikel wordt geplaatst op een locatie waar soortgelijke artikelen al beschikbaar zijn.  
    - Lege locatie zonder werk: het artikel wordt geplaatst op de eerste lege locatie die wordt gevonden. Een locatie wordt beschouwd als leeg als deze geen fysieke voorraad en geen verwacht inkomend werk heeft.  
5. Selecteer **Opslaan**.

## <a name="edit-the-query-for-directive-action-line"></a>De query voor een richtlijnactieregel bewerken
1. Selecteer **Query bewerken**.
2. Selecteer **Toevoegen**.
3. Typ `location profile ID` in het veld **Veld**. In dit voorbeeld worden de mogelijke locaties beperkt met een locatieprofiel-id.  
4. Typ een waarde in het veld **Criteria**.
5. Selecteer **OK**. U kunt richtlijnregels en richtlijnacties blijven toevoegen totdat u alle mogelijke scenario's in uw magazijn hebt gehad.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]