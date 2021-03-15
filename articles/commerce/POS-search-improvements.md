---
title: Zoekfunctie voor producten en klanten op het verkooppunt (POS)
description: Dit onderwerp biedt een overzicht van verbeteringen die zijn aangebracht in de functies voor het zoeken van producten en klanten in Dynamics 365 Commerce.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 1de8373471ff8187bd476305c9ed0b26beaa52d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965273"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Zoekfunctie voor producten en klanten op het verkooppunt (POS)

[!include [banner](includes/banner.md)]

MPOS (Modern Point of Sale) en CPOS (Cloud Point of Sale) bieden een gebruiksvriendelijke zoekfunctie voor producten en klanten. Omdat de zoekbalk altijd aanwezig is boven aan MPOS- en CPOS-vensters, kunnen medewerkers snel producten en klanten opzoeken.

Werknemers kunnen zoeken naar producten in de assortimenten en catalogi die zijn gekoppeld aan de huidige winkel. Ze kunnen ook zoeken in de assortimenten en catalogi die zijn gekoppeld aan alle andere winkels van het bedrijf. Kassamedewerkers kunnen dus producten buiten het winkelassortiment verkopen en retourneren. Op dezelfde wijze kunnen medewerkers zoeken naar klanten die zijn gekoppeld aan de huidige winkel of een andere winkel in het bedrijf. Daarnaast kunnen medewerkers zoeken naar klanten die zijn gekoppeld aan een ander bedrijf in de bovenliggende organisatie.

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
- Voor zoekopdrachten met meerdere zoekwoorden (zoekopdrachten met zoektermen) kunnen detailhandelaren configureren of de zoekresultaten resultaten bevatten die overeenkomen met *een* van de zoektermen of alleen resultaten die overeenkomen met *alle* zoektermen. De instelling voor deze functionaliteit is beschikbaar in het POS-functionaliteitsprofiel, in een nieuwe groep met de naam **Product zoeken**. De standaardinstelling is **Overeenkomen met willekeurige zoekterm(en)**. Deze instelling is ook de aanbevolen instelling. Wanneer de instelling **Overeenkomen met willekeurige zoekterm(en)** wordt gebruikt, worden alle producten die geheel of gedeeltelijk overeenkomen met de een of meer zoektermen geretourneerd als resultaat. Deze resultaten worden automatisch gesorteerd in oplopende volgorde met producten die de meeste trefwoordovereenkomsten (volledig of gedeeltelijk) hebben.

    De instelling **Overeenkomen met alle zoektermen** retourneert alleen producten die overeenkomen met alle zoektermen (volledig of gedeeltelijk). Deze instelling is handig voor lange productnamen en als werknemers niet te veel zoekresultaten willen krijgen. Dit type zoekopdracht heeft echter twee beperkingen:

    - De zoekopdracht wordt uitgevoerd op afzonderlijke producteigenschappen. Zo worden alleen producten geretourneerd die alle gezochte zoekwoorden in ten minste één producteigenschap bevatten.
    - Dimensies worden niet doorzocht.

- Detailhandelaren kunnen productzoekopdrachten nu zo configureren dat zoeksuggesties worden weergeven terwijl gebruikers productnamen typen. Er is een nieuwe instelling beschikbaar in het POS-functionaliteitsprofiel, in een nieuwe groep met de naam **Product zoeken**. De instelling heet **Suggesties weergeven tijdens het typen**. Met deze functionaliteit kunnen werknemers het product dat ze zoeken snel vinden omdat ze niet de hele naam handmatig hoeven in te voeren.
- Met het algoritme voor het zoeken van producten wordt nu ook gezocht naar de gezochte termen in de eigenschap **Zoeknaam** van het product.

![Productsuggesties](./media/Productsuggestions.png "Productsuggesties")

## <a name="customer-search"></a>Klant zoeken

Klantzoekopdrachten worden gebruikt om voor verschillende doeleinden naar klanten te zoeken. Een kassamedewerker kan bijvoorbeeld de wensenlijst of inkoophistorie weergeven of de klant aan een transactie toevoegen. Het zoekalgoritme komt overeen met de zoektermen met de waarden die aanwezig zijn in de volgende klanteigenschappen:

