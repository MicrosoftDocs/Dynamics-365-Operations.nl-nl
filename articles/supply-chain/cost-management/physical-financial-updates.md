---
title: Fysieke en financiële updates
description: Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b29c1c0727487992a478552d94b5bbe8684d0550
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967453"
---
# <a name="physical-and-financial-updates"></a>Fysieke en financiële updates

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen. 

Voorraadtransacties kunnen in Dynamics 365 Supply Chain Management fysiek en financieel worden bijgewerkt. Bepaalde typen van fysieke en financiële transacties verhogen voorraadhoeveelheden, terwijl andere de hoeveelheid verlagen.

## <a name="physical-increases"></a>Fysieke toename
Wanneer u een fysieke transactie boekt, wordt de status van de transactierecord **Ontvangen**. De volgende transacties worden beschouwd als een fysieke toename:

-   Ontvangst van inkooporder
-   Retour van pakbon voor verkooporder
-   Een productieorder gereedmelden
-   Bijproduct in een productieorderverzamellijst

## <a name="financial-increases"></a>Financiële toename
Wanneer u een financiële transactie boekt, wordt de status van de transactierecord die de hoeveelheid vergroot **Ingekocht**. De volgende transacties worden beschouwd als een financiële toename:

-   Leveranciersfactuur
-   Verkooporderfactuur voor een retour
-   Kostprijsberekening voor productieorder
-   Voorraadjournalen met een positieve hoeveelheid, zoals mutaties, winst en verlies, telling, stuklijsten en overboekingen

## <a name="transactions-that-increase-quantity"></a>Transacties waardoor de hoeveelheid toeneemt
Transacties waardoor de hoeveelheid toeneemt, worden geboekt tegen het lopend gemiddelde van de kostprijs. De berekende lopende gemiddelde kostprijs is gebaseerd op de kosten van elk van deze transacties voor elke voorraaddimensie die financieel wordt bijgehouden. Voor informatie over het uitvoeren van gemiddelde kostprijzen raadpleegt u [Lopende gemiddelde kostprijs](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transacties waardoor de hoeveelheid afneemt
Het berekende lopend gemiddelde van de kostprijs wordt gebruikt wanneer een transactie wordt geboekt waardoor de hoeveelheid afneemt, ongeacht welk voorraadwaarderingsmodel aan de voorraad is gekoppeld. De transactie, waardoor de hoeveelheid afneemt, mag vóór de boeking niet worden gekoppeld aan een andere transactie. Als de fysieke voorhanden voorraad negatief wordt, worden de voorraadkosten gebruikt die zijn gedefinieerd voor het artikel op de pagina **Artikel**. 

> [!NOTE]
> Als de functionaliteit voor meerdere sites is ingeschakeld, zijn deze kosten daarentegen de voorraadkosten die voor een locatie zijn gedefinieerd op de pagina **Standaard orderinstellingen**.

## <a name="physical-issues-vs-financial-issues"></a>Fysieke uitgiften en financiële uitgiften
Wanneer u een fysieke uitgiftetransactie boekt, wordt de status van de transactierecord **Ingehouden**. De volgende transacties worden beschouwd als fysieke uitgiften:

-   Productieorderverzamellijstjournaal
-   Pakbon voor verkooporder
-   Retour van pakbon voor inkooporder

Wanneer u een financiële transactie boekt, wordt de status van de transactierecord **Verkocht**. De volgende transacties worden beschouwd als financiële uitgiften:

-   Een productieorder beëindigen
-   Verkooporderfactuur
-   Leveranciersfactuur retourneren
-   Voorraadjournalen met een negatieve hoeveelheid, zoals mutaties, winst en verlies, telling, stuklijsten en overboekingen

Transacties waardoor de hoeveelheid afneemt, worden geboekt tegen het lopend gemiddelde van de kostprijs. Daarom is de procedure voor het afsluiten van voorraden vereist voor het vereffenen van uitgiftetransacties naar ontvangsttransacties op basis van het voorraadwaarderingsmodel dat aan elk artikel is gekoppeld.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]