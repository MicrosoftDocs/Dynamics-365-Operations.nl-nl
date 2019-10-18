---
title: Callcentercatalogi
description: In dit onderwerp wordt de callcenterspecifieke functionaliteit voor catalogi in Dynamics 365 Retail beschreven.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2ad50be1394daf5bffa6391d2f56340aad14120b
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023654"
---
# <a name="call-center-catalogs"></a>Callcentercatalogi

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de callcenterspecifieke functionaliteit beschreven die is gekoppeld aan de catalogusmogelijkheden in Dynamics 365 Retail.

De catalogusfuncties van Retail kunnen worden gebruikt voor meerdere doeleinden. De catalogusfuncties zijn in eerste instantie gemaakt ter ondersteuning van e-commerce-integraties van derden. Met catalogusinstelling konden bedrijven een groepering van producten en kenmerken maken die extern kunnen worden gepubliceerd voor gebruik door een e-commerceoplossing van derden.

Toen ondersteuning van callcenterkanalen werd toegevoegd aan Retail, werd het catalogusconcept uitgebreid met extra mogelijkheden ter ondersteuning en beheer van functies die gerelateerd zijn aan traditionele consumentenmarketingcatalogi. Een direct-to-consumer bedrijf produceert vaak afgedrukte catalogi die dan naar een of meer klantensegmenten worden verzonden. Deze catalogussen hebben meestal bepaalde acties of aanbiedingen die alleen worden gehonoreerd als de klant een catalogusidentificatiecode verstrekt op het moment van maken van de order.

Direct-to-consumer marketingbedrijven zijn zeer gericht op het bijhouden van het antwoord op deze catalogi om ervoor te zorgen dat de kosten van productie en verzending ervan gerechtvaardigd zijn. Voor het bijhouden van de reactie wordt traditioneel een code op de achterzijde van de catalogus afgedrukt en deze code wordt dan gevraagd en toegepast wanneer de catalogusontvanger belt om een order via de telefoon te plaatsen (of nu meer traditioneel kan de code worden ingevoerd wanneer de klant een order online plaatst). Er zijn verschillende branchetermen voor het identificeren van deze catalogustrackingcode (inclusief sleutelcode, promotiecode, cataloguscode, broncode), maar we noemen de code in Retail de **Broncode-ID**.

## <a name="basic-catalog-setup"></a>Basiscatalogusinstelling

Ga naar **Detailhandel** \> **Catalogi en assortimenten** \> **Alle catalogussen** voor het configureren van uw catalogus.

Wanneer u een nieuwe catalogus maakt, moet u eerst de catalogus koppelen aan een of meer detailhandelkanalen. Dit gebeurt op het sneltabblad **Detailhandelkanalen** op het formulier **Catalogusinstelling**. Klik op **Toevoegen** en selecteer een of meer detailhandelkanalen. Alleen artikelen die zijn gekoppeld aan uw geselecteerde kanaal[assortimenten](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments) kunnen worden gebruikt bij het maken van de catalogus.

Om producten toe te voegen aan een catalogus moet een navigatiehiërarchie worden gekozen. De navigatiehiërarchie ondersteunt de categoriestructuur van de catalogus. U moet kiezen uit een van de navigatiehiërarchieën die zijn gekoppeld aan de detailhandelkanalen die zijn geselecteerd op het sneltabblad **Detailhandelkanalen** van de pagina **Catalogus**. Als een navigatiekanaal niet eerder was gekoppeld aan een kanaal, gaat u naar **Detailhandel** \> **Afzetkanaalinstellingen** \> **Afzetkanaalcategorieën en productkenmerken** om een standaard navigatiehiërarchie te koppelen aan elk van uw detailhandelkanalen.

Klik op het menutabblad **Catalogi** op de pagina **Catalogusinstelling** op **Producten toevoegen** om de producten te configureren die u aan de catalogus wilt toevoegen, of selecteer een knooppunt in de navigatiehiërarchie (als u een knooppunt selecteert, verandert de schermpresentatie en kunt u producten direct aan een categorie in de catalogus toevoegen).

