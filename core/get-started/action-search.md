---
title: Actiezoekopdracht
description: Dit artikel worden de zoekfunctionaliteit actie in Microsoft Dynamics 365 voor bewerkingen. Actie zoeken kunt u zoeken en uitvoeren van acties op een pagina.
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Actiezoekopdracht

Dit artikel worden de zoekfunctionaliteit actie in Microsoft Dynamics 365 voor bewerkingen. Actie zoeken kunt u zoeken en uitvoeren van acties op een pagina.

<a name="introduction"></a>Introductie
------------

Pagina's in Microsoft Dynamics 365 for Operations blootgesteld voornamelijk opdrachten in actie deelvensters, zowel standaard actievenster die aan het begin van een pagina wordt weergegeven als de werkbalken die worden weergegeven in verschillende gedeelten van de pagina. In vorige versies kunt een functie sleutel Tips u snel toegang tot een knop in een actievenster door op de Alt-toets en vervolgens een reeks letters te drukken. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) echter in de huidige versie van Dynamics 365 for Operations sleutel Tips zijn niet langer beschikbaar, maar zijn vervangen door de zoekfunctie van actie. Met deze nieuwe functie kunt u snel zoeken en een knop uitvoeren van elk weergegeven actievenster.

## <a name="using-action-search"></a>Actiezoekopdrachten gebruiken
Om de functie van het actiezoekfunctie te gebruiken, volgt u deze stappen.

1.  Op het actievenster, klikt u in het veld **actiezoekopdracht**. (Het **actiezoekopdracht**-veld bevat een vergrootglaspictogram.)
2.  Typ of een gedeelte van de naam van de knop die u wilt uitvoeren. U kunt ook zoeken met behulp van woorden uit het van de knop 'pad'. (Zie de volgende sectie van dit artikel voor meer informatie.) Een knop wordt normaal gesproken boven aan de lijst met resultaten weergegeven nadat u twee tot vier tekens hebt getypt.
3.  Zoek en start de knop in de resultatenlijst (met de muis of het toetsenbord).

Nadat de knop is uitgevoerd, keert de focus terug naar uw de laatste positie op de pagina, zodat u door kunt werken. 

[![actie in het veld zoeken](./media/action-search-field.png)](./media/action-search-field.png)

U kunt actiezoekopdrachten ook starten door Ctrl+/ of Alt+Q in te drukken. Druk opnieuw op de toetsenbordsneltoets om de focus terug te plaatsen naar uw laatste positie op de pagina.

## <a name="understanding-the-results-list"></a>De resultatenlijst begrijpen
Vaak in Dynamics 365 voor bewerkingen, moet u weten zowel de locatie en de context van een knop op het doel van die knop volledig te begrijpen. Dus wordt als u meer informatie weergegeven voor elk artikel in de lijst met resultaten kunt u precies begrijpt welke knoppen worden weergegeven in de lijst. In het bijzonder wordt het 'pad' van de knop weergegeven. Dit pad kan de labels van de volgende UI-elementen bevatten, indien dit relevant is:

-   Tabblad actievenster
-   Knopgroep
-   Menuknop (als de knop in een menuknop is)
-   Menuscheidingsteken (als de knop in een benoemde groep in een menuknop is)
-   Groep of tabblad op de pagina (bijvoorbeeld de naam van een sneltabblad)

U hebt bijvoorbeeld **tot** in het **actiezoek**-veld getypt en bekijkt nu de resultatenlijst. Het eerste item, voor een knop met de naam **totalen**, wordt gemarkeerd. Een knop pad van **verkooporder**&gt;**weergave** wordt ook weergegeven. De **verkooporder** deel van het pad overeenkomt met de **verkooporder** tabblad in het actievenster en de **weergave** deel van het pad overeenkomt met de **weergeven** groeperen op dat tabblad. Op dezelfde manier het pad van de **totale korting** knop (**verkopen**&gt;**berekenen**) meldt u dat deze knop bevindt zich in de **berekenen** groeperen op de **verkopen** tabblad van het actievenster. Daarom kunt deze informatie u precies welke knop wordt aangestuurd door actie zoeken (als u die knop in de resultatenlijst) te begrijpen. 

[![actie-zoeken-veld-met-gegevens](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

In het vorige voorbeeld, werden de resultaten van de actiezoekopdracht van het standaard actievenster bovenaan een pagina weergegeven. De actiezoekopdracht geeft echter ook resultaten weer van zichtbare werkbalken die zich op andere plaatsen op de pagina bevinden. Bijvoorbeeld: u zoekt de **voorhanden voorraad** knop op de **verkooporderregels** sneltabblad. In dit geval wordt het pad van de knop in de lijst met resultaten (**verkooporderregels**&gt;**voorraad**&gt;**weergave**) meldt u dat deze knop bevindt zich onder de **weergave** titel op de **voorraad** menuknop op de **verkooporderregels** sneltabblad. 

[![op de voorhanden voorraad](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Actiezoekopdracht vergeleken met navigatiezoekopdracht
Zoeken van de actie is bedoeld om te zoeken en acties uitvoeren op een pagina, wordt er een aparte zoekactie mechanisme voor het zoeken en navigeren naar pagina's in Dynamics 365 voor bewerkingen. Zie voor meer informatie over deze functie, de [navigatie zoeken](navigation-search.md) artikel.


