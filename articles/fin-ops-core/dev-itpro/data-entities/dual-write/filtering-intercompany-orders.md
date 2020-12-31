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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="18d49-103">Intercompany-orders filteren om synchronisatie van Orders en OrderLines te voorkomen</span><span class="sxs-lookup"><span data-stu-id="18d49-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18d49-104">U kunt intercompany-orders filteren om synchronisatie van de entiteiten **Orders** en **OrderLines** te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="18d49-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="18d49-105">In sommige gevallen zijn de details van intercompany-orders nodig in de Customer Engagement-app.</span><span class="sxs-lookup"><span data-stu-id="18d49-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="18d49-106">Alle standaard Common Data Service-entiteiten worden uitgebreid met verwijzingen naar het veld **IntercompanyOrder** en de toewijzingen voor twee keer wegschrijven worden gewijzigd om te verwijzen naar de extra velden in de filters.</span><span class="sxs-lookup"><span data-stu-id="18d49-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="18d49-107">Het resultaat is dat de intercompany-orders niet meer worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="18d49-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="18d49-108">Met dit proces voorkomt u onnodige gegevens in de Customer Engagement-app.</span><span class="sxs-lookup"><span data-stu-id="18d49-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="18d49-109">Een verwijzing naar **IntercompanyOrder** toevoegen aan **CDS-verkooporderkoppen**.</span><span class="sxs-lookup"><span data-stu-id="18d49-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="18d49-110">Deze wordt alleen voor intercompany-orders ingevuld.</span><span class="sxs-lookup"><span data-stu-id="18d49-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="18d49-111">Het veld **IntercompanyOrder** is beschikbaar in **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="18d49-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Fasering aan doel toewijzen, SalesOrderHeader":::
    
2. <span data-ttu-id="18d49-113">Nadat **CDS-verkooporderkoppen** is uitgevouwen, is het veld **IntercompanyOrder** beschikbaar in de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="18d49-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="18d49-114">Een filter toepassen met `INTERCOMPANYORDER == ""` als querytekenreeks.</span><span class="sxs-lookup"><span data-stu-id="18d49-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Verkooporderkoppen, query bewerken":::

3. <span data-ttu-id="18d49-116">Voeg een verwijzing naar **IntercompanyInventTransId** toe aan **CDS-verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="18d49-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="18d49-117">Deze wordt alleen voor intercompany-orders ingevuld.</span><span class="sxs-lookup"><span data-stu-id="18d49-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="18d49-118">Het veld **InterCompanyInventTransID** is beschikbaar in **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="18d49-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Fasering aan doel toewijzen, SalesOrderLine":::

4. <span data-ttu-id="18d49-120">Nadat **CDS-verkooporderregels** is uitgevouwen, is het veld **IntercompanyInventTransId** beschikbaar in de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="18d49-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="18d49-121">Een filter toepassen met `INTERCOMPANYINVENTTRANSID == ""` als querytekenreeks.</span><span class="sxs-lookup"><span data-stu-id="18d49-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Verkooporderregels, query bewerken":::

5. <span data-ttu-id="18d49-123">Vouw **Kopteksten van verkoopfacturen V2** en **Verkoopfactuurregels V2** op dezelfde manier uit als waarop u de Common Data Service-entiteiten in stap 1 en 2 hebt uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="18d49-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="18d49-124">Voeg vervolgens de filterquery's toe.</span><span class="sxs-lookup"><span data-stu-id="18d49-124">Then add the filter queries.</span></span> <span data-ttu-id="18d49-125">De filtertekenreeks voor **Kopteksten van verkoopfacturen V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="18d49-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="18d49-126">De filtertekenreeks voor **Verkoopfactuurregels V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="18d49-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Fasering aan doel toewijzen, Kopteksten van verkoopfacturen":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Kopteksten van verkoopfacturen, query bewerken":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Verkoopfactuurregels, query bewerken":::

6. <span data-ttu-id="18d49-130">De entiteit **Offertes** heeft geen intercompany-relatie.</span><span class="sxs-lookup"><span data-stu-id="18d49-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="18d49-131">Als iemand een offerte voor een van uw intercompany-klanten maakt, kunt u al deze klanten in één klantgroep plaatsen met het veld **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="18d49-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="18d49-132">Koptekst en regels kunnen worden uitgevouwen om het veld **CustGroup** toe te voegen en vervolgens filteren om deze groep niet op te nemen.</span><span class="sxs-lookup"><span data-stu-id="18d49-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Fasering aan doel toewijzen, Verkoopoffertekoptekst":::

7. <span data-ttu-id="18d49-134">Nadat u de entiteit **Offertes** hebt uitgevouwen, past u een filter toe met `CUSTGROUP !=  "<company>"` als querytekenreeks.</span><span class="sxs-lookup"><span data-stu-id="18d49-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Verkoopoffertekoptekst, query bewerken":::
