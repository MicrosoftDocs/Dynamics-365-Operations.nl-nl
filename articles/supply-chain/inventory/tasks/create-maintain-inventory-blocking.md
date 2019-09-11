---
title: Een voorraadblokkering maken en beheren
description: Deze procedure laat zien hoe wordt voorkomen dat fysieke voorhanden voorraad kan worden gereserveerd door andere uitgaande brondocumenten met behulp van de voorraadblokkering.
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2485eaf31226b11106895074ae0ad95e561777b
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916594"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="efa6a-103">Een voorraadblokkering maken en beheren</span><span class="sxs-lookup"><span data-stu-id="efa6a-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="efa6a-104">Deze procedure laat zien hoe wordt voorkomen dat fysieke voorhanden voorraad kan worden gereserveerd door andere uitgaande brondocumenten met behulp van de voorraadblokkering.</span><span class="sxs-lookup"><span data-stu-id="efa6a-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="efa6a-105">U kunt de procedure uitvoeren in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="efa6a-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="efa6a-106">U moet een artikel met fysieke beschikbare voorhanden voorraad hebben voordat u deze procedure start.</span><span class="sxs-lookup"><span data-stu-id="efa6a-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="efa6a-107">Een voorraadblokkering maken</span><span class="sxs-lookup"><span data-stu-id="efa6a-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="efa6a-108">Ga in het **navigatievenster** naar **Modules > Voorraadbeheer > Periodieke taken > Voorraadblokkering**.</span><span class="sxs-lookup"><span data-stu-id="efa6a-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="efa6a-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="efa6a-109">Click **New**.</span></span>
3. <span data-ttu-id="efa6a-110">Klik in het veld **Artikelnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="efa6a-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="efa6a-111">Selecteer in de lijst het artikel dat u wilt kiezen.</span><span class="sxs-lookup"><span data-stu-id="efa6a-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="efa6a-112">Selecteer een artikelnummer met fysieke voorhanden voorraad die u wilt blokkeren.</span><span class="sxs-lookup"><span data-stu-id="efa6a-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="efa6a-113">Als u USMF gebruikt, kunt u artikel M9201 selecteren.</span><span class="sxs-lookup"><span data-stu-id="efa6a-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="efa6a-114">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="efa6a-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="efa6a-115">Als u artikel M9201 gebruikt, moet u minder dan 200 selecteren.</span><span class="sxs-lookup"><span data-stu-id="efa6a-115">If you’re using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="efa6a-116">Vouw het sneltabblad **Voorraaddimensies** uit.</span><span class="sxs-lookup"><span data-stu-id="efa6a-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="efa6a-117">Klik in het veld **Magazijn** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="efa6a-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="efa6a-118">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="efa6a-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="efa6a-119">Als u artikel M9201 gebruikt, kunt u magazijn 51 selecteren.</span><span class="sxs-lookup"><span data-stu-id="efa6a-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="efa6a-120">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="efa6a-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="efa6a-121">De voorwaarden van de voorraadblokkering bijwerken</span><span class="sxs-lookup"><span data-stu-id="efa6a-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="efa6a-122">Voer op het sneltabblad **Algemeen** in het veld **Hoeveelheid** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="efa6a-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="efa6a-123">Werk het veld van de voorraadhoeveelheid bij om de te blokkeren hoeveelheid aan te geven.</span><span class="sxs-lookup"><span data-stu-id="efa6a-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="efa6a-124">Voer in het veld **Verwachte datum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="efa6a-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="efa6a-125">U kunt bijvoorbeeld aangeven wanneer de geblokkeerde voorraad naar verwachting beschikbaar komt voor reservering door een verwachte datum toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="efa6a-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="efa6a-126">Als de optie Verwachte ontvangsten is geselecteerd voor de voorraadblokkering, zoals standaard het geval is wanneer u handmatig een blokkering uitvoert, wordt deze datum op de verwachte transactie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="efa6a-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="efa6a-127">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="efa6a-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="efa6a-128">De voorraadblokkering verwijderen</span><span class="sxs-lookup"><span data-stu-id="efa6a-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="efa6a-129">Klik in het **actievenster** op **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="efa6a-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="efa6a-130">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="efa6a-130">Click **Yes**.</span></span>
3. <span data-ttu-id="efa6a-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="efa6a-131">Close the page.</span></span>

