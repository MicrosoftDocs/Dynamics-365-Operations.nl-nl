---
title: Zoekopdrachten gebruiken om informatie te vinden
description: In Microsoft Dynamics 365 voor bewerkingen hebben veel velden zoekopdrachten waarmee u gemakkelijk de juiste of de gewenste waarde te vinden. Enkele verbeteringen zijn toegevoegd aan de zoekopdrachten die deze besturingselementen beter bruikbaar maken en gebruikers productiever. In dit onderwerp vindt u informatie over deze nieuwe functies voor zoeken en handige tips voor een optimaal gebruik uit zoekopdrachten informatie in het systeem zal ontvangen.
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Zoekopdrachten gebruiken om informatie te vinden

In Microsoft Dynamics 365 voor bewerkingen hebben veel velden zoekopdrachten waarmee u gemakkelijk de juiste of de gewenste waarde te vinden. Enkele verbeteringen zijn toegevoegd aan de zoekopdrachten die deze besturingselementen beter bruikbaar maken en gebruikers productiever. In dit onderwerp vindt u informatie over deze nieuwe functies voor zoeken en handige tips voor een optimaal gebruik uit zoekopdrachten informatie in het systeem zal ontvangen.  

<a name="responsive-lookups"></a>Reageert zoekopdrachten
------------------

Een gebruiker moet een expliciete actie ondernemen om te openen van het vervolgkeuzemenu in vorige versies van Dynamics 365 voor bewerkingen die interactie met een besturingselement van een zoekopdracht. Dit kan zijn door een sterretje (\*) in het besturingselement voor het filteren van de zoekopdracht op basis van de huidige waarde van het besturingselement te klikken op de vervolgkeuzepijl of via de **Alt**+**pijl-omlaag** sneltoets. Zoeken controleert zijn gewijzigd in de volgende manieren om beter te stemmen aan de geldende web gebruiken:

-   Vervolgkeuzelijsten zoeken opent nu automatisch na een geringe pauze in te typen, met de vervolgkeuzelijst menu inhoud gefilterd op basis van de waarde van het besturingselement zoeken.
    -   Houd er rekening mee dat het oude gedrag van de vervolgkeuzelijst automatisch openen na het typen van een sterretje (\*) is afgeschaft.
-   Nadat de vervolgkeuzelijst Zoeken is geopend, gebeurt het volgende:
    -   De cursor blijft staan in het besturingselement zoeken (in plaats van de focus verplaatsen naar de vervolgkeuzelijst) zodat u kunt nog wijzigingen aanbrengen in de waarde van het besturingselement. De gebruiker kan echter nog steeds gebruiken de **pijl-omhoog** en **pijl-omlaag** voor het wijzigen van rijen in de vervolgkeuzelijst en voer om de huidige rij in de vervolgkeuzelijst selecteren.
    -   De inhoud van de vervolgkeuzelijst wordt aangepast nadat alle wijzigingen zijn aangebracht in de waarde van het besturingselement zoeken.

Stel dat u een opzoekveld genoemd **plaats**. 

Wanneer de focus zich in de **plaats** veld, kunt u beginnen met zoeken naar de plaats die u wilt dat door een paar letters, zoals 'KOL'.  Nadat u stoppen met typen, wordt de zoekactie automatisch geopend, worden deze steden die met 'kol beginnen'. 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

De cursor zich op dit moment nog steeds in het zoekveld. Als u verder typen zodat de waarde 'kolom' is, wordt de inhoud van de zoekopdracht automatisch aangepast zodat de laatste waarde in het besturingselement. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Hoewel nog steeds in het zoekveld besturingselement de focus heeft, u kunt ook de **pijl-omhoog** of **pijl-omlaag** sleutels markeren van de rij die u wilt selecteren. Als u drukt op **Enter** in de gemarkeerde rij wordt geselecteerd uit de zoekopdracht en de waarde van het besturingselement wordt bijgewerkt. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Typen in meer dan de id 's
Wanneer u gegevens invoert, is het natuurlijke voor gebruikers proberen om een entiteit, zoals een klant of leverancier in de vorm van de naam in plaats van een id voor de entiteit te identificeren. In de huidige versie van Dynamics 365 for Operations nu toestaan contextgevoelige gegevensinvoer veel (maar niet alle) zoekopdrachten. Deze krachtige functie kan de gebruiker typt u de ID of de bijbehorende naam in het besturingselement zoeken. 

Stel de **klantrekening** veld bij het maken van een verkooporder. Dit veld bevat de **Account-ID** voor de klant, maar een gebruiker meestal liever Voer een **rekeningnaam** in plaats van een **Account-ID** voor dit veld bij het maken van een verkooporder, zoals 'Forest Wholesales' in plaats van 'Amerikaanse-003.'

Als de gebruiker is begonnen in te voeren een **Account-ID** in het besturingselement zoeken in de vervolgkeuzelijst zou automatisch openen zoals beschreven in de vorige sectie en de gebruiker ziet de zoekopdracht zoals hieronder wordt weergegeven.

[![Contextuele opzoeken wanneer een klantrekening-ID wordt ingevoerd.](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

De gebruiker kan echter ook nu invoeren het begin van een **rekeningnaam** ook. Als dit wordt gevonden, ziet de gebruiker de volgende zoekopdracht. Voorafgaande kennisgeving hoe de **naam** kolom wordt verplaatst naar de eerste kolom in de zoekopdracht worden en hoe de zoekopdracht wordt gesorteerd en gefilterd op basis van de **naam** kolom.

[![Contextuele opzoeken wanneer de naam van een klant wordt ingevoerd.](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Met behulp van de kolomkoppen raster voor geavanceerdere filteren en sorteren
De zoekopdracht verbeteringen besproken in de voorgaande twee secties aanzienlijk beter een gebruiker navigeert de rijen in een zoekopdracht op basis van een zoekopdracht 'begint met' van de **ID** of **naam** veld in de zoekopdracht. Er zijn echter situaties waarin meer geavanceerde filter (of sorteren) nodig is om de juiste rij te zoeken. In dergelijke situaties moet de gebruiker de opties voor filteren en sorteren in het raster kolomkoppen in de zoekopdracht gebruiken. Stel dat een werknemer invoeren van een verkooporderregel die nodig zijn voor het zoeken naar rechts 'kabel' als het product. Typ 'kabel' in de **artikelnummer** besturingselement is handig, niet als er geen productnamen die beginnen met 'kabel'. 

![emptyitemlookup](./media/emptyitemlookup.png) 

In plaats daarvan moet de gebruiker wist u de waarde van het besturingselement voor zoeken en opent u de vervolgkeuzelijst zoeken, filteren met behulp van de kolomkop raster vervolgkeuzemenu zoals hieronder wordt weergegeven. Een gebruiker muis (of contact) kunt gewoon klik (of touch) een kolomkop voor toegang tot het filteren en sorteren van de opties voor die kolom. Voor een gebruiker toetsenbord moet de gebruiker gewoon drukt u op **Alt**+**omlaag****pijl** nogmaals om focus te verplaatsen in de vervolgkeuzelijst, waarna de gebruiker kan met tab naar de juiste kolom, en druk vervolgens op **Ctrl**+**G** voor het openen van het raster vervolgkeuzelijst kolomkopmenu. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Nadat het filter is toegepast (Zie de onderstaande afbeelding), kan de gebruiker kan zoeken en selecteer de rij zoals gebruikelijk. 

![filtereditemlookup](./media/filtereditemlookup.png)


