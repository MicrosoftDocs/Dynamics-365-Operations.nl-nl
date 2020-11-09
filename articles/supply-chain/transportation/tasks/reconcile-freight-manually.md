---
title: Handmatig vracht afstemmen
description: Deze procedure laat zien hoe u vracht handmatig afstemt.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc4fc51955544df4d0156a4c83bcc5b5a0e13df3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016971"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="2a977-103">Handmatig vracht afstemmen</span><span class="sxs-lookup"><span data-stu-id="2a977-103">Reconcile freight manually</span></span>

<span data-ttu-id="2a977-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="2a977-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="2a977-105">Deze procedure laat zien hoe u vracht handmatig afstemt.</span><span class="sxs-lookup"><span data-stu-id="2a977-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="2a977-106">Dit wordt gewoonlijk gedaan door een transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="2a977-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="2a977-107">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="2a977-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="2a977-108">Selecteer belasting om af te stemmen</span><span class="sxs-lookup"><span data-stu-id="2a977-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="2a977-109">Ga naar Transportbeheer > Planning > Workbench van ladingplanning.</span><span class="sxs-lookup"><span data-stu-id="2a977-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="2a977-110">Schakel het selectievakje Verzonden en ontvangen verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="2a977-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="2a977-111">Selecteer in de lijst de lading met id 00006.</span><span class="sxs-lookup"><span data-stu-id="2a977-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="2a977-112">Een leverancierfactuur maken</span><span class="sxs-lookup"><span data-stu-id="2a977-112">Create a carrier invoice</span></span>
<span data-ttu-id="2a977-113">Als u handmatig vracht afstemt en vervoerdersfacturen niet automatisch ontvangt, kunt u een factuur maken op basis van de vrachtfactuur.</span><span class="sxs-lookup"><span data-stu-id="2a977-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="2a977-114">Klik op Verwante informatie.</span><span class="sxs-lookup"><span data-stu-id="2a977-114">Click Related information.</span></span>
2. <span data-ttu-id="2a977-115">Klik op Details vrachtfactuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="2a977-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="2a977-116">Klik op Vrachtfactuur genereren.</span><span class="sxs-lookup"><span data-stu-id="2a977-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="2a977-117">Typ een waarde in het veld Factuur.</span><span class="sxs-lookup"><span data-stu-id="2a977-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="2a977-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2a977-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="2a977-119">De factuur afstemmen</span><span class="sxs-lookup"><span data-stu-id="2a977-119">Reconcile the invoice</span></span>
<span data-ttu-id="2a977-120">Wanneer u een vervoerderfactuur en een vrachtfactuur afstemt, wordt dat regel voor regel gedaan.</span><span class="sxs-lookup"><span data-stu-id="2a977-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="2a977-121">Klik op Vrachtfacturen en facturen vereffenen.</span><span class="sxs-lookup"><span data-stu-id="2a977-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="2a977-122">Vouw de sectie Factuurdetails uit.</span><span class="sxs-lookup"><span data-stu-id="2a977-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="2a977-123">Vouw de sectie Niet-afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="2a977-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="2a977-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2a977-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="2a977-125">Klik op Afstemmen.</span><span class="sxs-lookup"><span data-stu-id="2a977-125">Click Match.</span></span>
6. <span data-ttu-id="2a977-126">Vouw de sectie Afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="2a977-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="2a977-127">De factuur verzenden voor goedkeuring</span><span class="sxs-lookup"><span data-stu-id="2a977-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="2a977-128">Klik op Aanbieden ter goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="2a977-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="2a977-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2a977-129">Close the page.</span></span>
3. <span data-ttu-id="2a977-130">Schakel het selectievakje Goedgekeurd verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="2a977-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="2a977-131">Klik op Leveranciersfactuurjournalen.</span><span class="sxs-lookup"><span data-stu-id="2a977-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="2a977-132">Klik om de koppeling in het veld Verwijzing naar journaalnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="2a977-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="2a977-133">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="2a977-133">Click Lines.</span></span>

