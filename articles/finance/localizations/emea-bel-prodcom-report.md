---
title: PRODCOM instellen en onderhouden
description: In dit artikel wordt uitgelegd hoe u PRODCOM instelt en onderhoudt in Microsoft Dynamics 365 Finance.
author: EvgenyPopovMBS
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: IntrastatToProdcom, InventProdComLineDetail, InventProdComLineWithCode, InventProdComParameters, InventProdComTable
audience: Application User
ms.reviewer: kfend
ms.custom: 264804
ms.search.region: Belgium
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 83d5d813d3195ecf53e0e4a57feaa42bf2bec57f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883094"
---
# <a name="set-up-and-maintain-prodcom"></a>PRODCOM instellen en onderhouden

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u PRODCOM instelt en onderhoudt. Fabrikanten van industriële producten zijn wettelijk verplicht de hoeveelheden en waarden van verkochte producten en bepaalde werknemersgegevens door te geven aan het Nationaal Instituut voor de Statistiek (NIS) in reactie op het routinematige PRODCOM-onderzoek. De meeste producenten dienen maandelijks een gespecificeerd PRODCOM-rapport bij het NIS in middels een van de zes standaardrapportindelingen. Het NIS bepaalt de rapportindeling, afhankelijk van de aard van de geproduceerde materialen. Het PRODCOM-rapport bevat productiestatistieken voor industriële producten die worden vervaardigd door productiebedrijven die in België gevestigd zijn. Dit rapport wordt meestal gebruikt door accountants en boekhoudmanagers.

## <a name="set-up-prodcom-reporting"></a>PRODCOM-rapportage instellen

Voordat u het PRODCOM-rapport genereert, moet u de PRODCOM-parameters instellen.

1. Ga naar **Belastingen** \> **Instellingen** \> **Buitenlandse handel** \> **PRODCOM-parameters**.
2. Voer een primaire contactpersoon-id in. Deze identificatie wordt afgedrukt onder het gedeelte met informatie over de primaire contactpersoon van de PRODCOM-verklaring.
3. Een externe contact-ID invoeren. Deze identificatie wordt afgedrukt onder het gedeelte met informatie over de externe contactpersoon van de PRODCOM-verklaring.
4. Selecteer een bedrijf of magazijn:

    - Als de lokale vestiging **Bedrijf** is, wordt het vestigingsnummer van het bedrijf naar de PRODCOM-regels overgeboekt.
    - Als de lokale vestiging **Magazijn** is, wordt het vestigingsnummer van het magazijn waar de verkoop heeft plaatsgevonden, naar de PRODCOM-regels overgeboekt.
    - Als het magazijn geen vestigingsnummer heeft, wordt in plaats daarvan het vestigingsnummer van het bedrijf gebruikt.

5. Geef de voorkeur op voor een automatische herberekening.
6. Nummerreeksen instellen.
7. Geef de vestigings-ID voor de rechtspersoon of magazijnen op. Zie voor meer informatie over de vestigings-ID voor verwerking van rechtspersonen, waaronder informatie over de vereisten [Registratie-ID's](emea-registration-ids.md).

## <a name="assign-prodcom-properties-to-an-item"></a>PRODCOM-eigenschappen toewijzen aan een artikel

1. Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten** om PRODCOM-eigenschappen toe te wijzen aan een artikel. 
2. Open de pagina **Informatie vrijgegeven product** in het gedeelte **Buitenlandse handel**, open het dialoogvenster PRODCOM en stel de volgende velden in:

    - **Eigen product** - schakel dit selectievakje in als u hoeveelheden en waarden van producten wilt rapporteren die zijn geleverd door bedrijven.
    - **Levering aan derden** - schakel dit selectievakje in als u hoeveelheden en waarden van producten wilt rapporteren die zijn geleverd door derden.
    - **Werk gedaan voor** **ondernemingen** - schakel dit selectievakje in als u hoeveelheden en waarden van producten wilt rapporteren die zijn geleverd door ondernemingen.

3. Wanneer u het instellen van PRODCOM hebt voltooid, gaat u naar **Belastingen** \> **Aangiften** \> **Buitenlandse handel** \> **PRODCOM** om PRODCOM-perioden aan te maken en verkoopregels naar het PRODCOM-rapport over te dragen.

## <a name="convert-intrastat-to-prodcom"></a>Conversie van Intrastat naar PRODCOM

1. Ga naar **Belastingen** \> **Instellingen** \> **Buitenlandse handel** \> **Conversie van Intrastat naar PRODCOM** om PRODCOM-codes toe te wijzen aan Intrastat-basisproductcodes. Deze codes kunnen elk jaar wijzigen.
2. Selecteer op de pagina **Conversie van Intrastat naar PRODCOM** **PRODCOM-gegevens importeren** om de informatie te importeren.

## <a name="use-prodcom"></a>PRODCOM gebruiken
Gebruik de pagina **PRODCOM** om PRODCOM-perioden te maken en verkoopregels naar het PRODCOM-rapport over te boeken. Nadat u de datums voor de aangifteperiode hebt ingevoerd en vervolgens de sectiecodes invoert, kunt u de verkoopregels overboeken naar het PRODCOM-rapport. Nadat u de verkoopregels naar het rapport hebt overgeboekt, kunt u de producten op de PRODCOM-lijst bekijken en bewerken en vervolgens het rapport afdrukken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
