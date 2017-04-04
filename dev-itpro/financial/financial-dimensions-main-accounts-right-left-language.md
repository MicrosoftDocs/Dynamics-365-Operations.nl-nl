---
title: "Financiële dimensies en hoofdrekeningen in een taal die van rechts naar links wordt geschreven"
description: "In dit onderwerp worden enkele implementatiebeslissingen beschreven waarmee u rekening moet houden wanneer u een van rechts naar links geschreven taal in Microsoft Dynamics 365 for Operations gebruikt. Daarnaast wordt aangegeven hoe u financiële dimensies en hoofdrekeningen instelt."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0a2fcbbc91960e0602f42d89ca5e46b8d51f98d6
ms.openlocfilehash: da5c53ddf113daf19a9832cf59f7a231a00b3367
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Financiële dimensies en hoofdrekeningen in een taal die van rechts naar links wordt geschreven

In dit onderwerp worden enkele implementatiebeslissingen beschreven waarmee u rekening moet houden wanneer u een van rechts naar links geschreven taal in Microsoft Dynamics 365 for Operations gebruikt. Daarnaast wordt aangegeven hoe u financiële dimensies en hoofdrekeningen instelt.

Financiële dimensies en hoofdrekeningen zijn belangrijke onderdelen van de planningsfase voor een implementatie. Nadat financiële dimensies en hoofdrekeningen in het systeem zijn gemaakt, worden deze gebruikt op de pagina's **Rekeningstructuren configureren**, **Geavanceerde regelstructuren** en **Configuratie van financiële dimensies voor integrerende toepassingen**. De gedefinieerde volgorde op die pagina's wordt gebruikt in het systeem voor gegevensinvoer en -verbruik. Op sommige locaties in het systeem worden de financiële dimensies en hoofdrekeningen in afzonderlijke velden weergegeven. En op andere locaties, zoals in journalen, worden de financiële dimensies en hoofdrekeningen als één reeks weergegeven.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Aanbevolen procedures voor het instellen van financiële dimensies en hoofdrekeningen in een systeem van rechts naar links

-   Wanneer u het scheidingsteken voor rekeningschema's, selecteer een van de opties dubbele scheidingsteken: dubbel koppelteken (-), dubbele balk (|) of dubbele punt (.) of dubbele onderstrepingstekens (\_\_).
-   Wanneer u de waarden voor financiële dimensies en hoofdrekeningen maakt, moet u alleen cijfers en tekens voor talen gebruiken die van rechts naar links worden geschreven.
-   Gebruik niet het geselecteerde scheidingsteken voor rekeningschema's in waarden voor financiële dimensie en hoofdrekeningen.

Door deze aanbevolen procedures te volgen, zorgt u ervoor dat de door de gebruiker gedefinieerd volgorde consistent wordt weergegeven in het systeem.


