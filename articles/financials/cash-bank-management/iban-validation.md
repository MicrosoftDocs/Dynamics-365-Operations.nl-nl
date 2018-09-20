---
title: IBAN-rekeningvalidatie (International Bank Account Number) account beheren
description: In dit onderwerp wordt uitgelegd hoe u IBAN-rekeningvalidatie (International Bank Account Number) kunt beheren.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: nl-nl
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>IBAN-rekeningvalidatie (International Bank Account Number) account beheren

[!include [banner](../includes/banner.md)]

Met IBAN-rekeningvalidatie (International Bank Account Number) wordt meer validatie uitgevoerd wanneer u een IBAN aan een bankrekening toevoegt.

De structuur van het IBAN is opgeslagen in Microsoft Dynamics 365 for Finance and Operation en wordt automatisch geladen wanneer u het IBAN voor het eerst voor bankrekeningen gebruikt. Het bankrekeningnummer is onderdeel van de structuur die is gedefinieerd voor een IBAN-nummer. Op basis van die structuur ontvangt u waarschuwingsberichten als de positie en de lengte van het rekeningnummer in het IBAN niet overeenkomen met de positie die is gedefinieerd in de structuur voor elk land of regio.

## <a name="set-up-iban-structures"></a>IBAN-structuren instellen

1. Ga naar **Contanten en bankbeheer \> Instellen \> IBAN-structuren**.
2. U ziet dat de IBAN-structuren voor elk land of elke regio automatisch zijn ingesteld.
3. Als u de structuren voor een bepaald land of bepaalde regio moet aanpassen moet, kunt u ze bewerken.
4. De structuurdefinities maken deel uit van elke nieuwe release. U kunt het menu **Structuren opnieuw instellen** gebruiken om de nieuwste definities na elke update te laden.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>De IBAN-structuur in een bankrekening valideren

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Maak een bankrekening.
3. Voer op het sneltabblad **Aanvullende gegevens** een IBAN op.

    Als de positie en de lengte van het rekeningnummer in het IBAN niet overeenkomen met de positie die is gedefinieerd in de structuur voor elk land of elke regio, ontvangt u een bericht. U kunt niet verdergaan als de lengte van het IBAN niet overeenkomt met de lengte in de IBAN-structuur.

    Met de validatie wordt ook geverifieerd of het bankrekeningnummer overeenkomt met het deel van het IBAN waarmee het bankrekeningnummer wordt vertegenwoordigd. Als het bankrekeningnummer niet overeenkomt, ontvangt u een waarschuwingsbericht. Dit bericht is slechts een waarschuwing. U kunt toch verdergaan, ook als het bankrekeningnummer niet overeenkomt.