Klik op het bovenste knooppunt van de catalogushiërarchie om terug te keren naar de hoofdkoptekstweergave van de catalogus. Benodigde ingangsdatums en vervaldatums configureren op het sneltabblad **Algemeen**.

Voordat de catalogus beschikbaar is voor gebruik, moet deze worden gepubliceerd. Klik op **Catalogus valideren** in het menu **Catalogi** om een validatie te verwerken. Dit is een vereiste actie en valideert dat de vereiste instelling klopt. Klik op **Resultaten weergeven** om de details van de validatie te zien. Als er fouten zijn gevonden, moet u de gegevens corrigeren en de validatie opnieuw uitvoeren totdat de validatie slaagt.

Nadat de validatie is bevestigd, klikt u op **Werkstroom** in het menu om de goedkeuringswerkstroom te starten. Klik op **Indienen** in het menu **Werkstroom** om de procedure uit te voeren. Configureer de stappen en gemachtigde gebruikers voor de werkstroom vanuit **Detailhandel** \> **Instelling van hoofdkantoor** \> **Detailhandelworkflows**. De werkstroom definieert de stappen die nodig zijn om de catalogus de status **Goedgekeurd** te geven. Wanneer de catalogus de status **Goedgekeurd** heeft, kunt u klikken op de optie **Publiceren** in het menu **Catalogus** om de procedure te voltooien. Nadat de catalogus de status **Gepubliceerd** heeft gekregen, kan deze worden gebruikt bij callcenterorderinvoer en catalogusverzendprocessen.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Catalogi gebruiken voor verkooporderprijzen en promoties

Een belangrijke reden om een catalogus te definiëren voor gebruik met een callcenter is specifieke prijzen en promoties voor die catalogus te kunnen configureren. Klanten die uit deze catalogus bestellen, ontvangen deze prijzen en promoties bij callcenterorderinvoer als de **Broncode-ID** van de catalogus wordt toegepast op de orderkop of -regels.

Als u specifieke catalogusprijzen wilt configureren, selecteert u de optie **Prijsgroepen** op het tabblad **Catalogi** om een of meer prijsgroepen te koppelen aan de catalogus. Alle handelsovereenkomsten, prijscorrectiejournalen en geavanceerde detailhandelskortingen (drempel, hoeveelheid, combinatie) die zijn gekoppeld aan dezelfde prijsgroep worden toegepast wanneer klanten uit deze catalogus bestellen.

Klik op het tabblad **Broncodes** op **Toevoegen** om een of meer **Broncode-ID's** toe te voegen aan deze catalogus. Dit is de code die tijdens callcenterorderinvoer wordt toegepast op de verkooporderkop (en -regels). Deze code wordt gebruikt om de verkooporder te koppelen aan de catalogus en uiteindelijk aan de prijsgroepen en speciale prijzen en promoties die zijn geconfigureerd.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>De bron-ID gebruiken voor het bijhouden van kosten en responspercentages

Wanneer u de **Broncode-ID** definieert, kunt u desgewenst deze ID koppelen aan een **Doelmarkt-id**. De **doelmarkt-id** kan worden gedefinieerd in **Detailhandel** \> **Klanten** \> **Doelmarkt**. De doelmarkt is een lijst met klanten en/of potentiële klanten die tot een door de gebruiker gedefinieerd segment behoren. Door de gegevens van klanten of potentiële klanten te koppelen aan de broncode-ID ontstaat betere zichtbaarheid van ontvangers van de catalogus. Als een klant is gekoppeld aan een doelmarkt en die doelmarkt is gekoppeld aan een actieve broncode-ID/catalogus, kunnen callcentergebruikers zien welke catalogi een klant heeft ontvangen door de menuoptie **Broncodes** te selecteren op het menutabblad **Klanten** van de pagina **Klantenservice**. Tijdens orderinvoer kunnen callcentergebruikers ook de specifieke catalogi zien die naar een klant zijn verzonden, in de vervolgkeuzelijst **Bron** in de verkooporderkop. Als het filter wordt gewijzigd van **Alle** in **Beoogde**, kan de gebruiker de specifieke actieve catalogi zien die naar de klant zijn verzonden. Dit is handig in situaties waarin de klant zijn of haar catalogus mogelijk niet kan vinden of de cataloguscode niet kan vinden of lezen wanneer hij of zij belt om een verkooporder te maken.

