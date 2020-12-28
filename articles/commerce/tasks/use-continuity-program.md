---
title: Continuïteitsprogramma's gebruiken
description: Deze procedure laat zien hoe u een continuïteitsprogramma verkoopt en de gerelateerde verkooporders verwerkt.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411406"
---
# <a name="using-continuity-program"></a><span data-ttu-id="82bfd-103">Continuïteitsprogramma's gebruiken</span><span class="sxs-lookup"><span data-stu-id="82bfd-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82bfd-104">Deze procedure laat zien hoe u een continuïteitsprogramma verkoopt en de gerelateerde verkooporders verwerkt.</span><span class="sxs-lookup"><span data-stu-id="82bfd-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="82bfd-105">Om deze procedure te kunnen uitvoeren, moet de gebruiker zijn ingesteld als een callcenter-gebruiker.</span><span class="sxs-lookup"><span data-stu-id="82bfd-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="82bfd-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="82bfd-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="82bfd-107">Ga naar Detailhandel en commerce > Klanten > Klantenservice.</span><span class="sxs-lookup"><span data-stu-id="82bfd-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="82bfd-108">Type in het veld Zoektekst 'Karen' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="82bfd-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="82bfd-109">Het dialoogvenster Geavanceerd zoeken moet worden geopend in een pop-upvenster.</span><span class="sxs-lookup"><span data-stu-id="82bfd-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="82bfd-110">Als dit niet gebeurt, klikt u op Zoeken rechts naast dit veld.</span><span class="sxs-lookup"><span data-stu-id="82bfd-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="82bfd-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="82bfd-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="82bfd-112">Er zou slechts één rij moeten zijn, die Karen Berg bevat.</span><span class="sxs-lookup"><span data-stu-id="82bfd-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="82bfd-113">Selecteer de rij door te klikken op de kolom met het selectievakje helemaal links in het raster.</span><span class="sxs-lookup"><span data-stu-id="82bfd-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="82bfd-114">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="82bfd-114">Click Select.</span></span>
5. <span data-ttu-id="82bfd-115">Klik op Nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="82bfd-115">Click New sales order.</span></span>
    * <span data-ttu-id="82bfd-116">Het is handig om nu het verkoopordernummer te noteren.</span><span class="sxs-lookup"><span data-stu-id="82bfd-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="82bfd-117">U hebt dit later in deze procedure nog nodig.</span><span class="sxs-lookup"><span data-stu-id="82bfd-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="82bfd-118">Type in het veld Artikelnummer '88000' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="82bfd-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="82bfd-119">Dit is een continuïteitsartikel in de demogegevens van USRT.</span><span class="sxs-lookup"><span data-stu-id="82bfd-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="82bfd-120">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="82bfd-120">Click Complete.</span></span>
8. <span data-ttu-id="82bfd-121">Selecteer in het veld Betalingsmethode 'Visa'.</span><span class="sxs-lookup"><span data-stu-id="82bfd-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="82bfd-122">Klik op Creditcard toevoegen.</span><span class="sxs-lookup"><span data-stu-id="82bfd-122">Click Add credit card.</span></span>
    * <span data-ttu-id="82bfd-123">Voer de vereiste creditcardinformatie in op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="82bfd-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="82bfd-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="82bfd-124">Click OK.</span></span>
11. <span data-ttu-id="82bfd-125">Vouw de sectie Betaling uit.</span><span class="sxs-lookup"><span data-stu-id="82bfd-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="82bfd-126">Om een callcenter-bestelling in te dienen, moeten voor de order ook betalingen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="82bfd-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="82bfd-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="82bfd-127">Click OK.</span></span>
13. <span data-ttu-id="82bfd-128">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="82bfd-128">Click Submit.</span></span>
    * <span data-ttu-id="82bfd-129">U bent klaar met het maken van een nieuwe continuïteitsorder.</span><span class="sxs-lookup"><span data-stu-id="82bfd-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="82bfd-130">Vervolgens voert u twee batchprocessen uit waarmee de continuïteitsorders worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="82bfd-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="82bfd-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="82bfd-131">Close the page.</span></span>
15. <span data-ttu-id="82bfd-132">Ga naar Detailhandel en commerce > Continuïteit > Continuïteitsbetalingen verwerken.</span><span class="sxs-lookup"><span data-stu-id="82bfd-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="82bfd-133">Type in het veld Continuïteitsartikel '88000' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="82bfd-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="82bfd-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="82bfd-134">Click OK.</span></span>
18. <span data-ttu-id="82bfd-135">Ga naar Detailhandel en commerce > Continuïteit > Onderliggende continuïteitsorders maken.</span><span class="sxs-lookup"><span data-stu-id="82bfd-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="82bfd-136">Dit proces maakt nieuwe verkooporders op basis van de instellingen van uw continuïteitsprogramma's.</span><span class="sxs-lookup"><span data-stu-id="82bfd-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="82bfd-137">Type in het veld Continuïteitsartikel '88000' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="82bfd-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="82bfd-138">Artikel '88000' is een continuïteitsartikel in de demogegevens van USRT.</span><span class="sxs-lookup"><span data-stu-id="82bfd-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="82bfd-139">Typ of selecteer een waarde in het veld Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="82bfd-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="82bfd-140">Voer het verkoopordernummer in dat u eerder in de procedure hebt genoteerd.</span><span class="sxs-lookup"><span data-stu-id="82bfd-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="82bfd-141">Dit zorgt ervoor dat de verwerkingstijd voor deze procedure minimaal blijft.</span><span class="sxs-lookup"><span data-stu-id="82bfd-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="82bfd-142">Het veld Verkooporder is optioneel. U kunt alle orders voor elk programma verwerken.</span><span class="sxs-lookup"><span data-stu-id="82bfd-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="82bfd-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="82bfd-143">Click OK.</span></span>

