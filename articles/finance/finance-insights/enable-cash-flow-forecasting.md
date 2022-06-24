---
title: Cashflowprognose inschakelen
description: In dit artikel wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 253e3ea9c1c44573b37503f167b4cb3860683c10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859852"
---
# <a name="enable-cash-flow-forecasting"></a>Cashflowprognose inschakelen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Finance Insights.

> [!NOTE]
> Als u betalingsvoorspellingen in de cashflow wilt gebruiken, moet u de functie Voorspellingen klantbetalingen instellen, zoals wordt beschreven in [Voorspellingen klantbetalingen inschakelen](enable-cust-paymnt-prediction.md).
  
1. Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:

    1. Selecteer **Controleren op updates**.
    2. Zoek op het tabblad **Alle** naar **Cashflowprognoses**. Als u die functie niet kunt vinden, zoekt u naar **(Preview) Cashflowprognoses**. 
    3. Schakel de functie in.

2. Ga naar **Contanten en bankbeheer \> Instelling van cashflowprognoses** en voeg de liquiditeitsrekeningen toe die in de prognoses moeten worden opgenomen. Stel ook de liquiditeitsrekening in voor betalingen op de tabbladen **Klanten** en **Leveranciers**. Bereken de cashflowprognose opnieuw.

    > [!NOTE]
    > Als er geen liquiditeitsrekeningen zijn ingesteld, kan de cashflow niet worden gegenereerd.
    >
    > Zie [Cashflowprognose](../cash-bank-management/cash-flow-forecasting.md) voor meer informatie over het instellen van cashflowprognoses.

3. Ga naar **Contanten en bankbeheer \> Instellen \> Financiële inzichten (preview) \> Cashflowprognoses (preview)** en volg deze stappen:

    1. Selecteer op het tabblad **Cashflowprognose** de optie **Functie inschakelen**.
    2. Selecteer **Voorspellingsmodel maken**.

> [!NOTE]
> Voor de modeltraining **Cashflowprognose** zijn gegevens nodig die meer dan 100 transacties omvatten en meer dan een jaar beslaan. We raden u aan minimaal twee jaar aan gegevens met meer dan 1000 transacties te gebruiken.

Zie [Cashflowprognose](cash-flow-forecast-intro.md) voor meer informatie over de mogelijkheden voor cashflowprognoses.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
