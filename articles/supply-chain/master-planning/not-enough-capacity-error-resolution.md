---
title: De planningsenginefout 'Er kan niet voldoende capaciteit worden gevonden' en eindige capaciteit oplossen
description: In dit artikel vindt u informatie over de redenen en oplossingen voor het bericht 'Productieorder %1 kan niet worden gepland. Er kan niet voldoende capaciteit worden gevonden' voor de planningsenginefout.
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135594"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>De planningsenginefout 'Er kan niet voldoende capaciteit worden gevonden' oplossen

[!include [banner](../includes/banner.md)]

Wanneer u de planning uitvoert, wordt mogelijk het volgende foutbericht weergegeven:

> Productieorder %1 kan niet worden gepland. Er kan niet voldoende capaciteit worden gevonden.

Er zijn verschillende redenen waarom de planningsengine niet kan worden uitgevoerd en dit foutbericht wordt weergegeven. Dit artikel biedt richtlijnen die u helpen om de hoofdoorzaak van de fout te vinden en deze vervolgens te beperken.

## <a name="review-the-applicable-resources"></a>De toepasselijke resources controleren

De fout kan optreden als er geen toepasselijke resources voldoen aan de bewerkingsvereisten op de productieorderlocatie.

Volg deze stappen om de toepasselijke resources te controleren.

1. Ga naar **Productiebeheer \> Productieorders \> Alle productieorders** en open of selecteer de productieorder die niet kan worden gepland.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Productiedetails** de optie **Route**.
1. Selecteer op de pagina **Productieroute** de bewerking en selecteer vervolgens in het actievenster **Toepasselijke resources**.
1. Stel in het dialoogvenster **Toepasselijke resources** het veld **Vereisten gebruiken voor** in op *Bewerkingsplanning* of *Taakplanning*, afhankelijk van het type planning dat u gebruikt.
1. Zorg ervoor dat er toepasselijke resources op de productieorderlocatie beschikbaar zijn.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>De kalenders controleren die aan resources zijn gekoppeld

De fout kan optreden als er geen kalender aan de resource of resourcegroep is gekoppeld, of als de bijbehorende kalender niet juist is ingesteld (als in de kalender bijvoorbeeld geen werktijden zijn ingesteld of de efficiëntie ervan als percentage is 0 \[nul\]).

Volg deze stappen om te controleren of er een kalender is gekoppeld aan de resource of resourcegroep.

1. Ga naar **Productiebeheer \> Productieorders \> Alle productieorders** en open of selecteer de productieorder die niet kan worden gepland.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Productiedetails** de optie **Route**.
1. Selecteer op de pagina **Productieroute** de bewerking en selecteer vervolgens in het actievenster **Toepasselijke resources**.
1. Selecteer in het dialoogvenster **Toepasselijke resources** de resource en selecteer vervolgens **Resource weergeven**. U kunt het veld **Resourcegroep** ook selecteren en vasthouden (of met de rechtermuisknop klikken) en vervolgens **Details weergeven** selecteren.
1. Zorg er op de pagina **Resources** of op de pagina **Resourcegroepen** op het sneltabblad **Kalenders** voor dat er een kalender aan de resource of resourcegroep is gekoppeld.

> [!NOTE]
> Als de fout optreedt tijdens het plannen van een bewerking, moet u ervoor zorgen dat er een kalender aan alle toepasselijke resourcegroepen is gekoppeld.

Volg deze stappen om de instellingen van de kalender te bekijken.

1. Ga naar **Organisatiebeheer \> Instellen \> Kalenders \> Kalenders** en selecteer de kalender die aan de resource of resourcegroep is gekoppeld.
1. Selecteer in het actievenster de optie **Werktijden**.
1. Zorg ervoor dat de pagina **Werktijden** niet leeg is. Controleer bovendien voor de dagen waarin u geïnteresseerd bent, dat het veld **Controle** niet is ingesteld op *Afgesloten*, dat er werktijden zijn en dat het veld **Efficiëntie is percentage** niet is ingesteld op *0* (nul).

Als de kalender is gekoppeld aan de basiskalender, moet u ook de instellingen van de basiskalender controleren.

> [!NOTE]
> Bij bewerkingsplanning wordt de kalender van de resourcegroep gebruikt om de begin- en eindtijden en de begin- en einddatums voor elke bewerking te bepalen. Bovendien wordt de hoeveelheid tijd beperkt die het systeem kan plannen voor één specifieke bewerking voor één specifieke dag in een specifieke resourcegroep. Als de werktijden voor een resourcegroep op een bepaalde dag bijvoorbeeld van 8:00 tot 16:00 zijn, kan de belasting van één bewerking voor de resourcegroep niet groter zijn dan de belasting die in acht uur kan worden gepast, ongeacht de hoeveelheid beschikbare capaciteit die de resourcegroep op die dag heeft. De beschikbare capaciteit kan de belasting echter verder beperken.

## <a name="review-the-scheduling-parameters"></a>De planningsparameters bekijken.

Voor goede prestaties wordt door de planningsengine alleen naar een resource gezocht voor een bepaalde tijd en een bepaald aantal planningsconflicten.

Volg deze stappen om de planningsparameters te bekijken.

1. Ga naar **Organisatiebeheer \> Instellen \> Planningsparameters**.
1. Volg één van deze stappen:

    - Als de optie **Planningstime-out ingeschakeld** is ingesteld op *Nee*, gaat u verder met stap 3.
    - Als de optie **Planninstime-out ingeschakeld** is ingesteld op *Ja*, verhoogt u de waarde van het veld **Maximumplanningtijd per reeks** om de verwerking meer tijd te geven om te worden voltooid.

