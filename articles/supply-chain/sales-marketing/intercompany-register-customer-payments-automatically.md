---
title: Betalingen automatisch registreren voor intercompany-klantfacturen
description: In dit onderwerp wordt uitgelegd hoe u betalingen automatisch registreert voor intercompany-klantfacturen
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ffc5c7bf44989fbcc18e940b5a7c9df81260d770
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548200"
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
