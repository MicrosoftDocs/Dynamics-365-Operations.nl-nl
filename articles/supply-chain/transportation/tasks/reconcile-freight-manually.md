--- 
title: Handmatig vracht afstemmen
description: Deze procedure laat zien hoe u vracht handmatig afstemt.
author: ShylaThompson
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: eb6f53de5013e8d5ee50c606bac15599bc960da4
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="4e413-103">Handmatig vracht afstemmen</span><span class="sxs-lookup"><span data-stu-id="4e413-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e413-104">Deze procedure laat zien hoe u vracht handmatig afstemt.</span><span class="sxs-lookup"><span data-stu-id="4e413-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="4e413-105">Dit wordt gewoonlijk gedaan door een transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="4e413-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="4e413-106">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="4e413-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="4e413-107">Selecteer belasting om af te stemmen</span><span class="sxs-lookup"><span data-stu-id="4e413-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="4e413-108">Ga naar Transportbeheer > Planning > Workbench van ladingplanning.</span><span class="sxs-lookup"><span data-stu-id="4e413-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="4e413-109">Schakel het selectievakje Verzonden en ontvangen verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="4e413-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="4e413-110">Selecteer in de lijst de lading met id 00006.</span><span class="sxs-lookup"><span data-stu-id="4e413-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="4e413-111">Een leverancierfactuur maken</span><span class="sxs-lookup"><span data-stu-id="4e413-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="4e413-112">Als u handmatig vracht afstemt en vervoerderfacturen niet automatisch ontvangt, kunt u een factuur maken op basis van de vrachtfactuur.</span><span class="sxs-lookup"><span data-stu-id="4e413-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="4e413-113">Klik op Verwante informatie.</span><span class="sxs-lookup"><span data-stu-id="4e413-113">Click Related information.</span></span>
2. <span data-ttu-id="4e413-114">Klik op Details vrachtfactuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="4e413-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="4e413-115">Klik op Vrachtfactuur genereren.</span><span class="sxs-lookup"><span data-stu-id="4e413-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="4e413-116">Typ een waarde in het veld Factuur.</span><span class="sxs-lookup"><span data-stu-id="4e413-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="4e413-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4e413-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="4e413-118">De factuur afstemmen</span><span class="sxs-lookup"><span data-stu-id="4e413-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="4e413-119">Wanneer u een vervoerderfactuur en een vrachtfactuur afstemt, wordt dat regel voor regel gedaan.</span><span class="sxs-lookup"><span data-stu-id="4e413-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="4e413-120">Klik op Vrachtfacturen en facturen vereffenen.</span><span class="sxs-lookup"><span data-stu-id="4e413-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="4e413-121">Vouw de sectie Factuurdetails uit.</span><span class="sxs-lookup"><span data-stu-id="4e413-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="4e413-122">Vouw de sectie Niet-afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="4e413-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="4e413-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4e413-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="4e413-124">Klik op Afstemmen.</span><span class="sxs-lookup"><span data-stu-id="4e413-124">Click Match.</span></span>
6. <span data-ttu-id="4e413-125">Vouw de sectie Afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="4e413-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="4e413-126">De factuur verzenden voor goedkeuring</span><span class="sxs-lookup"><span data-stu-id="4e413-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="4e413-127">Klik op Aanbieden ter goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="4e413-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="4e413-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4e413-128">Close the page.</span></span>
3. <span data-ttu-id="4e413-129">Schakel het selectievakje Goedgekeurd verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="4e413-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="4e413-130">Klik op Leveranciersfactuurjournalen.</span><span class="sxs-lookup"><span data-stu-id="4e413-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="4e413-131">Klik om de koppeling in het veld Verwijzing naar journaalnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="4e413-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="4e413-132">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="4e413-132">Click Lines.</span></span>


