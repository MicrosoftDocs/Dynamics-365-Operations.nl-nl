---
title: Actiezoekopdracht
description: In dit artikel wordt de zoekfunctionaliteit voor acties in Microsoft Dynamics 365 for Operations beschreven. Met een actiezoekopdracht kunt u zoeken naar acties op een pagina en deze uitvoeren.
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ef5709889dcabd4c9ed760f57d210956f38c37e9
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="action-search"></a>Actiezoekopdracht

[!include[banner](../includes/banner.md)]


In dit artikel wordt de zoekfunctionaliteit voor acties in Microsoft Dynamics 365 for Operations beschreven. Met een actiezoekopdracht kunt u zoeken naar acties op een pagina en deze uitvoeren.

<a name="introduction"></a>Introductie
------------

Pagina's in Microsoft Dynamics 365 for Operations bevatten voornamelijk opdrachten in actiedeelvensters, zowel in het standaardactievenster dat boven aan de pagina wordt weergegeven als op de werkbalken die in verschillende gedeelten van de pagina worden weergegeven. In eerdere versies kon u met de functie Tips toetsen snel een knop in een actievenster openen door op de Alt-toets en vervolgens op een reeks letters te drukken. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) In de huidige versie van Dynamics 365 for Operations zijn Tips toetsen echter niet meer beschikbaar en zijn deze vervangen door de functie actiezoekopdrachten. Met deze nieuwe functie kunt u snel zoeken en een knop uitvoeren van elk weergegeven actievenster.

## <a name="using-action-search"></a>Actiezoekopdrachten gebruiken
Om de functie van het actiezoekfunctie te gebruiken, volgt u deze stappen.

1.  Op het actievenster, klikt u in het veld **actiezoekopdracht**. (Het **actiezoekopdracht**-veld bevat een vergrootglaspictogram.)
2.  Typ de hele of een deel van de naam van de knop die u wilt gebruiken. U kunt ook zoeken met behulp van woorden van het "pad" van de knop. (Zie de volgende sectie van dit artikel voor meer informatie.) Een knop wordt normaal gesproken boven aan de lijst met resultaten weergegeven nadat u twee tot vier tekens hebt getypt.
3.  Zoek en start de knop in de resultatenlijst (met de muis of het toetsenbord).

Nadat de knop is uitgevoerd, keert de focus terug naar uw de laatste positie op de pagina, zodat u door kunt werken. 

[![actiezoekopdracht-veld](./media/action-search-field.png)](./media/action-search-field.png)

U kunt actiezoekopdrachten ook starten door Ctrl+/ of Alt+Q in te drukken. Druk opnieuw op de toetsenbordsneltoets om de focus terug te plaatsen naar uw laatste positie op de pagina.

## <a name="understanding-the-results-list"></a>De resultatenlijst begrijpen
Vaak moet u in Dynamics 365 for Operations zowel de locatie als de context van een knop weten om het doel van die knop volledig te begrijpen. Daarom wordt er aanvullende informatie weergegeven voor elk item in de lijst met resultaten, zodat u precies begrijpt welke knoppen in de lijst worden weergegeven. In het bijzonder wordt het 'pad' van de knop weergegeven. Dit pad kan de labels van de volgende UI-elementen bevatten, indien dit relevant is:

-   Tabblad actievenster
-   Knopgroep
-   Menuknop (als de knop in een menuknop is)
-   Menuscheidingsteken (als de knop in een benoemde groep in een menuknop is)
-   Groep of tabblad op de pagina (bijvoorbeeld de naam van een sneltabblad)

U hebt bijvoorbeeld **tot** in het **actiezoek**-veld getypt en bekijkt nu de resultatenlijst. Het eerste item, voor een knop met de naam **Totalen**, wordt gemarkeerd. Een knoppad van **Verkooporder** &gt; **Weergave** wordt ook weergegeven. Het gedeelte **Verkooporder** van het pad komt overeen met het tabblad **Verkooporder** in het actievenster en het gedeelte **Weergave** van het pad komt overeen met de groep **Weergave** op dat tabblad. Evenzo geeft het pad van de knop **Totale korting** (**Verkopen** &gt; **Berekenen**) aan dat deze knop zich bevindt in de groep **Berekenen** op het tabblad **Verkopen** van het actievenster. Daarom kunt u aan de hand van deze informatie precies bepalen welke knop wordt geactiveerd door de actiezoekopdracht (als u die knop selecteert in de resultatenlijst). 

[![actiezoekopdracht-veld-met-gegevens](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

In het vorige voorbeeld, werden de resultaten van de actiezoekopdracht van het standaard actievenster bovenaan een pagina weergegeven. De actiezoekopdracht geeft echter ook resultaten weer van zichtbare werkbalken die zich op andere plaatsen op de pagina bevinden. U zoekt bijvoorbeeld naar de knop **Voorhanden voorraad** die zich bevindt op het sneltabblad **Verkooporderregels**. In dit geval geeft het pad van de knop in de lijst met resultaten (**Verkooporderregels** &gt; **Voorraad** &gt; **Weergave**) aan dat deze knop zich bevindt onder de kop **Weergave** op de menuknop **Voorraad** op het sneltabblad **Verkooporderregels**. 

[![voorhanden-voorraad](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Actiezoekopdracht vergeleken met navigatiezoekopdracht
Actiezoekopdrachten zijn bedoeld om acties op een pagina te zoeken en uit te voeren, maar is er een apart zoekmechanisme voor het zoeken en navigeren naar pagina's in Dynamics 365 for Operations. Zie het artikel [Navigatiezoekfunctie](navigation-search.md) voor meer informatie over deze functie.




