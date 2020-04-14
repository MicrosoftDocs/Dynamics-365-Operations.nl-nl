---
title: Een batchtaak maken
description: Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143668"
---
# <a name="create-a-batch-job"></a>Een batchtaak maken

[!include [banner](../../includes/banner.md)]

Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden. Batchtaken worden uitgevoerd met behulp van de beveiligingsgegevens van de gebruiker die de taak heeft gemaakt. Voer de volgende procedure uit om een batchtaak te maken. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-the-batch-job"></a>De batchtaak maken
1. Ga naar **Navigatievenster > Modules > Systeembeheer > Query's > Batchtaken**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Taakomschrijving**.
4. Typ een datum en een tijd in het veld **Geplande begindatum/tijd**.
5. Klik op **Opslaan**.

## <a name="create-a-recurrence"></a>Een terugkeerpatroon maken
1. Klik in het actievenster op **Batchtaak**.
2. Klik op **Terugkeerpatroon**. Gebruik deze opties om een bereik en terugkeerpatroon in te voeren.  
3. Klik op **OK**.

## <a name="add-alerts"></a>Waarschuwingen toevoegen
1. Klik in het actievenster op **Batchtaak**.
2. Klik op **Waarschuwingen**. Geef aan of u waarschuwingsberichten wilt laten verzenden wanneer de batchtaak is voltooid, wanneer er een fout optreedt of wanneer de batchtaak wordt geannuleerd. Geef vervolgens op of u waarschuwingen wilt laten weergeven als pop-upberichten.   
3. Klik op **OK**.

## <a name="adjust-batch-job-status"></a>Status van batchtaak aanpassen
1. Ga naar **Systeembeheer > Query's > Batchtaken**.
2. Selecteer de gewenste batchtaak.
3. Klik in het actievenster op **Batchtaak > Functies > Status wijzigen**.
4. Selecteer de gewenste status:
    - **Inhouden**: stel de batchtaak in op **Inhouden**, zodat deze niet wordt opgenomen in de planner van batchtaken. Staat gelijk aan *Stoppen*.
    - **Wachten**: stel de batchtaak in op **Wachten** om deze in de wachtrij voor de planner van batchtaken te zetten. Staat gelijk aan *Gaan*.
5. Klik op **OK**.
