---
title: Producten en klanten zoeken in POS
description: Dit onderwerp biedt een overzicht van verbeteringen die zijn aangebracht in de functies voor het zoeken van producten en klanten in Dynamics 365 for Retail.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5f6f9a02b20549a75941d367c1b46e3439360078
ms.contentlocale: nl-nl
ms.lasthandoff: 01/19/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Overzicht van zoekfunctie voor producten en klanten in Point of Sale

[!include[banner](includes/banner.md)]

MPOS (Modern Point of Sale) en CPOS (Cloud Point of Sale) bieden een gebruiksvriendelijke zoekfunctie waarmee winkelpersoneel snel producten en klanten kan vinden. De zoekbalk is altijd aanwezig in MPOS en CPOS, zodat medewerkers snel producten en klanten kunnen opzoeken.

Medewerkers kunnen zoeken naar producten in de assortimenten en catalogi die zijn gekoppeld aan de huidige winkel en de assortimenten en catalogi die zijn gekoppeld aan andere winkels in het bedrijf. Kassamedewerkers kunnen dus producten buiten het winkelassortiment verkopen en retourneren. Op dezelfde wijze kunnen medewerkers zoeken naar klanten die zijn gekoppeld aan de huidige winkel of een andere winkel in het bedrijf. Daarnaast kunnen medewerkers zoeken naar klanten die zijn gekoppeld aan een ander bedrijf in de bovenliggende organisatie.

## <a name="product-search"></a>Artikel zoeken 

Standaard wordt in het assortiment van de winkel naar een product gezocht. Dit type zoekopdracht wordt ook wel een *lokale productzoekopdracht* genoemd. Werknemers kunnen echter gemakkelijk overschakelen naar een catalogus die is gekoppeld aan de huidige winkel of zoeken in een andere winkel. Dit type zoekopdracht wordt ook wel een *externe productzoekopdracht* genoemd. Als u de catalogus wilt wijzigen, selecteert u de knop **Categorieën** links op de pagina. Selecteer boven in het venster dat verschijnt de knop **Catalogus wijzigen** en selecteer vervolgens een van de beschikbare catalogi. De geselecteerde catalogus wordt doorzocht op producten.

Op de pagina **Catalogus wijzigen** kunnen werknemers eenvoudig een winkel selecteren of in alle winkels naar producten zoeken.

![De catalogus wijzigen](./media/Changecatalog.png "De catalogus wijzigen")
 
Met een lokale productzoekopdracht wordt gezocht in de volgende producteigenschappen:

- Productnummer
- Productnaam
- Omschrijving
- Dimensies
- Streepjescode
- Zoeknaam

### <a name="enhancements-to-local-product-searches"></a>Verbeteringen in lokale productzoekopdrachten

Lokale productzoekopdrachten zijn nu gebruiksvriendelijker. De volgende verbeteringen zijn doorgevoerd:

- Er zijn vervolgkeuzelijsten voor producten en klanten toegevoegd aan de zoekbalk, zodat werknemers **Product** of **Klant** kunnen selecteren voordat ze de zoekopdracht uitvoeren. Standaard is **Product** geselecteerd, zoals in de volgende afbeelding wordt weergegeven.
- Voor zoekopdrachten met meerdere zoekwoorden (zoekopdrachten met zoektermen) kunnen detailhandelaren configureren of de zoekresultaten resultaten bevatten die overeenkomen met een van de zoektermen of alleen resultaten die overeenkomen met alle zoektermen. Deze instelling is beschikbaar in het POS-functionaliteitsprofiel, onder een nieuwe groep met de naam **Product zoeken**. De standaardinstelling is **Overeenkomen met willekeurige zoekterm(en)**. Deze instelling is ook de aanbevolen instelling. Wanneer de instelling **Overeenkomen met willekeurige zoekterm(en)** wordt gebruikt, worden alle producten die geheel of gedeeltelijk overeenkomen als resultaten geretourneerd en worden de resultaten automatisch in oplopende volgorde weergegeven waarbij als eerste de producten met de meeste overeenkomende zoekwoorden (volledig of gedeeltelijk) worden weergegeven.

    De instelling **Overeenkomen met alle zoektermen** retourneert alleen producten die overeenkomen met alle zoektermen (volledig of gedeeltelijk). Deze instelling is handig voor lange productnamen en als werknemers niet te veel zoekresultaten willen krijgen. Dit type zoekopdracht heeft echter twee beperkingen:

    - De zoekopdracht wordt uitgevoerd op afzonderlijke producteigenschappen. Zo worden alleen producten geretourneerd die alle gezochte zoekwoorden in ten minste één producteigenschap bevatten.
    - Dimensies worden niet doorzocht.

