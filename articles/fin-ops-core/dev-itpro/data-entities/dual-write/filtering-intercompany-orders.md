---
title: Intercompany-orders filteren om synchronisatie van Orders en OrderLines te voorkomen
description: In dit onderwerp wordt uitgelegd hoe u intercompany-orders filtert, zodat de entiteiten Orders en Orderlines niet worden gesynchroniseerd.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 342db8c1b4337145bfd61f5698ff6de25434a400
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796601"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="c7b2b-103">Intercompany-orders filteren om synchronisatie van Orders en OrderLines te voorkomen</span><span class="sxs-lookup"><span data-stu-id="c7b2b-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7b2b-104">U kunt intercompany-orders filteren zodat de tabellen **Orders** en **OrderLines** niet worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="c7b2b-105">In sommige gevallen zijn de details van intercompany-orders niet nodig in een Customer Engagement-app.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="c7b2b-106">Alle standaard Dataverse-tabellen worden uitgebreid via verwijzingen naar de kolom **IntercompanyOrder** en de toewijzingen voor twee keer wegschrijven worden gewijzigd zodat deze verwijzen naar de extra kolommen in de filters.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="c7b2b-107">Hierdoor worden de intercompany-orders niet meer gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="c7b2b-108">Met dit proces worden onnodige gegevens in de Customer Engagement-app voorkomen.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="c7b2b-109">Breid de tabel **CDS-verkooporderkoppen** uit door een verwijzing naar de kolom **IntercompanyOrder** toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="c7b2b-110">Deze kolom wordt alleen bij intercompany-orders ingevuld.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="c7b2b-111">De kolom **IntercompanyOrder** is beschikbaar in de tabel **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Fasering aan doelpagina toewijzen voor CDS-verkooporderkoppen":::

2. <span data-ttu-id="c7b2b-113">Nadat **CDS-verkooporderkoppen** is uitgebreid, is de kolom **IntercompanyOrder** beschikbaar in de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="c7b2b-114">Pas een filter toe dat `INTERCOMPANYORDER == ""` als querytekenreeks heeft.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialoogvenster Query bewerken voor CDS-verkooporderkoppen":::

3. <span data-ttu-id="c7b2b-116">Breid de tabel **CDS-verkooporderregels** uit door een verwijzing naar de kolom **IntercompanyInventTransId** toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="c7b2b-117">Deze kolom wordt alleen bij intercompany-orders ingevuld.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="c7b2b-118">De kolom **InterCompanyInventTransId** is beschikbaar in de tabel **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Fasering aan doelpagina toewijzen voor CDS-verkooporderregels":::

4. <span data-ttu-id="c7b2b-120">Nadat **CDS-verkooporderregels** is uitgebreid, is de kolom **IntercompanyInventTransId** beschikbaar in de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="c7b2b-121">Pas een filter toe dat `INTERCOMPANYINVENTTRANSID == ""` als querytekenreeks heeft.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialoogvenster Query bewerken voor CDS-verkooporderregels":::

5. <span data-ttu-id="c7b2b-123">Herhaal stap 1 en 2 om de tabel **Kopteksten van verkoopfacturen V2** uit te breiden en een filterquery toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="c7b2b-124">In dit geval gebruikt u `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` als querytekenreeks voor het filter.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Fasering aan doelpagina toewijzen voor Kopteksten van verkoopfacturen V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialoogvenster Query bewerken voor Kopteksten van verkoopfacturen V2":::

6. <span data-ttu-id="c7b2b-127">Herhaal stap 3 en 4 om de tabel **Verkoopfactuurregels V2** uit te breiden en een filterquery toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="c7b2b-128">In dit geval gebruikt u `INTERCOMPANYINVENTTRANSID == ""` als querytekenreeks voor het filter.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialoogvenster Query bewerken voor Verkoopfactuurregels V2":::

7. <span data-ttu-id="c7b2b-130">De tabel **Offertes** heeft geen intercompany-relatie.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="c7b2b-131">Als iemand een offerte voor een van uw intercompany-klanten maakt, kunt u de kolom **CustGroup** gebruiken om al deze klanten in één klantgroep te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="c7b2b-132">U kunt de kop en regels uitbreiden door de kolom **CustGroup** toe te voegen en vervolgens te filteren zodat de groep niet wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Fasering aan doelpagina toewijzen voor CDS-verkoopoffertekoptekst":::

8. <span data-ttu-id="c7b2b-134">Nadat **Offertes** is uitgebreid, past u een filter toe met `CUSTGROUP != "<company>"` als querytekenreeks.</span><span class="sxs-lookup"><span data-stu-id="c7b2b-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialoogvenster Query bewerken voor CDS-verkoopoffertekoptekst":::
