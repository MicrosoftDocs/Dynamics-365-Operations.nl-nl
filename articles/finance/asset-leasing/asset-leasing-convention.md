---
title: Conventies voor het leasen van activa
description: In dit onderwerp worden conventies voor geleasde activa beschreven.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5e0aabce46e47079b754b8ac674b205cf00b5e26
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711025"
---
# <a name="asset-leasing-conventions"></a>Conventies voor het leasen van activa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden conventies voor geleasde activa beschreven. Leasingconventies worden gebruikt om de aanvangsdatum van een leaseboek te bepalen. Als de leasingconventie is ingesteld op **Geen**, is de aanvangsdatum gelijk aan de begindatum voor de lease (dat wil zeggen de waarde van het veld **Begindatum lease**). Als de leasingconventie is ingesteld op **Volledige maand**, is de aanvangsdatum de eerste dag van de maand waarin de begindatum van de lease valt.

De aanvangsdatum bepaalt de begindatum van de periode voor de afschrijvingsschema's voor de verplichting en de afschrijving van de activa. Rente- en afschrijvingskosten worden geboekt op de einddatum van de periode van de overeenkomstige schema's. De eerste inboeking en correctie worden geboekt op de aanvangsdatum.

> [!NOTE]
> De functie voor leasingconventies moet worden ingeschakeld via Functiebeheer. Zoek in de werkruimte voor **functiebeheer** de functie **Leasingconventie voor activaleasing** en selecteer **Nu inschakelen**.

Leasingconventies worden toegewezen aan de instellingen voor een lease-activaboek.

Volg deze stappen om de leasingconventie weer te geven of toe te wijzen.

1. Ga naar **Activa leasen \> Instellen \> Leaseboeken**.
2. Selecteer in het veld **Leasingconventie** een van de volgende waarden.

    | Leaseconventie | Beschrijving |
    |--------------------|-------------|
    | None               | De afschrijvingsschema's voor de verplichting en de afschrijving van de activa begint op de begindatum van de lease, omdat de aanvangsdatum gelijk is aan de begindatum van de lease. De einddatum is één maand later. Deze leasingconventie garandeert niet dat de rente op de laatste dag van elke maand wordt geboekt. |
    | Hele maand         | Voor lease-overeenkomsten met een begindatum op een willekeurig tijdstip in de maand, beginnen de afschrijvingsschema's voor de verplichting en de afschrijving van de activa met de opbouw van de kosten op de eerste dag van die maand. Deze leasingconventie zorgt ervoor dat de rente wordt opgebouwd op de laatste dag van elke maand voor de hele maand. |

3. Selecteer **Opslaan**.

Wanneer een lease wordt gemaakt, wordt de aanvangsdatum van elk boek automatisch ingevoerd op basis van de begindatum die is ingevoerd voor de lease en de leasingconventie die is opgegeven voor het boek.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