- Naam
- E-mailadres
- Telefoonnummer
- Nummer loyaliteitskaart
- Adres
- Rekeningnummer

Onder deze eigenschappen biedt de naam de meeste flexibiliteit voor zoekopdrachten met meerdere trefwoorden omdat het algoritme alle klanten retourneert die overeenkomen met een van de gezochte trefwoorden. De klanten die overeenkomen met de meeste zoekwoorden, worden bovenaan weergegeven in de resultaten. Dit is handig voor kassamedewerkers in situaties waarin ze zoeken door de volledige naam te typen, maar de achternaam en voornaam zijn omgewisseld tijdens de eerste gegevensinvoer. Met het oog op de prestaties behouden alle andere eigenschappen echter de volgorde van de zoekwoorden. Als de volgorde van de zoekwoorden niet overeenkomt met de volgorde waarin de gegevens zijn opgeslagen, worden er dus geen resultaten geretourneerd.

Standaard wordt een klantzoekopdracht uitgevoerd op de klantadresboeken die zijn gekoppeld aan de winkel. Dit type zoekopdracht wordt ook wel een *lokale klantzoekopdracht* genoemd. Werknemers kunnen echter ook wereldwijd naar klanten zoeken. Ze kunnen dus in alle winkels van het bedrijf en in alle andere rechtspersonen zoeken. Dit type zoekopdracht wordt ook wel een *externe klantzoekopdracht* genoemd.

Als werknemers wereldwijd willen zoeken, selecteren ze de knop **Resultaten filteren** onder aan de pagina en vervolgens de optie **Alle winkels zoeken**, zoals in de volgende afbeelding. In dit geval worden niet alleen klanten geretourneerd. Alle typen partijen die deel uitmaken van een adresboek in het hoofdkantoor worden ook geretourneerd. Dit kunnen werknemers, leveranciers, contactpersonen en concurrenten zijn.

> [!NOTE]
> Voor een externe klantzoekopdracht moeten minstens vier tekens worden ingevoerd om resultaten te retourneren.

Bij een externe klantzoekopdracht wordt de klant-ID niet weergegeven voor klanten uit de andere rechtspersonen omdat er geen klant-ID voor die partijen is gemaakt in het huidige bedrijf. Als een werknemer de pagina met klantgegevens opent, wordt automatisch een klant-ID voor de partij gegenereerd en worden de klantadresboeken van de winkel gekoppeld aan de klant. Daarom is de klant zichtbaar in lokale winkelzoekopdrachten die later worden uitgevoerd.

![Algemene zoekopdracht voor klant](./media/Globalcustomersearch.png "Algemene zoekopdracht voor klant")

### <a name="enhancements-to-local-customer-search"></a>Verbeteringen in lokale klantzoekopdracht

Zoekopdrachten die zijn gebaseerd op het telefoonnummer zijn vereenvoudigd. Deze zoekopdrachten negeren nu speciale tekens, zoals spaties, afbreekstreepjes en haken, die mogelijk zijn toegevoegd wanneer de klant is gemaakt. Daarom kunnen kassiers de indeling negeren van het telefoonnummer dat ze zoeken. Als een telefoonnummer van een klant bijvoorbeeld is ingevoerd als **123-456-7890**, kan een kassamedewerker de klant zoeken door **1234567890** te typen of door de eerste paar cijfers van het telefoonnummer in te voeren.

> [!NOTE]
> Een klant kan meerdere telefoonnummers en meerdere e-mailadressen hebben. Het klantzoekalgoritme doorzoekt ook deze secundaire e-mailadressen en telefoonnummers, maar de primaire e-mail en het telefoonnummer worden alleen weergegeven op de pagina met klantzoekresultaten. Dit kan leiden tot verwarring omdat de geretourneerde klantresultaten niet het gezochte e-mailadres of telefoonnummer weergeven. In een toekomstige versie gaan we het scherm met klantzoekresultaten verbeteren om deze gegevens weer te geven.

