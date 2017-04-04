---
title: "Fysieke en financiële updates"
description: Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>Fysieke en financiële updates

Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen. 

Voorraadtransacties kunnen fysiek en financieel worden bijgewerkt in Microsoft Dynamics 365 voor bewerkingen. Bepaalde typen van fysieke en financiële transacties verhogen voorraadhoeveelheden, terwijl andere de hoeveelheid verlagen.

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
Transacties waardoor de hoeveelheid toeneemt, worden geboekt tegen het lopend gemiddelde van de kostprijs. Dynamics 365 voor bewerkingen een lopende gemiddelde kostprijs berekend die is gebaseerd op de kosten van elk van deze transacties voor elke voorraaddimensie die financieel wordt bijgehouden. Voor informatie over het uitvoeren van gemiddelde kostprijzen raadpleegt u [Lopende gemiddelde kostprijs](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transacties waardoor de hoeveelheid afneemt
Dynamics 365 voor bewerkingen wordt de berekende lopend gemiddelde kostprijs gebruikt wanneer een transactie wordt geboekt, ongeacht het voorraadmodel dat is gekoppeld aan de voorraad. De transactie, waardoor de hoeveelheid afneemt, mag vóór de boeking niet worden gekoppeld aan een andere transactie. Als de fysieke voorhanden voorraad negatief wordt, Dynamics 365 for Operations de voorraadkosten gebruikt die is gedefinieerd voor het artikel op de **artikel** pagina. **Opmerking:** Als de functionaliteit voor meerdere sites is ingeschakeld, zijn deze kosten daarentegen de voorraadkosten die voor een locatie zijn gedefinieerd op de pagina **Standaard orderinstellingen**.

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


