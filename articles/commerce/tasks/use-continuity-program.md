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
ms.openlocfilehash: cd0bfcd99a23e4c639a6317adefb41a947a487a5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022103"
---
# <a name="using-continuity-program"></a><span data-ttu-id="9725b-103">Continuïteitsprogramma's gebruiken</span><span class="sxs-lookup"><span data-stu-id="9725b-103">Using continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9725b-104">Deze procedure laat zien hoe u een continuïteitsprogramma verkoopt en de gerelateerde verkooporders verwerkt.</span><span class="sxs-lookup"><span data-stu-id="9725b-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="9725b-105">Om deze procedure te kunnen uitvoeren, moet de gebruiker zijn ingesteld als een callcenter-gebruiker.</span><span class="sxs-lookup"><span data-stu-id="9725b-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="9725b-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="9725b-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="9725b-107">Ga naar Detailhandel en commerce > Klanten > Klantenservice.</span><span class="sxs-lookup"><span data-stu-id="9725b-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="9725b-108">Type in het veld Zoektekst 'Karen' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="9725b-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="9725b-109">Het dialoogvenster Geavanceerd zoeken moet worden geopend in een pop-upvenster.</span><span class="sxs-lookup"><span data-stu-id="9725b-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="9725b-110">Als dit niet gebeurt, klikt u op Zoeken rechts naast dit veld.</span><span class="sxs-lookup"><span data-stu-id="9725b-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="9725b-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9725b-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9725b-112">Er zou slechts één rij moeten zijn, die Karen Berg bevat.</span><span class="sxs-lookup"><span data-stu-id="9725b-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="9725b-113">Selecteer de rij door te klikken op de kolom met het selectievakje helemaal links in het raster.</span><span class="sxs-lookup"><span data-stu-id="9725b-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="9725b-114">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="9725b-114">Click Select.</span></span>
5. <span data-ttu-id="9725b-115">Klik op Nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="9725b-115">Click New sales order.</span></span>
    * <span data-ttu-id="9725b-116">Het is handig om nu het verkoopordernummer te noteren.</span><span class="sxs-lookup"><span data-stu-id="9725b-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="9725b-117">U hebt dit later in deze procedure nog nodig.</span><span class="sxs-lookup"><span data-stu-id="9725b-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="9725b-118">Type in het veld Artikelnummer '88000' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="9725b-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="9725b-119">Dit is een continuïteitsartikel in de demogegevens van USRT.</span><span class="sxs-lookup"><span data-stu-id="9725b-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="9725b-120">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="9725b-120">Click Complete.</span></span>
8. <span data-ttu-id="9725b-121">Selecteer in het veld Betalingsmethode 'Visa'.</span><span class="sxs-lookup"><span data-stu-id="9725b-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="9725b-122">Klik op Creditcard toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9725b-122">Click Add credit card.</span></span>
    * <span data-ttu-id="9725b-123">Voer de vereiste creditcardinformatie in op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="9725b-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="9725b-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9725b-124">Click OK.</span></span>
11. <span data-ttu-id="9725b-125">Vouw de sectie Betaling uit.</span><span class="sxs-lookup"><span data-stu-id="9725b-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="9725b-126">Om een callcenter-bestelling in te dienen, moeten voor de order ook betalingen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="9725b-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="9725b-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9725b-127">Click OK.</span></span>
13. <span data-ttu-id="9725b-128">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="9725b-128">Click Submit.</span></span>
    * <span data-ttu-id="9725b-129">U bent klaar met het maken van een nieuwe continuïteitsorder.</span><span class="sxs-lookup"><span data-stu-id="9725b-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="9725b-130">Vervolgens voert u twee batchprocessen uit waarmee de continuïteitsorders worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="9725b-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="9725b-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9725b-131">Close the page.</span></span>
15. <span data-ttu-id="9725b-132">Ga naar Detailhandel en commerce > Continuïteit > Continuïteitsbetalingen verwerken.</span><span class="sxs-lookup"><span data-stu-id="9725b-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="9725b-133">Type in het veld Continuïteitsartikel '88000' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="9725b-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="9725b-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9725b-134">Click OK.</span></span>
18. <span data-ttu-id="9725b-135">Ga naar Detailhandel en commerce > Continuïteit > Onderliggende continuïteitsorders maken.</span><span class="sxs-lookup"><span data-stu-id="9725b-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="9725b-136">Dit proces maakt nieuwe verkooporders op basis van de instellingen van uw continuïteitsprogramma's.</span><span class="sxs-lookup"><span data-stu-id="9725b-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="9725b-137">Type in het veld Continuïteitsartikel '88000' en druk de Tab-toets in.</span><span class="sxs-lookup"><span data-stu-id="9725b-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="9725b-138">Artikel '88000' is een continuïteitsartikel in de demogegevens van USRT.</span><span class="sxs-lookup"><span data-stu-id="9725b-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="9725b-139">Typ of selecteer een waarde in het veld Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="9725b-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="9725b-140">Voer het verkoopordernummer in dat u eerder in de procedure hebt genoteerd.</span><span class="sxs-lookup"><span data-stu-id="9725b-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="9725b-141">Dit zorgt ervoor dat de verwerkingstijd voor deze procedure minimaal blijft.</span><span class="sxs-lookup"><span data-stu-id="9725b-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="9725b-142">Het veld Verkooporder is optioneel. U kunt alle orders voor elk programma verwerken.</span><span class="sxs-lookup"><span data-stu-id="9725b-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="9725b-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9725b-143">Click OK.</span></span>
