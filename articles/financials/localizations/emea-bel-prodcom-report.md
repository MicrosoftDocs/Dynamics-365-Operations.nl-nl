---
title: PRODCOM instellen en onderhouden
description: In dit onderwerp wordt uitgelegd hoe u PRODCOM in Microsoft Dynamics 365 for Finance and Operations kunt instellen en beheren.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: IntrastatToProdcom, InventProdComLineDetail, InventProdComLineWithCode, InventProdComParameters, InventProdComTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264804
ms.search.region: Belgium
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 14dd8fd9c4e2111957ca87c46c90d8c26a345e21
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-and-maintain-prodcom"></a>PRODCOM instellen en onderhouden

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u PRODCOM in Microsoft Dynamics 365 for Finance and Operations kunt instellen en beheren. 

Fabrikanten van industriële producten zijn volgens de wet verplicht de hoeveelheden en waarden van de verkochte producten evenals bepaalde werknemersgegevens door te geven aan het Nationaal Instituut voor de Statistiek (NIS) in reactie op het jaarlijkse PRODCOM-onderzoek. De meeste producenten dienen maandelijks een gespecificeerd PRODCOM-rapport bij het NIS in middels een van de zes standaardrapportindelingen. Het NIS bepaalt de rapportindeling, afhankelijk van de aard van de geproduceerde materialen. Het PRODCOM-rapport bevat productiestatistieken voor industriële producten die worden vervaardigd door productiebedrijven die in België gevestigd zijn. Dit rapport wordt meestal gebruikt door accountants en boekhoudmanagers.

## <a name="set-up-prodcom-reporting"></a>PRODCOM-rapportage instellen
Voordat u het PRODCOM-rapport kunt genereren, moet u het volgende instellen op de pagina **PRODCOM-parameters**.

1.  Voer een primaire contactpersoon-id in. Dit is de identificatie die wordt afgedrukt onder het gedeelte met informatie over de primaire contactpersoon van de PRODCOM-aangifte.
2.  Voer een contactpersoon-id in. Dit is de identificatie die wordt afgedrukt onder het gedeelte met informatie over de externe contactpersoon van de PRODCOM-aangifte.
3.  Selecteer een bedrijf of magazijn.
    -   Als de lokale vestiging **Bedrijf** is, wordt het vestigingsnummer van het bedrijf naar de PRODCOM-regels overgeboekt.
    -   Als de lokale vestiging **Magazijn** is, wordt het vestigingsnummer van het magazijn waar de verkoop heeft plaatsgevonden, naar de PRODCOM-regels overgeboekt.
    -   Als het magazijn geen vestigingsnummer heeft, wordt het vestigingsnummer van het bedrijf gebruikt.

4.  Geef de voorkeur op voor een automatische herberekening.
5.  Nummerreeksen instellen.
6.  Geef de vestigings-id voor de rechtspersoon of magazijnen op. Zie voor meer informatie over de vestigings-id voor verwerking van rechtspersonen, waaronder de vereisten [Registratie-id's](emea-registration-ids.md).

## <a name="assign-prodcom-properties-to-an-item"></a>PRODCOM-eigenschappen toewijzen aan een artikel
PRODCOM-eigenschappen toewijzen aan een artikel (**Productgegevensbeheer** &gt; **Producten** &gt; **Vrijgegeven producten**). Open de pagina **Vrijgegeven productdetails** in de sectie **Buitenlandse handel**, open het dialoogvenster PRODCOM en geef de volgende gegevens op.

-   **Eigen product**: schakel dit selectievakje in als u hoeveelheden en waarden van producten moet rapporteren die zijn geleverd door bedrijven.
-   **Levering aan derden**: schakel dit selectievakje in als u hoeveelheden en waarden van producten wilt rapporteren die zijn geleverd door derden.
-   **Werk voor** **ondernemingen**: schakel dit selectievakje in als u hoeveelheden en waarden van producten wilt rapporteren die zijn geleverd door ondernemingen.

Nadat u PRODCOM hebt ingesteld, kunt u de pagina **PRODCOM** gebruiken om PRODCOM-perioden te maken en verkoopregels naar het PRODCOM-rapport over te boeken.

## <a name="convert-intrastat-to-prodcom"></a>Conversie van Intrastat naar PRODCOM
Gebruik de pagina **Conversie van Intrastat naar PRODCOM** om PRODCOM-codes toe te wijzen aan Intrastat-basisproductcodes. Deze codes kunnen elk jaar wijzigen. Klik op de pagina **Conversie van Intrastat naar PRODCOM** op **PRODCOM-gegevens importeren** om de gegevens te importeren.

## <a name="use-prodcom"></a>PRODCOM gebruiken
Gebruik de pagina **PRODCOM** om PRODCOM-perioden te maken en verkoopregels naar het PRODCOM-rapport over te boeken. Nadat u de datums voor de aangifteperiode hebt ingevoerd en vervolgens de sectiecodes invoert, kunt u de verkoopregels overboeken naar het PRODCOM-rapport. Nadat u de verkoopregels naar het rapport hebt overgeboekt, kunt u de producten op de PRODCOM-lijst bekijken en bewerken en vervolgens het rapport afdrukken.




