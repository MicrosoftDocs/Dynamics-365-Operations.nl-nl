---
title: Intercompany-klantgegevens synchroniseren
description: In dit onderwerp wordt de synchronisatie van klantgegevens voor intercompany-orders beschreven.
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
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548198"
---
# <a name="synchronize-intercompany-customer-information"></a>Intercompany-klantgegevens synchroniseren

[!include [banner](../../includes/banner.md)]

Klantgegevens worden gesynchroniseerd als het veld **Klantgegevens** is ingeschakeld wanneer de verkooporder wordt gemaakt of wanneer er een wijziging wordt aangebracht in de klantverwijzing, leverancierverwijzing of het bestelopdrachtnummer van de klant.

U kunt de waarde in deze synchronisatievelden altijd wijzigen. U kunt echter alleen bepalen of deze waarde naar de andere intercompany-orders wordt gekopieerd door deze parameter te selecteren. Als u het veld **Klantgegevens** hebt ingeschakeld op de intercompany-verkooporder, wordt een wijziging in de intercompany-verkooporder gesynchroniseerd met de intercompany-inkooporder. Als u het veld **Klantgegevens** ook hebt ingeschakeld op de intercompany-inkooporder, wordt de wijziging ook terug naar de oorspronkelijke verkooporder gesynchroniseerd.

> [!NOTE]
> Als u het veld **Klantgegevens** hebt ingeschakeld op zowel de intercompany-inkooporder als de intercompany-verkooporder, worden updates die door een persoon in een bedrijf zijn aangebracht, overschreven door updates die door een andere persoon in een ander bedrijf zijn aangebracht op dezelfde order.

De beste manier is om het veld **Klantgegevens** op de intercompany-inkooporder in te schakelen. Op die manier wordt synchronisatie ingeschakeld tussen de oorspronkelijke verkooporder en de intercompany-inkooporder en tussen de intercompany-inkooporder en de intercompany-verkooporder.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]