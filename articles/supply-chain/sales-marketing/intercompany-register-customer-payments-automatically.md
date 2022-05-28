---
title: Betalingen automatisch registreren voor intercompany-klantfacturen
description: In dit onderwerp wordt uitgelegd hoe u betalingen automatisch registreert voor intercompany-klantfacturen
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: dbd06b21d736d1e247cd087e5bb86fbe641352e6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669427"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Betalingen automatisch registreren voor intercompany-klantfacturen

[!include [banner](../../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management wordt een klanttransactie gemaakt als een intercompany-klantfactuur wordt geboekt. Deze klanttransactie blijft open tot deze wordt vereffend, wat wil zeggen dat deze is betaald. Als de factuur van de bijbehorende intercompany-inkooporder wordt bijgewerkt, wordt een leverancierstransactie gemaakt die overeenkomt met de klanttransactie. Deze leverancierstransactie blijft ook open tot deze wordt vereffend. Om het risico op verschillen te vermindere, kan automatisch een klantbetalingsjournaal worden gemaakt en geboekt wanneer het leveranciersbetalingsjournaal wordt geboekt.

1. Ga naar **Verkoop en marketing \> Klanten \> Alle klanten**.
1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Intercompany**.
1. Als u de intercompany-klantbetalingen wilt instellen op de pagina **Intercompany** voor verkooporders, selecteert u de koppeling **Verkooporderbeleid**.
1. Selecteer in het veld **Betalingsjournaal** het klantbetalingsjournaal waarin u intercompany-leveranciersbetalingen wilt registreren. U kunt dit instellen op de pagina **Parameters van module Klanten**.
1. Als u automatisch naar dit journaal wilt boeken, selecteert u het selectievakje **Journaal automatisch boeken**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