- Detailhandelaren kunnen productzoekopdrachten nu zo configureren dat zoeksuggesties worden weergeven terwijl gebruikers productnamen typen. Er is een nieuwe instelling beschikbaar in het POS-functionaliteitsprofiel, onder een nieuwe groep met de naam **Product zoeken**. De instelling heet **Suggesties weergeven tijdens het typen**. Met deze functionaliteit kunnen werknemers het product dat ze zoeken snel vinden omdat ze niet de hele naam handmatig hoeven in te voeren.
- Met het algoritme voor het zoeken van producten wordt nu ook gezocht naar de gezochte termen in de eigenschap **Zoeknaam** van het product.

![Productsuggesties](./media/Productsuggestions.png "Productsuggesties")

## <a name="customer-search"></a>Klant zoeken

Klantzoekopdrachten worden gebruikt om voor verschillende doeleinden naar klanten te zoeken. Een kassamedewerker kan bijvoorbeeld de wensenlijst of inkoophistorie weergeven of de klant aan een transactie toevoegen. In het geval van zoekopdrachten met meerdere trefwoorden, retourneert het zoekalgoritme voor klanten alle klanten die overeenkomen met een van de gezochte zoekwoorden. De klanten die overeenkomen met de meeste zoekwoorden, worden echter bovenaan weergegeven in de resultaten. Dit gedrag komt overeen met de manier waarop in andere zoekmachines resultaten worden weergegeven. Eerst worden de resultaten weergegeven die overeenkomen met het grootste aantal gezochte termen en vervolgens worden de resultaten weergegeven die gedeeltelijk overeenkomen met de zoekwoorden. Dit gedrag helpt kassamedewerkers in situaties waarin ze voor hun zoekopdracht meerdere zoekwoorden gebruiken, maar een van de zoekwoorden een spelfout bevat.

Standaard wordt een klantzoekopdracht uitgevoerd op de klantadresboeken die zijn gekoppeld aan de winkel. Dit type zoekopdracht wordt ook wel een *lokale klantzoekopdracht* genoemd. Werknemers kunnen echter ook wereldwijd naar klanten zoeken. Ze kunnen dus in alle winkels van het bedrijf en in alle andere rechtspersonen zoeken. Dit type zoekopdracht wordt ook wel een *externe klantzoekopdracht* genoemd.

Als werknemers wereldwijd willen zoeken, selecteren ze de knop **Resultaten filteren** onder aan de pagina en vervolgens de optie **Alle winkels zoeken**, zoals in de volgende afbeelding. In dit geval worden niet alleen klanten geretourneerd. Alle typen partijen die deel uitmaken van een adresboek in het hoofdkantoor worden ook geretourneerd. Dit kunnen werknemers, leveranciers, contactpersonen en concurrenten zijn.

> [!NOTE]
> Voor een externe klantzoekopdracht moeten minstens vier tekens worden ingevoerd om resultaten te retourneren.

Bij een externe klantzoekopdracht wordt de klant-ID niet weergegeven voor klanten uit de andere rechtspersonen omdat er geen klant-ID voor die partijen is gemaakt in het huidige bedrijf. Als een werknemer de pagina met klantgegevens opent, wordt automatisch een klant-ID voor de partij gegenereerd en worden de klantadresboeken van de winkel gekoppeld aan de klant. Daarom is de klant zichtbaar in lokale winkelzoekopdrachten die later worden uitgevoerd.

![Wereldwijde klantzoekopdracht](./media/Globalcustomersearch.png "Wereldwijde klantzoekopdracht")

### <a name="enhancements-to-local-customer-searches"></a>Verbeteringen in lokale klantzoekopdrachten

Met lokale klantzoekopdrachten kunnen werknemers klanten snel vinden op telefoonnummer. Werknemers hoeven geen speciale tekens te typen die zijn toegevoegd aan het telefoonnummer van een klant, zoals spaties, koppeltekens of haken. Hoewel kassamedewerkers telefoonnummers kunnen opslaan in elke indeling (ze kunnen bijvoorbeeld haken, koppeltekens, symbolen en dergelijke opnemen), kunnen ze klanten zoeken door een gedeeltelijk telefoonnummer te typen. Als een kassamedewerker speciale tekens heeft gebruikt bij het invoeren van een telefoonnummer, kunnen andere kassamedewerkers de klant vinden door de cijfers te typen die worden weergegeven na de speciale tekens. Als een telefoonnummer van een klant bijvoorbeeld is ingevoerd als **123-456-7890**, kan een kassamedewerker de klant zoeken door **123**, **456**, **7890** of **1234567890** te typen of door de eerste paar cijfers van het telefoonnummer in te voeren.