1. Volg één van deze stappen:

    - Als de optie **Time-out planningsoptimalisatie ingeschakeld** is ingesteld op *Nee*, gaat u verder met stap 4.
    - Als de optie **Time-out planningsoptimalisatie ingeschakeld** is ingesteld op *Ja*, verhoogt u de waarde van het veld **Time-out optimalisatiespogingen** om de verwerking meer tijd te geven om te worden voltooid.

1. Als u instellingen op de pagina hebt gewijzigd, kunt u de volgorde opnieuw plannen om het opnieuw te proberen.

## <a name="review-capacity"></a>Capaciteit controleren

De fout kan optreden wanneer u eindige planningen uitvoert, maar er geen vrije capaciteit is.

Voer de volgende stappen uit om onbeperkte capaciteitsplanning uit te voeren.

1. Ga naar **Productiebeheer \> Productieorders \> Alle productieorders** en selecteer of open de productieorder die niet kan worden gepland.
1. Selecteer in het actievenster op het tabblad **Planning** in de groep **Productieorder** de optie **Planningsbewerkingen** of **Taken plannen**.
1. Stel in het dialoogvenster **Planning van bewerkingen** of **Planning van taken** de optie **Eindige capaciteit** in op *Nee*.
1. Selecteer **OK** om de order te plannen.

Volg deze stappen om de beschikbare capaciteit van de resource te controleren.

1. Ga naar **Organisatiebeheer \> Resources \> Resources** en selecteer een resource die van toepassing is op de order die niet kan worden gepland.
1. Selecteer in het actievenster op het tabblad **Resource** in de groep **Weergeven** de optie **Capaciteitsbelasting** of **Grafiek van capaciteitsbelasting** en zorg ervoor dat er capaciteit beschikbaar is.

Volg deze stappen om de beschikbare capaciteit van de resourcegroep te controleren.

1. Ga naar **Organisatiebeheer \> Resources \> Resourcegroepen** en selecteer een resourcegroep die van toepassing is op de order die niet kan worden gepland.
1. Selecteer in het actievenster op het tabblad **Resourcegroep** in de groep **Weergeven** de optie **Capaciteitsbelasting** of **Grafiek van capaciteitsbelasting** en zorg ervoor dat er capaciteit beschikbaar is.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Hoofdplanning boekt een resource als de resourcekalender is afgesloten

Wanneer de bewerkingsplanning wordt gebruikt, wordt de capaciteit gepland op basis van de kalender van de primaire resourcegroep. De secundaire bewerking wordt tegelijk met de primaire bewerking geboekt en er wordt geen rekening gehouden met de kalenders of capaciteit van de secundaire bewerking. Dit kan resulteren in de planning van de productieorder op een afgesloten kalender of op een tijdstip waarop de secundaire bewerking niet beschikbaar is (kalender afgesloten, geen capaciteit).

Wanneer u taakplanning gebruikt, wordt bij het plannen van de order rekening gehouden met de capaciteit en kalender van zowel de primaire als de secundaire bewerking. Kalenders voor de resources van beide bewerkingen moeten geopend zijn en over beschikbare capaciteit beschikken om de order te kunnen plannen.

## <a name="maximum-job-lead-time-is-too-short"></a>De maximale doorlooptijd van de taak is te kort

De planningsengine kan een order niet plannen als de **Maximale doorlooptijd van taak** voor uw site kleiner is dan de doorlooptijd die voor een artikel is opgegeven in de standaardorderinstellingen of in de behoefteplanningsinstellingen.

Als u de instelling **Maximale doorlooptijd van taak** voor uw site wilt weergeven of bewerken, gaat u naar **Productiebeheer \> Instellingen \> Parameters productiebeheer** en opent u het tabblad **Algemeen**.

Voer de volgende stappen uit om de standaardorderinstellingen voor een artikel te definiëren:

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer het relevante product in de lijst.
1. Open in het actievenster het tabblad **Voorraad beheren** en selecteer **Standaardorderinstellingen**.
1. Vouw het sneltabblad **Voorraad** uit en bekijk of bewerk de instelling **Levertijd voorraad** zo nodig.

Voer de volgende stappen uit om de behoefteplanningsinstellingen voor een artikel weer te geven of te bewerken:

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer het relevante product in de lijst.
1. Open in het actievenster het tabblad **Plan** en selecteer **Artikelbehoefteplanning**.
1. Open het tabblad **Doorlooptijd** en bekijk of bewerk de waarde **Productietijd**.

## <a name="excessive-quantity-of-required-resources"></a>Te veel hoeveelheid van vereiste resources

Tijdens het plannen probeert de engine de vereiste resourcehoeveelheid die is ingesteld voor een routebewerking conform de bewerkingsresourcevereisten te matchen met de toepasselijke resources. Als u de resourcehoeveelheid te hoog instelt, kan een route onhaalbaar zijn, waardoor een planningsfout wordt veroorzaakt.

Gebruik de volgende procedure om zowel de opgegeven hoeveelheid als de toepasselijke resources voor een geselecteerd(e) product, route en routebewerking te controleren:

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer het relevante product in het raster.
1. Open in het actievenster het tabblad **Engineer** en selecteer **Route**.
1. Zoek en selecteer de relevante route in het raster.
1. Open het tabblad **Overzicht** onderaan de pagina.
1. Selecteer een bewerking in de lijst met geselecteerde routebewerkingen.
1. Selecteer **Toepasselijke resources** om een dialoogvenster te openen waarin u de toepasselijke resources voor de geselecteerde routebewerking kunt weergeven.
1. Open het tabblad **Belasting resource**. Het veld **Hoeveelheid** toont hier de resourcehoeveelheid die nodig is voor de geselecteerde routebewerking. Bekijk en/of bewerk de hoeveelheid zo nodig.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
