---
title: Garantieovereenkomsten
description: In dit onderwerp worden garantieovereenkomsten in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71905d5b362c80d48b78210b59cacfb1e7899757
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874688"
---
# <a name="warranty-agreements"></a>Garantieovereenkomsten

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


In Asset Management kunt u garantievoorwaarden instellen die kunnen worden verbonden met een activum of een activatype. Er worden garantievoorwaarden gemaakt voor een specifieke periode. U kunt de garantie instellen om volledige dekking of een deel van de dekking te bieden en u kunt voorwaarden instellen die zijn gerelateerd aan uren, onkosten en artikelen.

De eerste stap is het maken van garantieovereenkomsten voor leveranciers die u voor uw apparatuur hebt. Vervolgens koppelt u garantieovereenkomsten aan activa of activatypen. Garantieovereenkomsten met leveranciers worden alleen voor informatieve doeleinden gebruikt. Als er een leveranciersgarantie is ingesteld voor een activum, ziet u de dekkingsperiode van de garantie op de activa.

## <a name="create-a-warranty-agreement"></a>Een garantieovereenkomst maken

Een garantieovereenkomst kan meerdere overeenkomstregels bevatten om de garantie voor werkuren, onkosten en artikelen te dekken.

1. Selecteer **Activabeheer** \> **Instellen** \> **Activa** \> **Garantie**.
2. Selecteer **Nieuw** om een product te maken.
3. Voer in het veld **Garantie** een garantie-id in.
4. Voer in het veld **Naam** een beschrijving in.

    Het Sneltabblad **Details** geeft het veld **Activa** het aantal actieve activa weer dat de garantieovereenkomst gebruikt.

5. Voer op de Sneltabbladen **Urengarantie** en **Artikelgarantie** de volgende stappen uit om regels toe te voegen die moeten worden opgenomen in een garantieovereenkomst die betrekking heeft op uren of artikelen:

    1. Selecteer **Regel toevoegen** om een nieuwe voorwaarde toe te voegen aan de groep. In het veld **Regel** wordt automatisch een volgnummer voor de regel ingevoerd.
    2. Selecteer in het veld **Periode** het type garantieperiode.
    3. Typ een getal in het veld **Interval**. Dit veld bepaalt het aantal Perioden waarvoor de garantie geldig moet zijn.
    4. Voer in veld **Percentage** het dekkingspercentage voor de garantieregel in. Het percentage geeft aan hoeveel door uw bedrijf wordt gedekt.

![Figuur 1](media/01-warranty.png)