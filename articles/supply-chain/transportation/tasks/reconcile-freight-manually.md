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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8679a729dc17e3ee85468b459da3956a92160ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974055"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="8ca98-103">Handmatig vracht afstemmen</span><span class="sxs-lookup"><span data-stu-id="8ca98-103">Reconcile freight manually</span></span>

<span data-ttu-id="8ca98-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="8ca98-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="8ca98-105">Deze procedure laat zien hoe u vracht handmatig afstemt.</span><span class="sxs-lookup"><span data-stu-id="8ca98-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="8ca98-106">Dit wordt gewoonlijk gedaan door een transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="8ca98-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="8ca98-107">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="8ca98-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="8ca98-108">Selecteer belasting om af te stemmen</span><span class="sxs-lookup"><span data-stu-id="8ca98-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="8ca98-109">Ga naar Transportbeheer > Planning > Workbench van ladingplanning.</span><span class="sxs-lookup"><span data-stu-id="8ca98-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="8ca98-110">Schakel het selectievakje Verzonden en ontvangen verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="8ca98-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="8ca98-111">Selecteer in de lijst de lading met id 00006.</span><span class="sxs-lookup"><span data-stu-id="8ca98-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="8ca98-112">Een leverancierfactuur maken</span><span class="sxs-lookup"><span data-stu-id="8ca98-112">Create a carrier invoice</span></span>
<span data-ttu-id="8ca98-113">Als u handmatig vracht afstemt en vervoerdersfacturen niet automatisch ontvangt, kunt u een factuur maken op basis van de vrachtfactuur.</span><span class="sxs-lookup"><span data-stu-id="8ca98-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="8ca98-114">Klik op Verwante informatie.</span><span class="sxs-lookup"><span data-stu-id="8ca98-114">Click Related information.</span></span>
2. <span data-ttu-id="8ca98-115">Klik op Details vrachtfactuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="8ca98-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="8ca98-116">Klik op Vrachtfactuur genereren.</span><span class="sxs-lookup"><span data-stu-id="8ca98-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="8ca98-117">Typ een waarde in het veld Factuur.</span><span class="sxs-lookup"><span data-stu-id="8ca98-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="8ca98-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8ca98-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="8ca98-119">De factuur afstemmen</span><span class="sxs-lookup"><span data-stu-id="8ca98-119">Reconcile the invoice</span></span>
<span data-ttu-id="8ca98-120">Wanneer u een vervoerderfactuur en een vrachtfactuur afstemt, wordt dat regel voor regel gedaan.</span><span class="sxs-lookup"><span data-stu-id="8ca98-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="8ca98-121">Klik op Vrachtfacturen en facturen vereffenen.</span><span class="sxs-lookup"><span data-stu-id="8ca98-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="8ca98-122">Vouw de sectie Factuurdetails uit.</span><span class="sxs-lookup"><span data-stu-id="8ca98-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="8ca98-123">Vouw de sectie Niet-afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="8ca98-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="8ca98-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8ca98-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8ca98-125">Klik op Afstemmen.</span><span class="sxs-lookup"><span data-stu-id="8ca98-125">Click Match.</span></span>
6. <span data-ttu-id="8ca98-126">Vouw de sectie Afgestemde details vrachtfactuur uit.</span><span class="sxs-lookup"><span data-stu-id="8ca98-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="8ca98-127">De factuur verzenden voor goedkeuring</span><span class="sxs-lookup"><span data-stu-id="8ca98-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="8ca98-128">Klik op Aanbieden ter goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="8ca98-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="8ca98-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="8ca98-129">Close the page.</span></span>
3. <span data-ttu-id="8ca98-130">Schakel het selectievakje Goedgekeurd verbergen uit.</span><span class="sxs-lookup"><span data-stu-id="8ca98-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="8ca98-131">Klik op Leveranciersfactuurjournalen.</span><span class="sxs-lookup"><span data-stu-id="8ca98-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="8ca98-132">Klik om de koppeling in het veld Verwijzing naar journaalnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="8ca98-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="8ca98-133">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="8ca98-133">Click Lines.</span></span>

