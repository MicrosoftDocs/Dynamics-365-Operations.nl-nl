---
title: IBAN-rekeningvalidatie (International Bank Account Number) account beheren
description: In dit artikel wordt uitgelegd hoe u IBAN-rekeningvalidatie (International Bank Account Number) kunt beheren.
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 3d825e8699fbe10e080cd85f15d3d86f8c780f15
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880894"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>IBAN-rekeningvalidatie (International Bank Account Number) account beheren

[!include [banner](../includes/banner.md)]

Met IBAN-validatie (International Bank Account Number) wordt meer validatie uitgevoerd wanneer u een IBAN aan een bankrekening toevoegt.

Informatie over de structuur van de IBAN wordt opgeslagen in Microsoft Microsoft Dynamics 365 Finance en wordt automatisch geladen wanneer u IBAN voor het eerst gebruikt op bankrekeningen. Het bevat de lengte van het IBAN, de beginposities van het bankrekeningnummer en het routenummer en de lengte van het bankrekeningnummer en het routenummer.

## <a name="set-up-iban-structures"></a>IBAN-structuren instellen

1. Ga naar **Contanten en bankbeheer \> Instellen \> IBAN-structuren**.
2. U ziet dat de IBAN-structuren voor elk land of elke regio automatisch zijn ingesteld.
3. Selecteer de knop **Bewerken** als de structuur moet worden bijgewerkt voor een bepaald land of een bepaalde regio.
4. De structuurdefinities maken deel uit van elke nieuwe release. U kunt het menu **Structuren opnieuw instellen** gebruiken om de nieuwste definities na elke update te laden.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>De IBAN-structuur in een bankrekening valideren

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Maak een bankrekening.
3. Voer op het sneltabblad **Aanvullende gegevens** een IBAN op.

    Als de lengte van het IBAN niet overeenkomt met de lengte die is gedefinieerd voor elk land of regio, ontvangt u een waarschuwingsbericht. U kunt niet verdergaan als de lengte van het IBAN niet overeenkomt met de lengte die is opgegeven in de IBAN-structuur.

    Met de validatie wordt ook geverifieerd of het bankrekeningnummer overeenkomt met het deel van het IBAN waarmee het bankrekeningnummer wordt vertegenwoordigd. Als het bankrekeningnummer niet overeenkomt, ontvangt u een waarschuwingsbericht. Dit bericht is slechts een waarschuwing. U kunt toch verdergaan, ook als het bankrekeningnummer niet overeenkomt.

    Met de validatie wordt ook geverifieerd of het bankrouteringsnummer overeenkomt met het deel van het IBAN waarmee het bankrouteringsnummer wordt vertegenwoordigd. Het routenummer bevat een banknummer en vaak een aanvullend filiaalnummer. Als het bankrouteringsnummer niet overeenkomt, ontvangt u een waarschuwingsbericht. Dit bericht is slechts een waarschuwing. U kunt toch verdergaan, ook als het bankrouteringsnummer niet overeenkomt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
