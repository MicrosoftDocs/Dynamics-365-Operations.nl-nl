--- 
title: " Callcenterorders maken"
description: Deze procedure doorloopt het opzoeken van een klant, het maken van een nieuwe order, het zoeken naar een product en het innen van betaling van de klant.
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d46e5382c4808ecb01012800caf85209b173901a
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="create-call-center-orders"></a><span data-ttu-id="3d949-103"> Callcenterorders maken</span><span class="sxs-lookup"><span data-stu-id="3d949-103">Create call center orders</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3d949-104">Deze procedure doorloopt het opzoeken van een klant, het maken van een nieuwe order, het zoeken naar een product en het innen van betaling van de klant.</span><span class="sxs-lookup"><span data-stu-id="3d949-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="3d949-105">Deze procedure gebruikt het demobedrijf USRT en is bedoeld voor de verkoopordermedewerker.</span><span class="sxs-lookup"><span data-stu-id="3d949-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="3d949-106">Vereisten: de gebruiker die de procedure uitvoert, is ingesteld als een callcentergebruiker en de halfjaarlijkse catalogus van Fabrikam wordt gepubliceerd met minimaal één broncode.</span><span class="sxs-lookup"><span data-stu-id="3d949-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="3d949-107">Ga naar Detailhandel en commerce > Klanten > Klantenservice.</span><span class="sxs-lookup"><span data-stu-id="3d949-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="3d949-108">Voer in het veld Zoektekst de zoekcriteria in om de klant te zoeken.</span><span class="sxs-lookup"><span data-stu-id="3d949-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="3d949-109">Voor deze voorbeeldprocedure typt u 'karen' en drukt u op Tab.</span><span class="sxs-lookup"><span data-stu-id="3d949-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="3d949-110">Klik op Zoeken.</span><span class="sxs-lookup"><span data-stu-id="3d949-110">Click Search.</span></span>
    * <span data-ttu-id="3d949-111">Aangezien er slechts één klant met de naam Karen voorkomt in de demogegevens, wordt zij automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3d949-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="3d949-112">Klik op Nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="3d949-112">Click New sales order.</span></span>
5. <span data-ttu-id="3d949-113">Vouw de sectie Koptekst van verkooporder uit of samen.</span><span class="sxs-lookup"><span data-stu-id="3d949-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="3d949-114">Selecteer de broncode voor de catalogus.</span><span class="sxs-lookup"><span data-stu-id="3d949-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="3d949-115">Als er geen actieve broncodes zijn, kunt u het veld Bron sluiten en deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="3d949-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="3d949-116">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3d949-116">Click Add line.</span></span>
8. <span data-ttu-id="3d949-117">Voer in het veld Artikelnummer de zoekterm voor het artikel in.</span><span class="sxs-lookup"><span data-stu-id="3d949-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="3d949-118">Voor deze voorbeeldprocedure voert u het gedeeltelijke artikelnummer 8111 in en drukt u op Tab. Het venster voor het zoeken van artikelen wordt dan weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3d949-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="3d949-119">Selecteer het product dat aan de verkooporder moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3d949-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="3d949-120">Voer de verkoophoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="3d949-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="3d949-121">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="3d949-121">Click Create.</span></span>
12. <span data-ttu-id="3d949-122">Klik op Voltooien om de betaling van de klant vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="3d949-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="3d949-123">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3d949-123">Click Add.</span></span>
    * <span data-ttu-id="3d949-124">De koppeling Toevoegen bevindt zich op het tabblad Betalingen. Vouw het tabblad Betalingen uit als het is samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="3d949-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="3d949-125">Selecteer de betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="3d949-125">Select the payment method.</span></span>
    * <span data-ttu-id="3d949-126">Selecteer voor deze procedure de contante betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="3d949-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="3d949-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3d949-127">Close the page.</span></span>
16. <span data-ttu-id="3d949-128">Geef het bedrag op.</span><span class="sxs-lookup"><span data-stu-id="3d949-128">Enter the amount.</span></span>
    * <span data-ttu-id="3d949-129">Voor deze procedure voert u een bedrag in gelijk aan de orderbalans die wordt weergegeven op de pagina Overzicht van verkooporder, links van het bedragveld.</span><span class="sxs-lookup"><span data-stu-id="3d949-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="3d949-130">U kunt de order dan voltooien als volledig betaald.</span><span class="sxs-lookup"><span data-stu-id="3d949-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="3d949-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3d949-131">Click OK.</span></span>
18. <span data-ttu-id="3d949-132">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="3d949-132">Click Submit.</span></span>


