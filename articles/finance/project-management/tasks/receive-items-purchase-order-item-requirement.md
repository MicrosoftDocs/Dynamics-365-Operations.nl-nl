---
title: Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte
description: In dit onderwerp ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174415"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="c6ece-103">Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte</span><span class="sxs-lookup"><span data-stu-id="c6ece-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6ece-104">In dit onderwerp ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.</span><span class="sxs-lookup"><span data-stu-id="c6ece-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="c6ece-105">Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="c6ece-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="c6ece-106">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c6ece-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c6ece-107">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Projecten > Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="c6ece-108">Selecteer in de lijst de koppeling in de gewenste rij.</span><span class="sxs-lookup"><span data-stu-id="c6ece-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="c6ece-109">Selecteer **Plan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c6ece-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="c6ece-110">Selecteer **Artikelbehoeften**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="c6ece-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-111">Select **New**.</span></span>
6. <span data-ttu-id="c6ece-112">Typ of selecteer een waarde in de nieuwe rij in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="c6ece-113">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="c6ece-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="c6ece-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-114">Select **Save**.</span></span>
9. <span data-ttu-id="c6ece-115">Selecteer in het actievenster de optie **Beheren**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="c6ece-116">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-116">Select **Functions**.</span></span>
11. <span data-ttu-id="c6ece-117">Selecteer **Inkooporder maken**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="c6ece-118">Schakel het selectievakje **Alles opnemen** in.</span><span class="sxs-lookup"><span data-stu-id="c6ece-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="c6ece-119">In het veld **Leveranciersrekening** typt of selecteert u een waarde.</span><span class="sxs-lookup"><span data-stu-id="c6ece-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="c6ece-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-120">Select **OK**.</span></span>
15. <span data-ttu-id="c6ece-121">Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="c6ece-122">Selecteer in de lijst de koppeling in de gewenste rij.</span><span class="sxs-lookup"><span data-stu-id="c6ece-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="c6ece-123">Selecteer in het actievenster de optie **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="c6ece-124">Selecteer **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="c6ece-125">Selecteer **Ontvangen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c6ece-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="c6ece-126">Selecteer **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="c6ece-127">Typ een waarde in het veld **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="c6ece-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6ece-128">Select **OK**.</span></span>

