---
title: Handmatig vracht afstemmen
description: Deze procedure laat zien hoe u vracht handmatig afstemt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb9c850aa045b72137b8a1d3c8cdae51cf2fd7b6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843236"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="f2b82-103">Handmatig vracht afstemmen</span><span class="sxs-lookup"><span data-stu-id="f2b82-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2b82-104">Deze procedure laat zien hoe u vracht handmatig afstemt.</span><span class="sxs-lookup"><span data-stu-id="f2b82-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="f2b82-105">Dit wordt gewoonlijk gedaan door een transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="f2b82-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="f2b82-106">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="f2b82-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="f2b82-107">Selecteer belasting om af te stemmen</span><span class="sxs-lookup"><span data-stu-id="f2b82-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="f2b82-108">Ga naar Transportbeheer > Planning > Workbench van ladingplanning.</span><span class="sxs-lookup"><span data-stu-id="f2b82-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="f2b82-109">Schakel het selectievakje Verzonden en ontvangen verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="f2b82-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="f2b82-110">Selecteer in de lijst de lading met id 00006.</span><span class="sxs-lookup"><span data-stu-id="f2b82-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="f2b82-111">Een leverancierfactuur maken</span><span class="sxs-lookup"><span data-stu-id="f2b82-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="f2b82-112">Als u handmatig vracht afstemt en vervoerderfacturen niet automatisch ontvangt, kunt u een factuur maken op basis van de vrachtfactuur.</span><span class="sxs-lookup"><span data-stu-id="f2b82-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="f2b82-113">Klik op Verwante informatie.</span><span class="sxs-lookup"><span data-stu-id="f2b82-113">Click Related information.</span></span>
2. <span data-ttu-id="f2b82-114">Klik op Details vrachtfactuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="f2b82-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="f2b82-115">Klik op Vrachtfactuur genereren.</span><span class="sxs-lookup"><span data-stu-id="f2b82-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="f2b82-116">Typ een waarde in het veld Factuur.</span><span class="sxs-lookup"><span data-stu-id="f2b82-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="f2b82-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f2b82-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="f2b82-118">De factuur afstemmen</span><span class="sxs-lookup"><span data-stu-id="f2b82-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="f2b82-119">Wanneer u een vervoerderfactuur en een vrachtfactuur afstemt, wordt dat regel voor regel gedaan.</span><span class="sxs-lookup"><span data-stu-id="f2b82-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="f2b82-120">Klik op Vrachtfacturen en facturen vereffenen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="f2b82-121">Vouw de sectie Factuurdetails uit.</span><span class="sxs-lookup"><span data-stu-id="f2b82-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="f2b82-122">Vouw de sectie Niet-afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="f2b82-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="f2b82-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f2b82-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="f2b82-124">Klik op Afstemmen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-124">Click Match.</span></span>
6. <span data-ttu-id="f2b82-125">Vouw de sectie Afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="f2b82-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="f2b82-126">De factuur verzenden voor goedkeuring</span><span class="sxs-lookup"><span data-stu-id="f2b82-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="f2b82-127">Klik op Aanbieden ter goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="f2b82-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="f2b82-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f2b82-128">Close the page.</span></span>
3. <span data-ttu-id="f2b82-129">Schakel het selectievakje Goedgekeurd verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="f2b82-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="f2b82-130">Klik op Leveranciersfactuurjournalen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="f2b82-131">Klik om de koppeling in het veld Verwijzing naar journaalnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="f2b82-132">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="f2b82-132">Click Lines.</span></span>

