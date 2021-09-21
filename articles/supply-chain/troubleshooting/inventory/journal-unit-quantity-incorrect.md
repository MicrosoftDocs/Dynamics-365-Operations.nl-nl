---
title: De eenheid en hoeveelheid per eenheid werken niet goed in het voorraadjournaal
description: De eenheid en hoeveelheid per eenheid werken niet goed in het voorraadjournaal
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475993"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>De eenheid en hoeveelheid per eenheid werken niet goed in het voorraadjournaal

## <a name="symptoms"></a>Symptomen

Er kunnen een of meer van de volgende problemen voorkomen wanneer u met eenheden en hoeveelheden in een voorraadjournaal werkt:

- U ziet geen eenheden of eenheidshoeveelheden in het voorraadjournaal terwijl er een omrekeningseenheid is ingesteld voor het vrijgegeven product en u kunt de eenheid niet wijzigen in het voorraadjournaal.
- U ziet de velden **Hoeveelheid** en **Eenheid** in het voorraadjournaal, maar het veld **Hoeveelheid per eenheid** niet. Als u de eenheid wijzigt, een hoeveelheid invoert en het journaal boekt, wordt in het journaal nog steeds de oorspronkelijke maateenheid voor die hoeveelheid gebruikt.

## <a name="resolution"></a>Oplossing

Volg deze stappen om dit probleem op te lossen.

1. Zorg er in het werkgebied **Functiebeheer** voor dat de functie *Maateenheid en hoeveelheid per eenheid in voorraadjournalen gebruiken* is ingeschakeld. Met deze functie voegt u de velden **Eenheid** en **Hoeveelheid per eenheid** aan het journaal toe.
1. Nadat de functie is ingeschakeld, gebruikt u de velden **Hoeveelheid**, **Hoeveelheid per eenheid** en **Eenheid** als volgt:

    - **Hoeveelheid**: geef de hoeveelheid op door de standaardeenheid te gebruiken die voor het vrijgegeven product is gedefinieerd. De standaardeenheid zelf wordt hier echter niet weergegeven. Als er een omrekening is ingesteld tussen de standaardeenheid en de eenheid die is geselecteerd in het veld **Eenheid**, wordt het veld **Hoeveelheid** automatisch bijgewerkt op basis van de selecties in de velden **Hoeveelheid per eenheid** en **Eenheid**.
    - **Hoeveelheid per eenheid**: geef de hoeveelheid op met behulp van de eenheid die is geselecteerd in het veld **Eenheid**.
    - **Eenheid**: selecteer de eenheid die moet worden toegepast op de waarde in het veld **Hoeveelheid per eenheid**.
