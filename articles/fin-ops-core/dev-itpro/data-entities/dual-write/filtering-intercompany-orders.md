---
title: Intercompany-orders filteren om synchronisatie van Orders en OrderLines te voorkomen
description: In dit onderwerp wordt uitgelegd hoe u intercompany-orders filtert, zodat de entiteiten Orders en Orderlines niet worden gesynchroniseerd.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 123427db61782490d348489c23e0eaf5f8b513c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748636"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Intercompany-orders filteren om synchronisatie van Orders en OrderLines te voorkomen

[!include [banner](../../includes/banner.md)]

U kunt intercompany-orders filteren zodat de tabellen **Orders** en **OrderLines** niet worden gesynchroniseerd. In sommige gevallen zijn de details van intercompany-orders niet nodig in een Customer Engagement-app.

Alle standaard Dataverse-tabellen worden uitgebreid via verwijzingen naar de kolom **IntercompanyOrder** en de toewijzingen voor twee keer wegschrijven worden gewijzigd zodat deze verwijzen naar de extra kolommen in de filters. Hierdoor worden de intercompany-orders niet meer gesynchroniseerd. Met dit proces worden onnodige gegevens in de Customer Engagement-app voorkomen.

1. Breid de tabel **CDS-verkooporderkoppen** uit door een verwijzing naar de kolom **IntercompanyOrder** toe te voegen. Deze kolom wordt alleen bij intercompany-orders ingevuld. De kolom **IntercompanyOrder** is beschikbaar in de tabel **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Fasering aan doelpagina toewijzen voor CDS-verkooporderkoppen":::

2. Nadat **CDS-verkooporderkoppen** is uitgebreid, is de kolom **IntercompanyOrder** beschikbaar in de toewijzing. Pas een filter toe dat `INTERCOMPANYORDER == ""` als querytekenreeks heeft.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialoogvenster Query bewerken voor CDS-verkooporderkoppen":::

3. Breid de tabel **CDS-verkooporderregels** uit door een verwijzing naar de kolom **IntercompanyInventTransId** toe te voegen. Deze kolom wordt alleen bij intercompany-orders ingevuld. De kolom **InterCompanyInventTransId** is beschikbaar in de tabel **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Fasering aan doelpagina toewijzen voor CDS-verkooporderregels":::

4. Nadat **CDS-verkooporderregels** is uitgebreid, is de kolom **IntercompanyInventTransId** beschikbaar in de toewijzing. Pas een filter toe dat `INTERCOMPANYINVENTTRANSID == ""` als querytekenreeks heeft.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialoogvenster Query bewerken voor CDS-verkooporderregels":::

5. Herhaal stap 1 en 2 om de tabel **Kopteksten van verkoopfacturen V2** uit te breiden en een filterquery toe te voegen. In dit geval gebruikt u `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` als querytekenreeks voor het filter.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Fasering aan doelpagina toewijzen voor Kopteksten van verkoopfacturen V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialoogvenster Query bewerken voor Kopteksten van verkoopfacturen V2":::

6. Herhaal stap 3 en 4 om de tabel **Verkoopfactuurregels V2** uit te breiden en een filterquery toe te voegen. In dit geval gebruikt u `INTERCOMPANYINVENTTRANSID == ""` als querytekenreeks voor het filter.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialoogvenster Query bewerken voor Verkoopfactuurregels V2":::

7. De tabel **Offertes** heeft geen intercompany-relatie. Als iemand een offerte voor een van uw intercompany-klanten maakt, kunt u de kolom **CustGroup** gebruiken om al deze klanten in één klantgroep te plaatsen. U kunt de kop en regels uitbreiden door de kolom **CustGroup** toe te voegen en vervolgens te filteren zodat de groep niet wordt opgenomen.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Fasering aan doelpagina toewijzen voor CDS-verkoopoffertekoptekst":::

8. Nadat **Offertes** is uitgebreid, past u een filter toe met `CUSTGROUP != "<company>"` als querytekenreeks.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialoogvenster Query bewerken voor CDS-verkoopoffertekoptekst":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]