De traditionele zoekopdracht voor klanten kan tijdrovend zijn, omdat er meerdere velden worden doorzocht. Kassiers kunnen in plaats daarvan nu zoeken in één klanteigenschap, zoals de naam, het e-mailadres of het telefoonnummer. De eigenschappen waarvan het klantzoekalgoritme gebruikmaakt, staan bekend als de *klantzoekcriteria*. De systeembeheerer kan eenvoudig een of meer criteria configureren als snelkoppelingen die op het POS worden weergegeven. Omdat de zoekactie is beperkt tot één criteriu, worden alleen de relevante zoekresultaten weergegeven en zijn de prestaties veel beter dan met de standaard zoekopdracht voor klanten. In de volgende afbeelding ziet u de snelkoppelingen voor klant zoeken op het POS.

![Snelkoppelingen voor zoeken naar klant](./media/SearchShortcutsPOS.png "Snelkoppelingen voor zoeken naar klant")

Voor het instellen van zoekcriteria als snelkoppelingen moet de beheerder de pagina **Commerce-parameters** in Commerce openen en vervolgens op het tabblad **POS-zoekcriteria** klikken en alle criteria selecteren die moeten worden weergegeven als snelkoppelingen.

![Snelkoppelingen voor zoeken configureren](./media/ConfigureShortcutsAX.png "Snelkoppelingen voor zoeken configureren")

> [!NOTE]
> Als u te veel snelkoppelingen toevoegt, wordt de vervolgkeuzelijst op de zoekbalk in POS onoverzichtelijk wat een negatieve invloed heeft op de zoekodprachten van werknemers. Het is raadzaam alleen snelkoppelingen toe te voegen die u nodig hebt.

Het veld **Weergavevolgorde** bepaalt de volgorde waarin de snelkoppelingen worden weergegeven op het POS. De getoonde criteria zijn standaardeigenschappen die het klantzoekalgoritme gebruikt om klanten te zoeken. Partners kunnen echter aangepaste eigenschappen toevoegen als snelkoppelingen. Als u aangepaste eigenschappen als snelkoppelingen wilt toevoegen, moet de systeembeheerder de uitbreidbare opsomming (enum) die wordt gebruikt voor de klantzoekcriteria uitbreiden en de aangepaste eigenschappen van de partner als snelkoppelingen opgeven. Partners zijn verantwoordelijk voor het schrijven van de code voor het zoeken van resultaten wanneer aangepaste sneltoetsen worden gebruikt voor zoekopdrachten.

> [!NOTE]
> Een aangepaste eigenschap die wordt toegevoegd aan de enum heeft geen invloed op het standaardzoekalgoritme voor klanten. Het klantzoekalgoritme zoekt dus niet in de aangepaste eigenschap. Gebruikers kunnen alleen een aangepaste eigenschap gebruiken voor zoekopdrachten als die aangepaste eigenschap is toegevoegd als een snelkoppeling of als het standaardzoekalgoritme is overschreven.

In een aanstaande release van Commerce kunnen detailhandelaren de standaardzoekmodus voor klanten in POS instellen op **In alle winkels zoeken**. Deze configuratie kan handig zijn in scenario's waar klanten die buiten POS zijn gemaakt onmiddellijk moeten worden doorzocht (bijvoorbeeld zelfs voordat de distributietaak wordt uitgevoerd). De nieuwe optie **Standaardzoekmodus voor klanten** is beschikbaar in het POS-functionaliteitsprofiel. Stel deze optie in op **Aan** om de standaardzoekmodus in te stellen op **In alle winkels zoeken**. Bij elke zoekpoging van klanten wordt vervolgens een realtime aanroep naar het hoofdkantoor uitgevoerd.

Om onverwachte problemen met prestaties te voorkomen, wordt deze configuratie verborgen achter een flighting-markering met de naam **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Als de instelling **Standaardzoekmodus voor klanten** in de gebruikersinterface moet worden weergegeven, moet de detailhandelaar dus een ondersteuningsticket maken voor de UAT- (User Acceptance Testing) en productieomgevingen. Nadat het ticket is ontvangen, werkt het technisch team samen met de detailhandelaar om ervoor te zorgen dat de detailhandelaar de tests uitvoert in de niet-productieomgeving om de prestaties te beoordelen en eventuele vereiste optimalisaties te implementeren.



[!INCLUDE[footer-include](../includes/footer-banner.md)]