Het is mogelijk meerdere broncode-id's te koppelen aan een catalogus. Dit is vaak vereist wanneer een bedrijf het responspercentage van verschillende segmenten wil bijhouden. Het bedrijf geeft een unieke cataloguscode aan verschillende klantsegmenten, zodat het responspercentage kan worden bijgehouden, tot aan het segmentniveau, binnen een bepaalde catalogusgebeurtenis.

Als een bepaalde **Broncode-ID**-record wordt geselecteerd en op de optie **Details** wordt geklikt op het sneltabblad **Broncodes**, krijgt u extra velden waar verkoopprognoses, verzendkosten en verzenddatums kunnen worden vastgelegd. Deze gegevens zijn handig voor het uitvoeren van gedetailleerde analyses van de effectiviteit van de catalogus. Gebruikers kunnen na verloop van tijd terugkeren naar deze pagina en de knoppen **Broncodeanalyse** en **Promoties vergelijken** gebruiken om analytische rapporten te activeren op basis van huidige verkoopgegevens en kosten en budgetten te vergelijken met werkelijke bedragen.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Catalogusspecifieke order- en artikelscripts configureren

Wanneer een callcentergebruiker een verkooporder maakt, kan hij of zij scripts op het scherm gebruiken. Deze op tekst gebaseerde scripts kunnen extra informatie bieden die de gebruiker aan de klant moet geven, of het kunnen interne opmerkingen/herinneringen zijn die de callcentergebruiker moet bekijken en op moet reageren wanneer deze de verkooporder maakt.

Het is vaak handig om verschillende reeksen scripts voor verschillende catalogi te hebben. Op het tabblad **Scripts** kunnen vooraf gedefinieerde scripts worden gekoppeld aan een catalogus. Gebruik het veld **Timing** veld om te bepalen of het script verschijnt aan het begin van de order (zodra de broncode-ID wordt ingevoerd in de orderkop) of aan het einde van de order (in het overzichtsformulier van de verkooporder).

Wanneer een knooppunt wordt geselecteerd in de hiërarchie van de catalogus en wordt gewerkt met de gegevens op het sneltabblad **Producten**, kunnen gebruikers met de actie **Scripts** ook scripts koppelen die specifiek voor catalogi of artikelen zijn.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Catalogusspecifieke upsell- en cross-sell-artikelen configureren

Upsell- of cross-sell-suggesties koppelen aan een artikel kan worden gedaan vanuit de productinstelling, maar in sommige gevallen wil een bedrijf speciale upsell- of cross-sell-artikelen promoten bij klanten die een specifiek product uit een specifieke catalogus bestellen. Selecteer op het sneltabblad **Producten** een artikel en klik op **Meerverkoop/bijverkoopartikelen** om producten te configureren voor upselling of cross-selling aan klanten die het geselecteerde artikel uit de catalogus hebben gekocht. Tijdens de callcenterorderinvoer worden specifieke upsell-/cross-sell-artikelen op het scherm weergegeven in plaats van standaard upsell-/cross-sell-producten die kunnen zijn geconfigureerd voor dat artikel door middel van de gebruikelijke productconfiguratie.

Artikelen upsellen/cross-sellen kan ook profiteren van de scriptfuncties om specifieke berichten te tonen die een gebruiker zal zien wanneer het upsell-/cross-sell-artikel wordt weergegeven tijdens orderinvoer. Scripts die zijn verbonden met upsell-/cross-sell-producten die specifiek voor een catalogusproduct zijn geconfigureerd, worden alleen weergegeven wanneer de broncode van die catalogus wordt toegepast in callcenterorderinvoer.

## <a name="catalog-page-analysis"></a>Analyse van cataloguspagina's

