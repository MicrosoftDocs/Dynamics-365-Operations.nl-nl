---
title: Voorwaarden voor leveranciersbetalingen definiëren
description: In dit onderwerp wordt uitgelegd u betalingstermijnen voor instelt voor leveranciersfacturen.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6a37272694609be14b566dae3c6cf561d4c6d2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227227"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="6d29a-103">Voorwaarden voor leveranciersbetalingen definiëren</span><span class="sxs-lookup"><span data-stu-id="6d29a-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d29a-104">In dit onderwerp wordt uitgelegd u betalingstermijnen voor instelt voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="6d29a-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="6d29a-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6d29a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6d29a-106">Ga naar **Navigatievenster > Modules > Leveranciers > Betalingsinstelling > Betalingstermijnen**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="6d29a-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-107">Select **New**.</span></span> <span data-ttu-id="6d29a-108">De pagina Betalingstermijnen wordt gebruikt om te bepalen hoe de vervaldatum wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="6d29a-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="6d29a-109">Het wordt niet gebruikt om te bepalen hoe de datum contantkorting wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="6d29a-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="6d29a-110">Typ een waarde in het veld **Betalingstermijn**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="6d29a-111">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="6d29a-112">Voer in het veld **Dagen** een getal in.</span><span class="sxs-lookup"><span data-stu-id="6d29a-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="6d29a-113">Het hier ingevoerde getal wordt gebruikt om op te tellen bij de vervaldatum of bij het einde van de periode die wordt geïdentificeerd in Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="6d29a-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="6d29a-114">Als u bijvoorbeeld **Netto** selecteert, wordt de waarde opgeteld bij de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="6d29a-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="6d29a-115">Als u **Huidige maand** selecteert, wordt de waarde opgeteld bij de laatste dag van de huidige maand om de vervaldatum te berekenen.</span><span class="sxs-lookup"><span data-stu-id="6d29a-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="6d29a-116">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-116">Select **Save**.</span></span>
7. <span data-ttu-id="6d29a-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6d29a-117">Close the page.</span></span>
8. <span data-ttu-id="6d29a-118">Ga naar **Leveranciers > Betalingsinstelling > Contantkortingen**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="6d29a-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-119">Select **New**.</span></span>
10. <span data-ttu-id="6d29a-120">Typ een id iin het veld **Contantkorting**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="6d29a-121">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="6d29a-122">Als de leverancier een gelaagde korting aanbiedt, selecteert u de volgende contantkorting nadat de huidige is vervallen.</span><span class="sxs-lookup"><span data-stu-id="6d29a-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="6d29a-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6d29a-123">Close the page.</span></span>
14. <span data-ttu-id="6d29a-124">Voer in het veld **Dagen** een getal in.</span><span class="sxs-lookup"><span data-stu-id="6d29a-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="6d29a-125">De hoeveelheid die in het veld **Dagen** is ingevoerd, wordt gebruikt voor het berekenen van de datum voor de contantkorting, op basis van de optie die is geselecteerd in het veld **Netto/Huidige maand**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="6d29a-126">Als **Netto** is geselecteerd, wordt de hoeveelheid opgeteld bij de factuurdatum om de datum voor de contantkorting te bepalen.</span><span class="sxs-lookup"><span data-stu-id="6d29a-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="6d29a-127">Als **Huidige maand** is geselecteerd, wordt de hoeveelheid opgeteld bij het einde van de valutamaand om de datum voor de contantkorting te bepalen.</span><span class="sxs-lookup"><span data-stu-id="6d29a-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="6d29a-128">Voer het percentage van de contantkorting in het veld **Korting** in.</span><span class="sxs-lookup"><span data-stu-id="6d29a-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="6d29a-129">Voer de hoofdrekening in waarnaar de contantkorting voor klantfacturen wordt geboekt, en voer vervolgens de hoofdrekening in waarnaar de contantkorting voor leveranciersfacturen wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="6d29a-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="6d29a-130">Als **Korting tegenrekeningen** is ingesteld op **Hoofdrekening voor leverancierskortingen gebruiken**, wordt de hoofdrekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6d29a-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="6d29a-131">Als de optie is ingesteld op **Rekeningen op de factuurregels**, wordt de contantkorting geboekt naar de activa-/onkostenrekeningen op de regels van de factuur.</span><span class="sxs-lookup"><span data-stu-id="6d29a-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="6d29a-132">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6d29a-132">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]