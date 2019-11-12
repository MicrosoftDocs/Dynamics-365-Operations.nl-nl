---
title: Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat
description: Dit onderwerp beschrijft het proces voor het voltooien van eindproducten voor een productieorder tot aan de voorraad wanneer een nummerplaat de locatie beheert.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572124"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat 

Het proces met de naam Gereedmelding voltooit eindproducten op een productieorder in de voorraad. Als het voltooide product is ingeschakeld voor de geavanceerde magazijnprocessen, wordt het product gereedgemeld aan een locatie die de productie-uitvoerlocatie wordt genoemd. Zie [productie-uitvoerlocatie](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)voor informatie over het instellen van de productie-uitvoerlocatie.

U moet een bestaand nummerplaatnummer selecteren om deze taak te voltooien. Als de productie-uitvoerlocatie is ingesteld voor tracering met een nummerplaat, moet er een nummerplaatnummer worden opgenomen wanneer de productie-uitvoerlocatie wordt gereedgemeld. Het veld **Nummerplaat** wordt weer gegeven op de prompt **Voortgang rapporteren** van de pagina **Taakkaartapparaat**. Het veld wordt alleen weer gegeven op de prompt **Voortgang rapporteren** bij het rapporteren van de laatste bewerking van de productieorder. Het veld wordt alleen weergegeven als het artikel voor de productieorder is ingeschakeld voor magazijnbeheerprocessen. 
