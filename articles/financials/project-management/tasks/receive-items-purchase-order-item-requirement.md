--- 
title: Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte
description: In deze procedure ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.
author: KimANelson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: faaea6c46e83dc85e9b7efe7a9ca5c261811a3de
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="1d44e-103">Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte</span><span class="sxs-lookup"><span data-stu-id="1d44e-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d44e-104">In deze procedure ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.</span><span class="sxs-lookup"><span data-stu-id="1d44e-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="1d44e-105">Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="1d44e-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="1d44e-106">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1d44e-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1d44e-107">Ga naar Projectbeheer en boekhouding > Projecten > Alle projecten.</span><span class="sxs-lookup"><span data-stu-id="1d44e-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="1d44e-108">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d44e-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="1d44e-109">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="1d44e-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="1d44e-110">Klik op Artikelbehoeften.</span><span class="sxs-lookup"><span data-stu-id="1d44e-110">Click Item requirements.</span></span>
5. <span data-ttu-id="1d44e-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1d44e-111">Click New.</span></span>
6. <span data-ttu-id="1d44e-112">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d44e-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="1d44e-113">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1d44e-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="1d44e-114">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="1d44e-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="1d44e-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1d44e-115">Click Save.</span></span>
10. <span data-ttu-id="1d44e-116">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="1d44e-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="1d44e-117">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="1d44e-117">Click Functions.</span></span>
12. <span data-ttu-id="1d44e-118">Klik op Inkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="1d44e-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="1d44e-119">Schakel het selectievakje Opnemen in.</span><span class="sxs-lookup"><span data-stu-id="1d44e-119">Select the Include check box.</span></span>
14. <span data-ttu-id="1d44e-120">Typ of selecteer een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="1d44e-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="1d44e-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1d44e-121">Click OK.</span></span>
16. <span data-ttu-id="1d44e-122">Ga naar Leveranciers > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="1d44e-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="1d44e-123">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d44e-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="1d44e-124">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="1d44e-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="1d44e-125">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="1d44e-125">Click Confirm.</span></span>
20. <span data-ttu-id="1d44e-126">Klik in het actievenster op Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="1d44e-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="1d44e-127">Klik op Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="1d44e-127">Click Product receipt.</span></span>
22. <span data-ttu-id="1d44e-128">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d44e-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="1d44e-129">Typ een waarde in het veld Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="1d44e-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="1d44e-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1d44e-130">Click OK.</span></span>


