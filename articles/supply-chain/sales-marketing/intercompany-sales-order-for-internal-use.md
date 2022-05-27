---
title: Een intercompany-verkooporder voor intern gebruik maken
description: In dit onderwerp wordt uitgelegd hoe u een intercompany-verkooporder voor intern gebruik maakt
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
ms.openlocfilehash: 9b4d2dc450fb5996e0e08c92836c1d1942a05b73
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673685"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Een intercompany-verkooporder voor intern gebruik maken

[!include [banner](../../includes/banner.md)]

Een intercompany-verkooporder wordt meestal automatisch op basis van een intercompany-inkooporder gemaakt. U kunt ook handmatig een intercompany-verkooporder maken, waarmee vervolgens een intercompany-inkooporder wordt gegenereerd in de rechtspersoon van de intercompany-klant.

![Intern intercompany-verkoopproces](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Handmatig een intercompany-verkooporder maken

Voer deze stappen uit in rechtspersoon B, zoals getoond in de afbeelding.

1. Ga naar **Klanten \> Verkooporders \> Alle verkooporders**.
1. Selecteer in het actievenster **Verkooporder** om een verkooporder te maken.
1. Selecteer op de pagina **Verkooporder maken** een klantrekening. Zorg ervoor dat op het sneltabblad **Algemeen** het selectievakje **Intercompany** is ingeschakeld. Dit geeft aan dat de geselecteerde klant een intercompany-klant is.
1. Voer de gegevens in of wijzig de bestaande gegevens, selecteer **OK** en maak de orderregels zoals gewoonlijk.

    De veldwaarde **Afleveradres** in de kop van de intercompany-verkooporder wordt gekopieerd naar de kop van de intercompany-inkooporder. De veldwaarde **Artikelnummer**, inclusief productdimensies, en de veldwaarden **Leveringsdatum** en **Valutacode** in de intercompany-verkooporderregels worden gekopieerd naar de intercompany-inkooporderregels.

1. Selecteer in de orderkoptekst **Intercompany** om de gerelateerde intercompany-inkooporder weer te geven.
1. Selecteer in de orderregels **Intercompany** om informatie over voorhanden voorraad voor intercompany-handel weer te geven.

> [!TIP]
> U kunt intercompany-verkooporders weergeven op de pagina **Intercompany-orders**.

> [!NOTE]
> Wanneer u met intercompany werkt, is het raadzaam om het selectievakje **Order verwijderen na facturering** uit te schakelen op de pagina **Parameters van module Klanten**. Als u dit niet doet, wordt de bijbehorende inkooporder verwijderd. U wordt ook aangeraden om het selectievakje **Inkooporder verwijderen na facturering** uit te schakelen op de pagina **Parameters van module Klanten**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
