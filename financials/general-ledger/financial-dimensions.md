---
title: "Financiële dimensies"
description: "In dit artikel worden de verschillende typen financiële dimensies uitgelegd en hoe ze worden ingesteld."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 01f189b8de3f0cc707dcc54f4cde75aed95b8e3f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions"></a>Financiële dimensies

[!include[banner](../includes/banner.md)]


In dit artikel worden de verschillende typen financiële dimensies uitgelegd en hoe ze worden ingesteld.

Gebruik de pagina Financiële dimensies om financiële dimensies te maken die u als rekeningsegmenten kunt gebruiken voor rekeningsschema's. Er zijn twee typen van financiële dimensies, aangepaste dimensies en door een entiteit ondersteunde dimensies. De aangepaste dimensies worden gedeeld over rechtspersonen en de waarden worden door de gebruiker ingevoerd en onderhouden. Door een entiteit ondersteunde dimensies zijn dimensies waarvan de waarden elders in het systeem worden gedefinieerd, zoals Klanten of Winkels. Bepaalde door entiteiten ondersteunde dimensies zijn verdeeld over rechtspersonen en sommige door entiteiten ondersteunde dimensies zijn bedrijfsspecifiek. 

Nadat u de financiële dimensies hebt gemaakt, gebruikt u de pagina Waarden van financiële dimensie om aanvullende eigenschappen toe te wijzen aan elke financiële dimensie. 

Hoewel u financiële dimensies kunt gebruiken om rechtspersonen te vertegenwoordigen zonder de entiteiten in Microsoft Dynamics 365 for Operations te maken, zijn financiële dimensies niet bedoeld om de operationele of zakelijke belangen van rechtspersonen te behartigen. De functionaliteit voor inter-unit boekhouding in Microsoft Dynamics 365 for Operations is ontworpen om alleen met de boekhoudkundige vermeldingen te werken die door elke transactie worden gemaakt. 

Voordat u de financiële dimensies instelt als rechtspersonen, moet u uw bedrijfsprocessen evalueren in de volgende gebieden om te bepalen of deze instelling zal werken voor uw organisatie:

-   Voorraad
-   Verkoop en inkoop tussen financiële dimensies en rechtspersonen
-   Btw-berekening en rapportage
-   Operationele rapporteren

Hierna volgen enkele voorbeelden van de beperkingen:

-   U kunt de btw-functionaliteit alleen gebruiken met rechtspersonen, niet met financiële dimensies.
-   Sommige rapporten omvatten geen financiële dimensies, zodat u niet altijd volgens financiële dimensie kunt rapporteren tenzij rapporten worden gewijzigd.

**Aangepaste dimensies** 

Als u een door de gebruiker gedefinieerde financiële dimensie wilt maken, selecteert u &lt; Aangepaste dimensie &gt; in het veld Waarden gebruiken van. U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die u voor dimensiewaarden kunt invoeren. U kunt tekens zoals letters of een koppelteken invoeren die voor elke dimensiewaarde hetzelfde blijven. U kunt ook hekjes (\#) en en-tekens (&) invoeren die dienen als tijdelijke aanduidingen voor letters en cijfers die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt. Gebruik een hekje (\#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter. 

**Voorbeeld** 

Om de dimensiewaarde te beperken tot de letters CC en drie getallen, voert u CC-\#\#\# als opmaakmasker in. Dit veld is alleen beschikbaar wanneer u &lt;Aangepaste dimensie &gt; selecteert in het veld Waarden gebruiken van. 

**Door een entiteit ondersteunde dimensies** 

Als u een door een entiteit ondersteunde financiële dimensie wilt maken, selecteert u in het veld Waarden gebruiken van een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd. Waarden van financiële dimensies worden op basis van deze selectie gemaakt. Als u bijvoorbeeld dimensiewaarden voor projecten wilt maken, selecteert u Projecten. Er wordt voor elke projectnaam een dimensiewaarde gemaakt. Op de pagina Dimensiewaarden worden de waarden voor de entiteit weergegeven en of deze bedrijfsspecifiek zijn, het bedrijf voor de waarde. 

**Dimensies activeren** 

Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet overal gebruiken voordat deze is geactiveerd. U kunt een financiële dimensie bijvoorbeeld niet toevoegen aan een rekeningstructuur voordat de financiële dimensie is geactiveerd. Als u op Activeren klikt, worden alle dimensies met statuswijzigingen bijgewerkt. 

**Vertalingen** 

Met de pagina Vertaling tekst kunt u tekst invoeren die in verschillende talen moet worden weergegeven voor de geselecteerde financiële dimensies. Op de pagina Vertaling hoofdrekening kunt u tekst invoeren die in verschillende talen moet worden weergegeven voor de hoofdrekening. 

**Overschrijvingen rechtspersoon** 

Niet alle dimensies zijn geldig voor alle rechtspersonen en sommige hoofdrekeningen zijn mogelijk alleen relevant voor een specifiek tijdsbestek. In dit scenario kan de sectie Overschrijvingen rechtspersoon worden gebruikt om te bepalen voor welke bedrijven de dimensie moet worden opgeschort, wie de eigenaar is en gedurende welke periode de dimensie actief is.






