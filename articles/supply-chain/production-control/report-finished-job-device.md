---
title: Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat
description: Dit onderwerp beschrijft het proces voor het voltooien van eindproducten voor een productieorder tot aan de voorraad wanneer een nummerplaat de locatie beheert.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092563"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat 

Het proces met de naam Gereedmelding voltooit eindproducten op een productieorder in de voorraad. Als het voltooide product is ingeschakeld voor de geavanceerde magazijnprocessen, wordt het product gereedgemeld aan een locatie die de productie-uitvoerlocatie wordt genoemd. Zie [productie-uitvoerlocatie](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)voor informatie over het instellen van de productie-uitvoerlocatie.

Als de productie-uitvoerlocatie wordt gecontroleerd op nummerplaat, moet een nummerplaat worden opgegeven bij het gereedmelden. Het veld **Nummerplaat** wordt weer gegeven op de prompt **Voortgang rapporteren** van de pagina **Taakkaartapparaat**. Het veld is alleen zichtbaar bij **Voortgang melden** bij het rapporteren over de laatste bewerking van de productieorder en als het artikel voor de productieorder is ingeschakeld voor de magazijnbeheerprocessen. 

Er zijn twee opties voor het opgeven van de nummerplaat
- De gebruiker selecteert een bestaande nummerplaat in het veld Nummerplaat.
- De nummerplaat wordt automatisch gegenereerd op basis van een nummerreeks en wordt standaard opgenomen in het veld Nummerplaat.

U configureert de optie om de nummerplaat automatisch te laten genereren door de optie **Nummerplaat genereren** op de pagina **Taakkaart configureren voor apparaten** te selecteren.
