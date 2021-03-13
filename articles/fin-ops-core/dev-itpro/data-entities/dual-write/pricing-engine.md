---
title: Op verzoek synchroniseren met de Supply Chain Management-prijsengine
description: In dit onderwerp wordt beschreven hoe u de prijsengine in Microsoft Dynamics 365 Supply Chain Management gebruikt vanuit Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 45a9de18a3ff9c50eba8b316171b492605d683d4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130648"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="9858a-103">Op verzoek synchroniseren met de Supply Chain Management-prijsengine</span><span class="sxs-lookup"><span data-stu-id="9858a-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="9858a-104">Microsoft Dynamics 365 Supply Chain Management bevat een prijsengine waarmee handelsovereenkomsten, prijslijsten, klantloyaliteitsprogramma's, promoties en kortingen worden afgehandeld.</span><span class="sxs-lookup"><span data-stu-id="9858a-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="9858a-105">De prijsengine gebruikt complexe regels om de beste prijs voor een bepaalde offerte of order te bepalen.</span><span class="sxs-lookup"><span data-stu-id="9858a-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="9858a-106">Wanneer u Twee keer wegschrijven gebruikt, gebruikt u statische prijzen of de prijsengine van Dynamics 365 Supply Chain Management op de offerte- en orderpagina's in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9858a-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="9858a-107">De prijsengine uit Supply Chain Management in Sales gebruiken</span><span class="sxs-lookup"><span data-stu-id="9858a-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="9858a-108">Ga in Sales naar **Verkoop \> Orders**.</span><span class="sxs-lookup"><span data-stu-id="9858a-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="9858a-109">Selecteer **Nieuw** om een nieuwe order te maken of selecteer een bestaande order in de lijst **Mijn orders**.</span><span class="sxs-lookup"><span data-stu-id="9858a-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="9858a-110">Voeg een nieuwe orderregel toe.</span><span class="sxs-lookup"><span data-stu-id="9858a-110">Add a new order line.</span></span>
4. <span data-ttu-id="9858a-111">Als u een nieuwe order maakt, selecteert u **Prijsorder** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9858a-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="9858a-112">Als u een bestaande order bijwerkt, selecteert u **Opnieuw berekenen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9858a-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="9858a-113">De volgende kolommen worden automatisch ingevuld:</span><span class="sxs-lookup"><span data-stu-id="9858a-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="9858a-114">Detailbedrag</span><span class="sxs-lookup"><span data-stu-id="9858a-114">Detail Amount</span></span>
    + <span data-ttu-id="9858a-115">Kortingspercentage</span><span class="sxs-lookup"><span data-stu-id="9858a-115">Discount %</span></span>
    + <span data-ttu-id="9858a-116">Korting</span><span class="sxs-lookup"><span data-stu-id="9858a-116">Discount</span></span>
    + <span data-ttu-id="9858a-117">Bedrag vóór vracht</span><span class="sxs-lookup"><span data-stu-id="9858a-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="9858a-118">Vrachtkosten</span><span class="sxs-lookup"><span data-stu-id="9858a-118">Freight Amount</span></span>
    + <span data-ttu-id="9858a-119">Totaal belasting</span><span class="sxs-lookup"><span data-stu-id="9858a-119">Total Tax</span></span>
    + <span data-ttu-id="9858a-120">Totaalbedrag</span><span class="sxs-lookup"><span data-stu-id="9858a-120">Total Amount</span></span>
    
5. <span data-ttu-id="9858a-121">Om ervoor te zorgen dat het systeem handel- en verkoopovereenkomsten meeneemt bij het berekenen van de prijs:</span><span class="sxs-lookup"><span data-stu-id="9858a-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="9858a-122">Ga naar uw Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="9858a-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="9858a-123">Navigeer naar **Klanten \> Instellen \> Parameters van Klanten**.</span><span class="sxs-lookup"><span data-stu-id="9858a-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="9858a-124">Selecteer het tabblad **Prijzen** op de navigatiebalk aan de zijkant.</span><span class="sxs-lookup"><span data-stu-id="9858a-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="9858a-125">Schakel de optie **Handmatige invoer** uit op het sneltabblad **Evaluatie van handelsovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="9858a-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="9858a-126">Hoe het werkt</span><span class="sxs-lookup"><span data-stu-id="9858a-126">How it works</span></span>

<span data-ttu-id="9858a-127">Wanneer u **Prijsorder** selecteert in Sales, wordt de functie **Totalen** op het tabblad **Verkooporder \> Weergeven** in Supply Chain Management aangeroepen voor de bijbehorende verkooporder.</span><span class="sxs-lookup"><span data-stu-id="9858a-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="9858a-128">De waarden in het ordertotaal in Sales worden gebruikt om de overeenkomende kolommen in Supply Chain Management in te vullen.</span><span class="sxs-lookup"><span data-stu-id="9858a-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="9858a-129">Wanneer het verkoopordertotaal wordt berekend in Supply Chain Management, worden de bestaande handelsovereenkomsten en verkoopovereenkomsten voor de klant en de producten in de verkooporder geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="9858a-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="9858a-130">Deze informatie wordt gebruikt om de totalen te berekenen.</span><span class="sxs-lookup"><span data-stu-id="9858a-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="9858a-131">Wanneer **Prijsorder** is geselecteerd, worden in Sales automatisch alle instellingen weergegeven die zijn geconfigureerd in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9858a-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="9858a-132">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="9858a-132">Limitations</span></span>

<span data-ttu-id="9858a-133">Wanneer de kolommen in Sales zijn ingevuld, gelden de volgende beperkingen:</span><span class="sxs-lookup"><span data-stu-id="9858a-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="9858a-134">De instellingen van toeslagen en toeslagtoewijzingen in Supply Chain Management worden niet in Sales gerepliceerd.</span><span class="sxs-lookup"><span data-stu-id="9858a-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="9858a-135">Voor prijzen wordt geen rekening gehouden met speciale adviesprijzen die zijn opgegeven in de kolom **Detailhandelafzetkanaal** op de pagina Verkooporderregel in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9858a-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="9858a-136">Kortingen die zijn gedefinieerd in de sectie **Beheer van handelstoeslag** van Supply Chain Management worden niet meegenomen.</span><span class="sxs-lookup"><span data-stu-id="9858a-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
