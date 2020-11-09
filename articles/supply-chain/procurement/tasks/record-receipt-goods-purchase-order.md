---
title: De ontvangst van goederen registreren voor de inkooporder
description: In dit onderwerp wordt uitgelegd hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd8ca2cbd24f326c4eaf9cd39e32de0eca81149d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018601"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="58757-103">De ontvangst van goederen registreren voor de inkooporder</span><span class="sxs-lookup"><span data-stu-id="58757-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58757-104">In dit onderwerp wordt uitgelegd hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren.</span><span class="sxs-lookup"><span data-stu-id="58757-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="58757-105">Het is ook mogelijk om de productontvangst in het magazijn te registreren en deze later vast te leggen voor de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="58757-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="58757-106">Deze taak wordt gewoonlijk uitgevoerd door een inkoper of een leverancierscoördinator.</span><span class="sxs-lookup"><span data-stu-id="58757-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="58757-107">Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf.</span><span class="sxs-lookup"><span data-stu-id="58757-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="58757-108">Het voorbeeld bevat stappen om een eenvoudige inkooporder te maken zodat u de procedure als taakbegeleiding kunt afspelen.</span><span class="sxs-lookup"><span data-stu-id="58757-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="58757-109">Als u de procedure met uw eigen gegevens gebruikt, begint u bij de subtaak **Ontvangst van goederen registreren**.</span><span class="sxs-lookup"><span data-stu-id="58757-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="58757-110">Een nieuwe inkooporder voor de ontvangst van goederen voorbereiden</span><span class="sxs-lookup"><span data-stu-id="58757-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="58757-111">Ga naar **Navigatievenster > Modules > Inkoopbeheer > Inkooporders > Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="58757-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="58757-112">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="58757-112">Select **New**.</span></span>
3. <span data-ttu-id="58757-113">Typ `US-101` in het veld **Leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="58757-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="58757-114">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="58757-114">Select **OK**.</span></span>
5. <span data-ttu-id="58757-115">Typ `M0001` in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="58757-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="58757-116">Typ `5` in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="58757-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="58757-117">Selecteer in het actievenster de optie **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="58757-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="58757-118">Selecteer **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="58757-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="58757-119">Ontvangst van goederen registreren</span><span class="sxs-lookup"><span data-stu-id="58757-119">Record receipt of goods</span></span>
1. <span data-ttu-id="58757-120">Selecteer **Ontvangen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="58757-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="58757-121">Selecteer **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="58757-121">Select **Product receipt**.</span></span> <span data-ttu-id="58757-122">In het veld **Hoeveelheid** kunt u verschillende opties selecteren voor de hoeveelheid die u wilt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="58757-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="58757-123">Als bijvoorbeeld eerder een hoeveelheid in het magazijn is geregistreerd, kunt u **Geregistreerde hoeveelheid** selecteren.</span><span class="sxs-lookup"><span data-stu-id="58757-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="58757-124">Gebruik voor dit voorbeeld de waarde van **Bestelde hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="58757-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="58757-125">Vouw de sectie **Overzicht** uit.</span><span class="sxs-lookup"><span data-stu-id="58757-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="58757-126">Typ een willekeurige waarde in het veld **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="58757-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="58757-127">Dit veld wordt gebruikt om een verwijzing in te voeren die als het boekstuk voor productontvangstbonjournaal wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="58757-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="58757-128">Vouw de sectie **Regels** uit.</span><span class="sxs-lookup"><span data-stu-id="58757-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="58757-129">Stel **Hoeveelheid** in op '4'.</span><span class="sxs-lookup"><span data-stu-id="58757-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="58757-130">Hier kunt u handmatig de hoeveelheid opgeven die voor elke regel in de order wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="58757-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="58757-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="58757-131">Select **OK**.</span></span> <span data-ttu-id="58757-132">De goederen zijn nu geregistreerd zo ontvangen voor de inkooporder, en er is een productontvangstbonjournaal gemaakt als document om dit te reflecteren.</span><span class="sxs-lookup"><span data-stu-id="58757-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="58757-133">U kunt de actie Productontvangstbon gebruiken om de journalen te controleren die bij de inkooporder zijn gemaakt en om te zien wat is ontvangen, en wanneer.</span><span class="sxs-lookup"><span data-stu-id="58757-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

