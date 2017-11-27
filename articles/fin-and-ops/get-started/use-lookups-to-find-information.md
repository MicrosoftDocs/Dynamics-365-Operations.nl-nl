---
title: Lookups gebruiken om informatie te vinden
description: Veel velden in Microsoft Dynamics 365 for Finance and Operations hebben lookups waarmee u gemakkelijk de juiste of de gewenste waarde vindt. Enkele verbeteringen zijn toegevoegd aan de lookups, die deze besturingselementen bruikbaarder maken en gebruikers productiever. In dit onderwerp vindt u informatie over deze nieuwe lookupfuncties en handige tips voor een optimaal gebruik van lookups in het systeem.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 013901724864092571099835b2c71b297710ff03
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="use-lookups-to-find-information"></a>Lookups gebruiken om informatie te vinden

[!include[banner](../includes/banner.md)]


Veel velden in Microsoft Dynamics 365 for Finance and Operations hebben lookups waarmee u gemakkelijk de juiste of de gewenste waarde vindt. Enkele verbeteringen zijn toegevoegd aan de lookups, die deze besturingselementen bruikbaarder maken en gebruikers productiever. In dit onderwerp vindt u informatie over deze nieuwe lookupfuncties en handige tips voor een optimaal gebruik van lookups in het systeem.  

<a name="responsive-lookups"></a>Responsieve lookups
------------------

In eerdere versies van Finance and Operations moest een gebruiker bij de interactie met een lookup-besturingselement expliciet een handeling uitvoeren om de vervolgkeuzelijst te openen. Dit kon hij doen door een sterretje (\*) in het besturingselement te typen, om de lookup te filteren op basis van de huidige waarde van het besturingselement, door op de vervolgkeuzepijl te klikken, of met de sneltoets **Alt**+**pijl-omlaag**. Lookup-besturingselementen zijn op de volgende wijzen aangepast, om beter aan te sluiten op bestaande praktijken op het internet:

-   Lookup-vervolgkeuzelijsten openen nu automatisch na een korte pauze in het typen, waarbij de inhoud van de vervolgkeuzelijst wordt gefilterd op basis van de waarde van het lookup-besturingselement.
    -   Houd er rekening mee dat het oude gedrag van de vervolgkeuzelijst, namelijk automatisch openen na het typen van een sterretje (\*), is afgeschaft.
-   Nadat de lookup-vervolgkeuzelijst is geopend, gebeurt het volgende:
    -   De cursor blijft staan in het lookup-besturingselement (in plaats van dat de focus wordt verplaatst naar de vervolgkeuzelijst) zodat u nog wijzigingen kunt aanbrengen in de waarde in het besturingselement. De gebruiker kan echter nog steeds met de toetsen **pijl-omhoog** en **pijl-omlaag** bladeren naar andere rijen in de vervolgkeuzelijst en de huidige rij in de vervolgkeuzelijst selecteren met de Enter-toets.
    -   De inhoud van de vervolgkeuzelijst wordt aangepast nadat wijzigingen zijn aangebracht in de waarde in het lookup-besturingselement.

Neem bijvoorbeeld een lookup-veld met de naam **Plaats**. 

Wanneer de focus zich in het veld **Plaats** bevindt, kunt u naar de gewenste plaatsnaam gaan zoeken door een paar letters te typen, zoals 'col'.  Nadat u ophoudt met typen, wordt de lookup automatisch geopend. De lijst is gefilterd op plaatsnamen die beginnen met 'col'. 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

De cursor bevindt zich op dit moment nog steeds in het zoekveld. Als u doorgaat met typen zodat de waarde 'colum' is, wordt de inhoud van de lookup automatisch aangepast aan de meest recente waarde in het besturingselement. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Hoewel het lookup-besturingselement nog steeds de focus heeft, u kunt ook met de toetsen **pijl-omhoog** of **pijl-omlaag** de rij markeren die u wilt selecteren. Als u op **Enter** drukt, wordt de gemarkeerde rij geselecteerd uit de lookup en de waarde van het besturingselement wordt bijgewerkt. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Meer invoeren dan id's
Bij het invoeren van gegevens proberen gebruikers een entiteit (zoals een klant of leverancier) eerder op naam te vinden dan via een id die de entiteit vertegenwoordigt. In de huidige versie van Finance and Operations kan in vele (maar niet alle) lookups ook contextuele informatie worden ingevoerd. Met deze krachtige functie kan de gebruiker nu kiezen of hij de id of de bijbehorende naam in het besturingselement invoert. 

Neem bijvoorbeeld het veld **Klantaccount** bij het maken van een verkooporder. Dit veld bevat de **Account-id** van de klant, maar een gebruiker zou in dit veld meestal liever een **Accountnaam** invoeren in plaats van een **Account-id** bij het maken van een verkooporder, zoals 'Forest Wholesales' in plaats van 'US-003.'

Als de gebruiker begint met het invoeren van een **Account-id** in het lookup-besturingselement, wordt de vervolgkeuzelijst automatisch geopend zoals beschreven in de vorige sectie. De gebruiker ziet de lookup zoals hieronder weergegeven.

[![Contextuele lookup wanneer een account-id wordt ingevoerd.](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

De gebruiker kan nu echter ook het begin van een **Accountnaam** invoeren. Als dit wordt gedetecteerd, ziet de gebruiker de volgende lookup. Merk op hoe de kolom **Naam** is verplaatst naar de eerste kolom in de lookup en hoe de lookup is gesorteerd en gefilterd op basis van de kolom **Naam**.

[![Contextuele lookup wanneer een klantnaam wordt ingevoerd.](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Rasterkolomkoppen gebruiken voor geavanceerd filteren en sorteren
De lookup-verbeteringen die in de voorgaande twee secties zijn besproken, maken het de gebruiker aanzienlijk makkelijker om door rijen in een lookup te bladeren op basis van een zoekopdracht 'begint met' voor de velden **Id** of **Naam** in de lookup. Er zijn echter situaties waarin meer geavanceerde filteren (of sorteren) nodig is om de juiste rij te vinden. In dergelijke situaties moet de gebruiker de opties voor filteren en sorteren in de rasterkolomkoppen in de lookup gebruiken. Stel dat een werknemer een verkooporderregel invoert en als product de juiste 'cable' moet vinden. Het woord 'cable' invoeren in het besturingselement voor **Artikelnummer** is niet zo handig, omdat er geen productnamen zijn die beginnen met 'cable'. 

![legeartikellookup](./media/emptyitemlookup.png) 

In plaats daarvan moet de gebruiker de waarde in het lookup-besturingselement wissen, de lookup-vervolgkeuzelijst openen en filteren met behulp van de rasterkolomkop, zoals hieronder weergegeven. Een gebruiker met muis of touchscreen kan elke kolomkop aanklikken of aantikken om de filter- en sorteeropties voor die kolom te openen. Een gebruiker die een toetsenbord gebruikt, moet de toetscombinatie **Alt**+**pijl****-omlaag** nog een keer indrukken. De focus wordt nu  naar de vervolgkeuzelijst verplaatst, waarna de gebruiker de juiste kolom kan selecteren. Als hij dan **Ctrl**+**G** indrukt, wordt de vervolgkeuzelijst van de rasterkolomkop geopend. 

[![rasterfilterartikellookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Nadat het filter is toegepast (zie de onderstaande afbeelding), kan de gebruiker de rij zoals gebruikelijk zoeken en selecteren. 

![gefilterdartikellookup](./media/filtereditemlookup.png)




