---
title: Overzicht van transitorische posten
description: In dit artikel worden toerekeningen beschreven en wordt aangegeven hoe u deze instelt en transacties maakt.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23d4ab4a3a14a3068daf49090db6ffab4fb586ff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985056"
---
# <a name="accruals-overview"></a>Overzicht van transitorische posten

[!include [banner](../includes/banner.md)]

In dit artikel worden toerekeningen beschreven en wordt aangegeven hoe u deze instelt en transacties maakt.

Transitorische posten worden gebruikt in periodetoerekeningsboekhouding om opbrengst bij te houden die wordt verantwoord in de periode waarin deze wordt verdiend en niet wanneer de betaling wordt ontvangen, en om onkosten (kosten) bij te houden die worden verantwoord wanneer ze worden gemaakt en niet wanneer de betaling wordt uitgevoerd.

## <a name="accrual-schemes"></a>Toerekeningsschema's
Toerekeningsschema's worden gebruikt om de uitgestelde opbrengst en de kosten in te stellen en hetzelfde toerekeningsschema kan zowel voor opbrengsten als voor kosten worden gebruikt. Met transitorische grootboekposten worden de kosten of opbrengsten van een journaalregel zo verdeeld dat de kosten en opbrengsten in de betreffende perioden worden verantwoord. Op de pagina **Toerekeningsschema** geeft u de debet- en creditrekeningen op die worden gebruikt wanneer het toerekeningsschema wordt toegepast.

-   **Debet**: met de hoofdrekening die u definieert, wordt de debethoofdrekening op de journaalboekstukregel vervangen. Deze rekening wordt ook gebruikt voor de terugboeking van het uitstel op basis van de transitorische grootboekposttransacties.
-   **Credit**: met de hoofdrekening die u definieert, wordt de credithoofdrekening op de journaalboekstukregel vervangen. Deze rekening wordt ook gebruikt voor de terugboeking van het uitstel op basis van de transitorische grootboekposttransacties.

Nadat u hebt bepaald welke rekeningen moeten worden gebruikt, kunt u opgeven hoe het boekstuknummer wordt gemaakt wanneer de transitorische posten worden gemaakt. U kunt ook opgeven hoe vaak de transacties plaatsvinden, het aantal keren dat de transacties worden gemaakt en wanneer de transacties worden geboekt. Nadat het toerekeningsschema is gemaakt, kunt u het in sommige journalen gebruiken met behulp van de functie Transitorische grootboekposten.

## <a name="ledger-accruals"></a>Transitorische grootboekposten
Wanneer u een journaal invoert, kunt u klikken op **Transitorische grootboekposten** in het menu **Functies**. Wanneer u vervolgens het toerekeningsschema selecteert, ziet u het basisbedrag van het journaal dat over de periode wordt verspreid, zoals bepaald door het toerekeningsschema. Als u bijvoorbeeld de verzekering van een werknemer voor het hele jaar in januari betaalt en het bedrag is 12.000, moet u die onkosten elke maand verantwoorden. U kunt de begindatum selecteren. U kunt ook opgeven of het bedrag dat wordt toegerekend, wordt gebaseerd op de rekening of de tegenrekening. Nadat u uw selecties hebt gemaakt, klikt u op **Transacties** om alle transacties weer te geven die zijn gemaakt op basis van het toerekeningsschema. Bijvoorbeeld: als u het bedrag van 12.000 aan verzekeringsonkosten over het jaar verspreid, ziet u een bedrag van 1000 voor elke maand. Nadat u het journaal hebt geboekt, kunt u de transacties bekijken met behulp van de querypagina **Boekstuktransacties**. Als een toerekeningsschema niet kan worden toegepast (bijvoorbeeld in geval van een verkooporderfactuur of inkooporderfactuur), kunt u het vooruitbetaalde bedrag crediteren en het onkostenbedrag debiteren. Vervolgens kunt u **Tegenrekening** selecteren wanneer u het toerekeningsschema toepast.


Zie voor meer informatie [Toerekeningsschema's maken](tasks/create-accrual-schemes.md) en [Toenametransacties voor grootboek maken](tasks/create-ledger-accrual-transactions.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]