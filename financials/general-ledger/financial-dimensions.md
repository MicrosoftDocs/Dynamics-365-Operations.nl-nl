---
title: "Financiële dimensies"
description: "In dit artikel worden de verschillende typen financiële dimensies uitgelegd en hoe ze worden ingesteld."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Financiële dimensies

In dit artikel worden de verschillende typen financiële dimensies uitgelegd en hoe ze worden ingesteld.

Gebruik de pagina Financiële dimensies om financiële dimensies te maken die u als rekeningsegmenten kunt gebruiken voor rekeningsschema's. Er zijn twee typen van financiële dimensies, aangepaste dimensies en door een entiteit ondersteunde dimensies. De aangepaste dimensies worden gedeeld over rechtspersonen en de waarden worden door de gebruiker ingevoerd en onderhouden. Door een entiteit ondersteunde dimensies zijn dimensies waarvan de waarden elders in het systeem worden gedefinieerd, zoals Klanten of Winkels. Bepaalde door entiteiten ondersteunde dimensies zijn verdeeld over rechtspersonen en sommige door entiteiten ondersteunde dimensies zijn bedrijfsspecifiek. 

Nadat u de financiële dimensies hebt gemaakt, gebruikt u de pagina Waarden van financiële dimensie om aanvullende eigenschappen toe te wijzen aan elke financiële dimensie. 

Hoewel u financiële dimensies gebruiken kunt om aan te geven van rechtspersonen zonder dat de rechtspersonen in Microsoft Dynamics 365 voor bewerkingen, financiële dimensies zijn niet bedoeld voor het adres van de operationele of bedrijf nodig heeft van rechtspersonen. De Inter-unit boekhouding-functionaliteit in Microsoft Dynamics 365 for Operations is ontworpen om alleen de boekingen die zijn gemaakt door elke transactie. 

Voordat u de financiële dimensies instelt als rechtspersonen, moet u uw bedrijfsprocessen evalueren in de volgende gebieden om te bepalen of deze instelling zal werken voor uw organisatie:

-   Voorraad
-   Verkoop en inkoop tussen financiële dimensies en rechtspersonen
-   Btw-berekening en rapportage
-   Operationele rapporteren

Hierna volgen enkele voorbeelden van de beperkingen:

-   U kunt de btw-functionaliteit alleen gebruiken met rechtspersonen, niet met financiële dimensies.
-   Sommige rapporten omvatten geen financiële dimensies, zodat u niet altijd volgens financiële dimensie kunt rapporteren tenzij rapporten worden gewijzigd.

**Custom dimensions** 

Voor meer informatie over het maken van een gebruiker gedefinieerde financiële dimensie in het veld waarden gebruiken van &lt;aangepaste dimensie&gt;. U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die u voor dimensiewaarden kunt invoeren. U kunt tekens zoals letters of een koppelteken invoeren die voor elke dimensiewaarde hetzelfde blijven. U kunt ook opgeven met hekjes (\#) en ampersands (&) als tijdelijke aanduidingen voor cijfers en letters die verandert telkens wanneer een dimensiewaarde wordt gemaakt. Gebruik een hekje (\#) als tijdelijke aanduiding voor een nummer en een en -teken (&) als tijdelijke aanduiding voor een brief. 

**Voorbeeld ** 

Alleen de dimensiewaarde voor de letters CC en drie cijfers u CC -\#\#\# als het opmaakmasker. Dit veld is alleen beschikbaar wanneer u &lt;aangepaste dimensie &gt;in het veld waarden gebruiken van. 

**Back-entiteit-dimensies** 

Als u een financiële entiteitdimensie back in het veld waarden gebruiken van, selecteert een systeem gedefinieerde entiteit waarop de financiële dimensie moet worden. Waarden van financiële dimensies worden op basis van deze selectie gemaakt. Als u bijvoorbeeld dimensiewaarden voor projecten wilt maken, selecteert u Projecten. Er wordt voor elke projectnaam een dimensiewaarde gemaakt. Op de pagina Dimensiewaarden worden de waarden voor de entiteit weergegeven en of deze bedrijfsspecifiek zijn, het bedrijf voor de waarde. 

**Activeren** 

Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet overal gebruiken voordat deze is geactiveerd. U kunt een financiële dimensie bijvoorbeeld niet toevoegen aan een rekeningstructuur voordat de financiële dimensie is geactiveerd. Als u op Activeren klikt, worden alle dimensies met statuswijzigingen bijgewerkt. 

**Translations** 

De pagina van de vertaling van tekst kunt u tekst invoeren die moet worden weergegeven in verschillende talen voor de geselecteerde financiële dimensie. Op de pagina Vertaling hoofdrekening kunt u tekst invoeren die in verschillende talen moet worden weergegeven voor de hoofdrekening. 

**Legal entity overrides** 

Niet alle dimensies zijn geldig voor alle rechtspersonen en sommige alleen relevant kan zijn voor een bepaalde periode. In dit scenario kan de sectie Overschrijvingen rechtspersoon worden gebruikt om te bepalen voor welke bedrijven de dimensie moet worden opgeschort, wie de eigenaar is en gedurende welke periode de dimensie actief is.




