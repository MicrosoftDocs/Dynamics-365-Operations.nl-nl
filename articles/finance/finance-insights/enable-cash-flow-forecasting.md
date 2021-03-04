---
title: Cashflowprognose inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Financiële inzichten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 321c716c10b136769ea3a48a3b60a8a717798338
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646224"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Cashflowprognose inschakelen (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Financiële inzichten.

> [!NOTE]
> Als u betalingsvoorspellingen in de cashflow wilt gebruiken, moet u de functie Voorspellingen klantbetalingen instellen, zoals wordt beschreven in [Voorspellingen klantbetalingen inschakelen](enable-cust-paymnt-prediction.md).

1. Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving. Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving. (Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Als uw implementatie van Microsoft Dynamics 365 Finance een Service Fabric-implementatie is, kunt u deze stap overslaan. Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld. Als de functies niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt wanneer u deze wilt inschakelen, neemt u contact op met <fiap@microsoft.com>.
  
2. Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:

    1. Selecteer **Controleren op updates**.
    2. De volgende functies inschakelen:

        - Nieuw rasterbesturingselement
        - Groeperen in rasters (preview) 
        - Betalingsvoorspellingen voor klanten (preview)
        - Cashflowprognoses (preview)

3. Ga naar **Contanten en bankbeheer \> Instelling van cashflowprognoses** en voeg de liquiditeitsrekeningen toe die in de prognoses moeten worden opgenomen.

    > [!NOTE]
    > Als er geen liquiditeitsrekeningen zijn ingesteld, kan de cashflow niet worden gegenereerd.

4. Ga naar **Contanten en bankbeheer \> Instellen \> Financiële inzichten (preview) \> Cashflowprognoses (preview)** en volg deze stappen:

    1. Selecteer op het tabblad **Cashflowprognose** de optie **Functie inschakelen**.
    2. Selecteer **Voorspellingsmodel maken**.

Zie [Cashflowprognose](cash-flow-forecast-intro.md) voor meer informatie over de mogelijkheden voor cashflowprognoses.

## <a name="privacy-notice"></a>Privacyverklaring

Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.