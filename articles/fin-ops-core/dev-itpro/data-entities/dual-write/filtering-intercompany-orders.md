---
title: Intercompany-orders filteren om synchronisatie van Orders en OrderLines te voorkomen
description: In dit onderwerp wordt beschreven hoe intercompany-orders kunnen worden gefilterd om synchronisatie van Orders en OrderLines te voorkomen.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701028"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Intercompany-orders filteren om synchronisatie van Orders en OrderLines te voorkomen

[!include [banner](../../includes/banner.md)]

U kunt intercompany-orders filteren om synchronisatie van de entiteiten **Orders** en **OrderLines** te voorkomen. In sommige gevallen zijn de details van intercompany-orders nodig in de Customer Engagement-app.

Alle standaard Common Data Service-entiteiten worden uitgebreid met verwijzingen naar het veld **IntercompanyOrder** en de toewijzingen voor twee keer wegschrijven worden gewijzigd om te verwijzen naar de extra velden in de filters. Het resultaat is dat de intercompany-orders niet meer worden gesynchroniseerd. Met dit proces voorkomt u onnodige gegevens in de Customer Engagement-app.

1. Een verwijzing naar **IntercompanyOrder** toevoegen aan **CDS-verkooporderkoppen**. Deze wordt alleen voor intercompany-orders ingevuld. Het veld **IntercompanyOrder** is beschikbaar in **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Fasering aan doel toewijzen, SalesOrderHeader":::
    
2. Nadat **CDS-verkooporderkoppen** is uitgevouwen, is het veld **IntercompanyOrder** beschikbaar in de toewijzing. Een filter toepassen met `INTERCOMPANYORDER == ""` als querytekenreeks.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Verkooporderkoppen, query bewerken":::

3. Voeg een verwijzing naar **IntercompanyInventTransId** toe aan **CDS-verkooporderregels**.  Deze wordt alleen voor intercompany-orders ingevuld. Het veld **InterCompanyInventTransID** is beschikbaar in **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Fasering aan doel toewijzen, SalesOrderLine":::

4. Nadat **CDS-verkooporderregels** is uitgevouwen, is het veld **IntercompanyInventTransId** beschikbaar in de toewijzing. Een filter toepassen met `INTERCOMPANYINVENTTRANSID == ""` als querytekenreeks.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Verkooporderregels, query bewerken":::

5. Vouw **Kopteksten van verkoopfacturen V2** en **Verkoopfactuurregels V2** op dezelfde manier uit als waarop u de Common Data Service-entiteiten in stap 1 en 2 hebt uitgevouwen. Voeg vervolgens de filterquery's toe. De filtertekenreeks voor **Kopteksten van verkoopfacturen V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. De filtertekenreeks voor **Verkoopfactuurregels V2** is `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Fasering aan doel toewijzen, Kopteksten van verkoopfacturen":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Kopteksten van verkoopfacturen, query bewerken":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Verkoopfactuurregels, query bewerken":::

6. De entiteit **Offertes** heeft geen intercompany-relatie. Als iemand een offerte voor een van uw intercompany-klanten maakt, kunt u al deze klanten in één klantgroep plaatsen met het veld **CustGroup**.  Koptekst en regels kunnen worden uitgevouwen om het veld **CustGroup** toe te voegen en vervolgens filteren om deze groep niet op te nemen.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Fasering aan doel toewijzen, Verkoopoffertekoptekst":::

7. Nadat u de entiteit **Offertes** hebt uitgevouwen, past u een filter toe met `CUSTGROUP !=  "<company>"` als querytekenreeks.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Verkoopoffertekoptekst, query bewerken":::
