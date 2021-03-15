---
title: Garantieovereenkomsten
description: In dit onderwerp worden garantieovereenkomsten in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021499"
---
# <a name="warranty-agreements"></a>Garantieovereenkomsten

[!include [banner](../../includes/banner.md)]

 


In Asset Management kunt u garantievoorwaarden instellen die kunnen worden verbonden met een activum of een activatype. Er worden garantievoorwaarden gemaakt voor een specifieke periode. U kunt de garantie instellen om volledige dekking of een deel van de dekking te bieden en u kunt voorwaarden instellen die zijn gerelateerd aan uren, onkosten en artikelen.

De eerste stap is het maken van garantieovereenkomsten voor leveranciers die u voor uw apparatuur hebt. Vervolgens koppelt u garantieovereenkomsten aan activa of activatypen. Garantieovereenkomsten met leveranciers worden alleen voor informatieve doeleinden gebruikt. Als er een leveranciersgarantie is ingesteld voor een activum, ziet u de dekkingsperiode van de garantie op de activa.

## <a name="create-a-warranty-agreement"></a>Een garantieovereenkomst maken

Een garantieovereenkomst kan meerdere overeenkomstregels bevatten om de garantie voor werkuren, onkosten en artikelen te dekken.

1. Selecteer **Activabeheer** \> **Instellen** \> **Activa** \> **Garantie**.
2. Selecteer **Nieuw** om een product te maken.
3. Voer in het veld **Garantie** een garantie-id in. 
4. Voer in het veld **Naam** een beschrijving in.

    Het Sneltabblad **Details** geeft het veld **Activa** het aantal actieve activa weer dat de garantieovereenkomst gebruikt.

5. Voer op het sneltabblad **Garantieregels** de volgende stappen uit om regels toe te voegen die moeten worden opgenomen in een garantieovereenkomst:

    1. Selecteer **Regel toevoegen** om een nieuwe voorwaarde toe te voegen aan de groep. In het veld **Regel** wordt automatisch een volgnummer voor de regel ingevoerd.
    2. Selecteer in het veld **Periode** het type garantieperiode.
    3. Typ een getal in het veld **Interval**. Dit veld bepaalt het aantal Perioden waarvoor de garantie geldig moet zijn.
    4. Voer in veld **Percentage** het dekkingspercentage voor de garantieregel in. Het percentage geeft aan hoeveel door uw bedrijf wordt gedekt.

![Pagina Garantie](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]