Op het tabblad **Catalogi** zijn opties beschikbaar om **Cataloguspagina's** te configureren. Met deze functie kunt u bepaalde pagina's en paginatypen voor de afgedrukte catalogus en de bijbehorende kosten ervan definiëren.

Bij het configureren van de producten in de catalogus gebruikt u de actie **Productpagina-indeling** om de specifieke pagina's, het percentage pagina's en de positie van de paginadetails voor het artikel te definiëren. Als deze gegevens worden geconfigureerd, kunnen gebruikers profiteren van het **Analyserapport van catalogusgebied**. U vindt dit rapport door te navigeren naar **Detailhandel** \> **Callcenterrapporten** \> **Analyse van catalogusgebied**. Dit rapport analyseert geplaatste verkoop ten opzichte van de catalogus (verkooporders waarbij de bron-ID voor de catalogus is verbonden met de orderkop of orderregel) en het bijbehorende paginapercentage en kosten om een traditioneel direct-marketingrapport **Vierkante centimeter-analyse** te krijgen.

## <a name="catalog-requests"></a>Catalogusaanvragen

Als catalogi worden geconfigureerd en gepubliceerd in Retail, kan de functie **Catalogus verzenden** worden gebruikt. Deze functie is beschikbaar op de pagina's **Klant zoeken** en **Klantenservice**. Na het selecteren van een klantrecord via **Klant zoeken** of tijdens het bekijken van een geselecteerde klantaccount vanuit **Klantenservice** kunnen gebruikers de optie **Catalogus verzenden** selecteren om een dialoogvenster te openen waarin de gebruiker kan kiezen uit een lijst met gepubliceerde en actieve catalogi. Een gebruiker kan een catalogus en een hoeveelheid selecteren en een bepaalde broncode-ID om te verzenden. Wanneer ze klikken op de knop **Verzenden**, wordt een aanvraag opgeslagen die vervolgens kan worden beheerd door het afdrukken van het rapport **Catalogusaanvragen**. U vindt dit rapport door te navigeren naar **Detailhandel** \> **Callcenterrapporten** \> **Rapport Catalogusaanvragen**. Hiermee worden alle catalogusverzoeken weergegeven, met inbegrip van de klantgegevens voor naam en adres van de klant die de catalogus heeft aangevraagd. Dit rapport kan intern worden gebruikt of de gegevens kunnen worden overgebracht naar een extern ondersteunend proces van derden voor het fysiek verzenden van de catalogus naar de klant.

## <a name="additional-features"></a>Extra functies

Op het tabblad **Catalogi** zijn ook opties beschikbaar voor het configureren van een **Betalingsplanning** en **Gratis producten**. Als de bron-code-ID die is gekoppeld aan de catalogus, wordt toegepast tijdens callcenterorderinvoer, komt de klant in aanmerking voor de gratis producten of gebruikt deze de specifieke catalogusbetalingsplanningen, zoals gedefinieerd. Als het nodig is de klant te beperken zodat deze alleen kan selecteren uit betalingsplanningen die aan hun catalogus zijn gekoppeld, en niet uit alle actieve betalingsplanningen in het systeem, kan het selectievakje **Alleen catalogusplannen toestaan** voor een of meer van de gedefinieerde broncode-ID's worden ingeschakeld om die beperking op te leggen.

## <a name="additional-notes"></a>Verdere notities

Momenteel, wanneer een broncode-ID wordt toegepast op een verkooporder in een callcenter, wordt deze gebruikt voor prijzen, promoties, scripts en upsells/cross-sells die catalogusspecifiek zijn. Het systeem verbiedt of voorkomt niet dat een product dat niet in de catalogus staat, wordt besteld op de verkooporder. Als een artikel wordt besteld dat geen deel uitmaakt van de catalogus, probeert het systeem eerst de **prijsgroep** te gebruiken die is gedefinieerd in het callcenterkanaal (**Detailhandel** \> **Afzetkanalen** \> **Callcenters** \> **Alle callcenters**) voor artikelprijs of promoties. Als er geen specifieke kanaalprijs wordt gevonden, wordt de basisverkoopprijs van het artikel gebruikt.
