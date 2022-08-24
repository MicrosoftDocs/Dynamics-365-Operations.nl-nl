---
title: Het wisselkoerstype en het datumtype voor de globale bronbelastingvaluta inschakelen
description: In dit artikel wordt uitgelegd hoe u de globale instellingen van het wisselkoerstype en het datumtype voor de bronbelastingvaluta kunt inschakelen.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229955"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Het wisselkoerstype en het datumtype voor de globale bronbelastingvaluta inschakelen

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u de globale instellingen van het wisselkoerstype en het datumtype voor de bronbelastingvaluta kunt inschakelen. U kunt nu een speciaal wisselkoerstype en datumtype voor de berekening van de wisselkoers voor de bronbelastingvaluta selecteren. Deze selecties bepalen de wisselkoers in vreemde valuta die wordt gebruikt om het bronbelastingbedrag in de bronbelastingvaluta in de betalingstransacties te berekenen.

Deze functionaliteit is beschikbaar in Microsoft Dynamics 365 Finance versie 10.0.29 en hoger.

1. Ga naar **Btw** \> **Instellen** \> **Parameters** \> **Grootboekparameters**.
2. Stel op het tabblad **Bronbelasting** de optie **Geavanceerde bronbelastingvaluta inschakelen** in op **Ja**.
3. Selecteer in het veld **Wisselkoerstype** een wisselkoerstype voor de bronbelastingvaluta.
4. Selecteer in het veld **Berekeningsdatumtype** een berekeningsdatumtype dat de wisselkoers voor de bronbelastingvaluta bepaalt:

    - **Betalingsdatum**: bepaal de wisselkoers op basis van de boekingsdatum van het betalingsjournaal.
    - **Factuurdatum**: bepaal de wisselkoers op basis van de factuurdatum van het factureringsjournaal. Als de factuurdatum van het boekstuk leeg is, wordt de boekingsdatum van de factuur gebruikt. 
    - **Documentdatum**: bepaal de wisselkoers op basis van de documentdatum van het betalingsjournaal. Als de documentdatum van het boekstuk leeg is, wordt de betaaldatum van de factuur gebruikt.

5. Selecteer **Opslaan**.

Als de transactievaluta verschilt van de bronbelastingvaluta die is gedefinieerd in de bronbelastingcode, wordt het bedrag in de bronbelastingvaluta berekend op basis van de transactievaluta, gebaseerd op de voorgaande instellingen, en wordt het vastgelegd in de geboekte bronbelastingtransacties.
