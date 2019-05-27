---
title: De ontvangst van goederen registreren voor de inkooporder
description: Deze procedure laat zien hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551901"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="1d7f1-103">De ontvangst van goederen registreren voor de inkooporder</span><span class="sxs-lookup"><span data-stu-id="1d7f1-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d7f1-104">Deze procedure laat zien hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="1d7f1-105">Het is ook mogelijk om de productontvangst in het magazijn te registreren en deze later vast te leggen voor de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="1d7f1-106">Deze taak wordt gewoonlijk uitgevoerd door een inkoper of een leverancierscoördinator.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="1d7f1-107">Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="1d7f1-108">Het voorbeeld bevat stappen om een eenvoudige inkooporder te maken zodat u de procedure als taakbegeleiding kunt afspelen.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="1d7f1-109">Als u de procedure op uw eigen gegevens gebruikt, begint u bij de subtaak Ontvangst van goederen registreren.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="1d7f1-110">Een nieuwe inkooporder voor de ontvangst van goederen voorbereiden</span><span class="sxs-lookup"><span data-stu-id="1d7f1-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="1d7f1-111">Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="1d7f1-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-112">Click New.</span></span>
3. <span data-ttu-id="1d7f1-113">Typ in het veld Leveranciersrekening de waarde US-101.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="1d7f1-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-114">Click OK.</span></span>
5. <span data-ttu-id="1d7f1-115">Voer M0001 in het veld Artikelnummer in.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="1d7f1-116">Typ 5 in het veld Hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="1d7f1-117">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="1d7f1-118">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="1d7f1-119">Ontvangst van goederen registreren</span><span class="sxs-lookup"><span data-stu-id="1d7f1-119">Record receipt of goods</span></span>
1. <span data-ttu-id="1d7f1-120">Klik in het actievenster op Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="1d7f1-121">Klik op Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-121">Click Product receipt.</span></span>
    * <span data-ttu-id="1d7f1-122">Met het veld Hoeveelheid kunt u verschillende opties voor de hoeveelheid selecteren die u wilt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="1d7f1-123">Als bijvoorbeeld eerder een hoeveelheid in het magazijn is geregistreerd, kunt u Geregistreerde hoeveelheid selecteren.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="1d7f1-124">Gebruik de waarde van Bestelde hoeveelheid voor dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="1d7f1-125">Typ een willekeurige waarde in het veld Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="1d7f1-126">Dit veld wordt gebruikt om een verwijzing in te voeren die als het boekstuk voor productontvangstbonjournaal wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="1d7f1-127">Vouw de sectie Regels uit.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="1d7f1-128">Stel Hoeveelheid in op '4'.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="1d7f1-129">Hier kunt u handmatig de hoeveelheid opgeven die voor elke regel in de order wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="1d7f1-130">Vouw de sectie Regels samen.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="1d7f1-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-131">Click OK.</span></span>
    * <span data-ttu-id="1d7f1-132">De goederen zijn nu geregistreerd zo ontvangen voor de inkooporder, en er is een productontvangstbonjournaal gemaakt als document om dit te reflecteren.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="1d7f1-133">U kunt de actie Productontvangstbon gebruiken om de journalen te controleren die bij de inkooporder zijn gemaakt en om te zien wat is ontvangen, en wanneer.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

