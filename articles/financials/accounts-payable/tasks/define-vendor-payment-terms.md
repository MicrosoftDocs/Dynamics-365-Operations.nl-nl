--- 
title: "Voorwaarden voor leveranciersbetalingen definiëren"
description: Stel de betalingsvoorwaarden in voor leveranciersfacturen.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a00ca73b1bc301960132a86846749d12c39ed3f7
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="db5d2-103">Voorwaarden voor leveranciersbetalingen definiëren</span><span class="sxs-lookup"><span data-stu-id="db5d2-103">Define vendor payment terms</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db5d2-104">Stel de betalingsvoorwaarden in voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="db5d2-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="db5d2-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="db5d2-106">Ga naar Leveranciers > Betalingsinstelling > Betalingstermijnen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="db5d2-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="db5d2-107">Click New.</span></span>
    * <span data-ttu-id="db5d2-108">De pagina Betalingstermijnen wordt gebruikt om te bepalen hoe de vervaldatum wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="db5d2-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="db5d2-109">Het wordt niet gebruikt om te bepalen hoe de datum contantkorting wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="db5d2-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="db5d2-110">Typ een waarde in het veld Betalingstermijnen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="db5d2-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="db5d2-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="db5d2-112">Voer een getal in het veld Dagen in.</span><span class="sxs-lookup"><span data-stu-id="db5d2-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="db5d2-113">Het hier ingevoerde getal wordt gebruikt om op te tellen bij de vervaldatum of bij het einde van de periode die wordt geïdentificeerd in Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="db5d2-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="db5d2-114">Als u bijvoorbeeld Netto selecteert, wordt het nummer opgeteld bij de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="db5d2-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="db5d2-115">Als u Huidige maand selecteert, wordt het getal opgeteld bij de laatste dag van de huidige maand om de vervaldatum te berekenen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="db5d2-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="db5d2-116">Click Save.</span></span>
7. <span data-ttu-id="db5d2-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="db5d2-117">Close the page.</span></span>
8. <span data-ttu-id="db5d2-118">Ga naar Leveranciers > Betalingsinstelling > Contantkortingen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="db5d2-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="db5d2-119">Click New.</span></span>
10. <span data-ttu-id="db5d2-120">Geef een id op in het veld Contantkorting.</span><span class="sxs-lookup"><span data-stu-id="db5d2-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="db5d2-121">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="db5d2-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="db5d2-122">Als de leverancier een gelaagde korting aanbiedt, selecteert u de volgende contantkorting nadat de huidige is vervallen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="db5d2-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="db5d2-123">Close the page.</span></span>
14. <span data-ttu-id="db5d2-124">Voer een getal in het veld Dagen in.</span><span class="sxs-lookup"><span data-stu-id="db5d2-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="db5d2-125">De hoeveelheid die in het veld Dagen is ingevoerd wordt gebruikt voor het berekenen van de datum voor de contantkorting, op basis van de optie die is geselecteerd in het veld Netto/Huidig.</span><span class="sxs-lookup"><span data-stu-id="db5d2-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="db5d2-126">Als Netto is geselecteerd, wordt de hoeveelheid opgeteld bij de factuurdatum om de datum voor de contantkorting te bepalen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="db5d2-127">Als Huidge maand is geselecteerd, wordt de hoeveelheid opgeteld bij het einde van de valutamaand om de datum voor de contantkorting te bepalen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="db5d2-128">Voer het percentage van de contantkorting in het veld Korting in.</span><span class="sxs-lookup"><span data-stu-id="db5d2-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="db5d2-129">Voer de hoofdrekening in waaraan de contantkorting wordt geboekt voor klantfacturen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="db5d2-130">Voer de hoofdrekening in waaraan de contantkorting wordt geboekt voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="db5d2-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="db5d2-131">Als Korting tegenrekeningen is ingesteld op Hoofdrekening voor leverancierskortingen gebruiken, wordt de hoofdrekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="db5d2-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="db5d2-132">Als de optie is ingesteld op Rekeningen op de factuurregels, wordt de contantkorting geboekt naar de activa-/onkostenrekeningen op de regels van de factuur.</span><span class="sxs-lookup"><span data-stu-id="db5d2-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="db5d2-133">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="db5d2-133">Click Save.</span></span>


