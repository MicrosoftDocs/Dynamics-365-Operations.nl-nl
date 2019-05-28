---
title: IBAN-rekeningvalidatie (International Bank Account Number) account beheren
description: In dit onderwerp wordt uitgelegd hoe u IBAN-rekeningvalidatie (International Bank Account Number) kunt beheren.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 19e0528b95952de8e5503c361efcfeca4c529caf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573417"
---
# <a name="manage-international-bank-account-number-iban-validation"></a>IBAN-validatie (International Bank Account Number) beheren

[!include [banner](../includes/banner.md)]

Met IBAN-validatie (International Bank Account Number) wordt meer validatie uitgevoerd wanneer u een IBAN aan een bankrekening toevoegt.

Informatie over de structuur van het IBAN wordt opgeslagen in Microsoft Dynamics 365 for Finance and Operations. Deze informatie wordt automatisch geladen wanneer u voor het eerst het IBAN voor bankrekeningen gebruikt. Het bevat de lengte van het IBAN, de beginposities van het bankrekeningnummer en het routenummer en de lengte van het bankrekeningnummer en het routenummer.

## <a name="set-up-iban-structures"></a>IBAN-structuren instellen

1. Ga naar **Contanten en bankbeheer \> Instellen \> IBAN-structuren**.
2. U ziet dat de IBAN-structuren voor elk land of elke regio automatisch zijn ingesteld.
3. Als u de structuren voor een bepaald land of bepaalde regio wilt aanpassen, kunt u ze bewerken.
4. De structuurdefinities maken deel uit van elke nieuwe release. U kunt het menu **Structuren opnieuw instellen** gebruiken om de nieuwste definities na elke update te laden.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>De IBAN-structuur in een bankrekening valideren

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Maak een bankrekening.
3. Voer op het sneltabblad **Aanvullende gegevens** een IBAN op.

    Als de lengte van het IBAN niet overeenkomt met de lengte die is gedefinieerd voor elk land of regio, ontvangt u een waarschuwingsbericht. U kunt niet verdergaan als de lengte van het IBAN niet overeenkomt met de lengte die is opgegeven in de IBAN-structuur.

    Met de validatie wordt ook geverifieerd of het bankrekeningnummer overeenkomt met het deel van het IBAN waarmee het bankrekeningnummer wordt vertegenwoordigd. Als het bankrekeningnummer niet overeenkomt, ontvangt u een waarschuwingsbericht. Dit bericht is slechts een waarschuwing. U kunt toch verdergaan, ook als het bankrekeningnummer niet overeenkomt.

    Met de validatie wordt ook geverifieerd of het bankrouteringsnummer overeenkomt met het deel van het IBAN waarmee het bankrouteringsnummer wordt vertegenwoordigd. Het routenummer bevat een banknummer en vaak een aanvullend filiaalnummer. Als het bankrouteringsnummer niet overeenkomt, ontvangt u een waarschuwingsbericht. Dit bericht is slechts een waarschuwing. U kunt toch verdergaan, ook als het bankrouteringsnummer niet overeenkomt.
