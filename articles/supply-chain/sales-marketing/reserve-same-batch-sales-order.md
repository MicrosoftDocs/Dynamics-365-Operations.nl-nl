---
title: Dezelfde batch voor een verkooporder reserveren
description: "In dit artikel wordt beschreven hoe u een product instelt om de reservering van voorraad voor één batch van voorraad toe te staan."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aef3a52f4cb2d5af47a8c25a67e6c2076fa1ff03
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Dezelfde batch voor een verkooporder reserveren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een product instelt om de reservering van voorraad voor één batch van voorraad toe te staan.

Met reserveringen uit dezelfde batch kunt u voorraad reserveren voor een verkooporderregel uit één voorraadbatch. Een klant die behang bestelt, kan bijvoorbeeld aangeven dat de volledige order uit dezelfde batch of partij moet worden gehaald om verschillen tussen de rollen te voorkomen. Als u een product wilt instellen voor reservering uit dezelfde batch, moeten de volgende instellingen actief zijn in de artikelmodelgroep, traceringsdimensiegroep en opslagdimensiegroepen die u aan het product toewijst:

-   **Artikelmodelgroepen**: in de artikelmodelgroep moeten de velden **Dezelfde batchselectie** en **Behoeften consolideren** zijn geselecteerd in de veldgroep **Reservering** voor voorraadbeleid.
-   **Traceringsdimensiegroepen**: in de traceringsdimensiegroep moet het veld **In behoefteplan opnemen volgens dimensie** zijn geselecteerd voor het batchnummer.
-   **Opslagdimensiegroepen**: in de opslagdimensiegroep moet het veld **In behoefteplan opnemen volgens dimensie** zijn geselecteerd voor **Locatie** en **Magazijn**.

Als u voorraad reserveert voor een product op een verkooporderregel die is ingesteld voor selectie uit dezelfde batch, probeert Microsoft Dynamics 365 for Finance and Operations de bestelde hoeveelheid te reserveren uit één voorraadbatch. Hierbij wordt rekening gehouden met eventuele specifieke batchkenmerkbehoeften. Als de hoeveelheid niet uit één batch kan worden gehaald, wordt de pagina **Conflict door reservering van dezelfde batch** weergegeven. Deze pagina geeft de uitgiften en ook de acties weer die u kunt uitvoeren om door te gaan met de reservering. De volgende omstandigheden kunnen voorkomen dat de batch wordt gereserveerd:

-   Het veld **Reservering blokkeren** voor verkoop van de batchbeschikkingscode heeft de markering **Geblokkeerd**.
-   De batchdatum is verlopen op basis van de vervaldatum en eventuele van toepassing zijnde verkoopbare dagen voor de klant. Het artikel kan nog in aanmerking komen voor reservering als de artikelmodelgroep voor het artikel een FEFO (First Expiry First Out)-datumcontrole heeft en als de houdbaarheidsdatum is geselecteerd als orderverzamelcriterium.
-   Er zijn onvoldoende houdbaarheidsdagen resterend voor de batch op basis van de vervaldatum en houdbaarheidsdatum plus eventuele van toepassing zijnde verkoopbare dagen voor de klant.





