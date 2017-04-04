---
title: Instellen en beheren van PRODCOM
description: In dit onderwerp wordt uitgelegd hoe u moet instellen en beheren van PRODCOM in Microsoft Dynamics 365 voor bewerkingen.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: IntrastatToProdcom, InventProdComLineDetail, InventProdComLineWithCode, InventProdComParameters, InventProdComTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264804
ms.assetid: b9c3b605-13fd-4764-9f7a-8d4a797297e0
ms.search.region: Belgium
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f7fd20ef0c78bc781f0ef9f17fc612723906ac78
ms.openlocfilehash: 8dc30a4dcf22eaa2fb5403ba479fb8f533472d03
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-maintain-prodcom"></a>Instellen en beheren van PRODCOM

In dit onderwerp wordt uitgelegd hoe u moet instellen en beheren van PRODCOM in Microsoft Dynamics 365 voor bewerkingen. 

Fabrikanten van industriële producten zijn volgens de wet verplicht de hoeveelheden en waarden van de verkochte producten evenals bepaalde werknemersgegevens door te geven aan het Nationaal Instituut voor de Statistiek (NIS) in reactie op het jaarlijkse PRODCOM-onderzoek. De meeste producenten dienen maandelijks een gespecificeerd PRODCOM-rapport bij het NIS in middels een van de zes standaardrapportindelingen. Het NIS bepaalt de indeling, afhankelijk van de aard van de geproduceerde materialen. Het PRODCOM-rapport bevat productiestatistieken voor industriële producten die worden vervaardigd door productiebedrijven die in België. Dit rapport wordt meestal gebruikt door accounting en boekhouders.

## <a name="set-up-prodcom-reporting"></a>PRODCOM-rapportage instellen
Voordat u het PRODCOM-rapport genereren kunt, moet u instellen van het volgende op de **PRODCOM-parameters** pagina.

1.  Voer een primaire contact-ID. Dit is de id die wordt afgedrukt onder het gedeelte van de primaire contactgegevens van de PRODCOM-aangifte.
2.  Voer een extern contactpersoon-ID: dit is de id die wordt afgedrukt onder het gedeelte van de externe contactgegevens van de PRODCOM-aangifte.
3.  Selecteer een bedrijf of magazijn.
    -   Als de lokale vestiging **bedrijf**, het vestigingsnummer van het bedrijf wordt overgebracht naar de PRODCOM-regels.
    -   Als de lokale vestiging **magazijn**, het vestigingsnummer van het magazijn waar de verkoop plaatsgevonden heeft wordt overgebracht naar de PRODCOM-regels.
    -   Als het magazijn geen vestigingsnummer heeft, wordt het vestigingsnummer van het bedrijf gebruikt.

4.  Geef de voorkeur voor een automatische herberekening.
5.  Nummerreeksen instellen.
6.  Geef de vertakking-ID voor de rechtspersoon of magazijnen. Zie voor meer informatie over de vertakking-ID van de juridische entiteit verwerking, met inbegrip van de vereiste onderdelen [registratie-id's](emea-registration-ids.md).

## <a name="assign-prodcom-properties-to-an-item"></a>PRODCOM-eigenschappen toewijzen aan een artikel
PRODCOM-eigenschappen toewijzen aan een artikel (**productgegevensbeheer**&gt;**producten**&gt;**vrijgegeven producten**). Open de **vrijgegeven productdetails** pagina in de **buitenlandse handel** sectie, opent u het dialoogvenster PRODCOM en de volgende gegevens bevatten.

-   **Eigen product** -Schakel dit selectievakje in als u verplicht hoeveelheden en waarden van producten die zijn geleverd door companies.* **
-   **Levering aan een derde partij** -Schakel dit selectievakje in als u verplicht hoeveelheden en waarden van producten die zijn geleverd door derden.
-   **Werkzaamheden voor****ondernemingen** -Schakel dit selectievakje in als u verplicht hoeveelheden en waarden van producten die zijn geleverd door enterprises.* **

Nadat u PRODCOM hebt ingesteld, kunt u de **PRODCOM** pagina PRODCOM-perioden en verkoopregels naar het PRODCOM-rapport overboeken.

## <a name="convert-intrastat-to-prodcom"></a>Conversie van Intrastat naar PRODCOM
Gebruik de **van Intrastat naar PRODCOM-conversie** pagina toewijzen PRODCOM-codes aan Intrastat-basisproductcodes. Deze codes kunnen elk jaar wijzigen. Op de **van Intrastat naar PRODCOM-conversie** pagina, klikt u op **importeren PRODCOM-gegevens** u de gegevens wilt importeren.

## <a name="use-prodcom"></a>PRODCOM gebruiken
Gebruik de **PRODCOM** pagina PRODCOM-perioden en verkoopregels naar het PRODCOM-rapport overboeken. Nadat u de datums voor de aangifteperiode invoeren en voer vervolgens de sectiecodes, kunt u de verkoopregels overbrengen naar het PRODCOM-rapport. Nadat u de verkoopregels naar het rapport overbrengen, kunt u bekijken en bewerken van de producten op de PRODCOM-lijst en vervolgens kunt u het rapport afdrukken.


