---
title: Een nieuwe handelsovereenkomst maken
description: Deze procedure laat zien hoe u een handelsovereenkomst maakt waarin u een nieuwe productverkoopprijs registreert die u met een specifieke klant bent overeengekomen.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1221bb57aea4c93cb60fc29caec2d3b41798f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836393"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="0dd76-103">Een nieuwe handelsovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="0dd76-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0dd76-104">Deze procedure laat zien hoe u een handelsovereenkomst maakt waarin u een nieuwe productverkoopprijs registreert die u met een specifieke klant bent overeengekomen.</span><span class="sxs-lookup"><span data-stu-id="0dd76-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="0dd76-105">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="0dd76-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0dd76-106">Als u uw eigen gegevens gebruikt, moet u voordat u deze guide start ervoor zorgen dat er een handelsovereenkomstjournaal bestaat met de naam Standaard, waarvan de relatie is ingesteld op "Prijs (verkoop)".</span><span class="sxs-lookup"><span data-stu-id="0dd76-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="0dd76-107">Een nieuw handelsovereenkomstjournaal maken en boeken</span><span class="sxs-lookup"><span data-stu-id="0dd76-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="0dd76-108">Ga naar **Navigatievenster > Modules > Verkoop en marketing > Prijzen en kortingen > Handelsovereenkomstjournalen**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="0dd76-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-109">Click **New**.</span></span>
3. <span data-ttu-id="0dd76-110">Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0dd76-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0dd76-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0dd76-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0dd76-112">Klik in het **actievenster** op **Regels**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="0dd76-113">Selecteer Tabel in het veld **Rekeningcode**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="0dd76-114">In dit voorbeeld werkt u de prijs voor een specifieke klant bij, wat betekent dat u mogelijk Tabel moet kiezen.</span><span class="sxs-lookup"><span data-stu-id="0dd76-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="0dd76-115">Als u de catalogusprijs van het product zou bijwerken, zou u Alle selecteren, zodat de nieuwe prijs voor alle klanten geldt.</span><span class="sxs-lookup"><span data-stu-id="0dd76-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="0dd76-116">Als u onderscheid zou maken tussen verschillende prijzen uit verschillende klantsegmenten, zou u Groep selecteren.</span><span class="sxs-lookup"><span data-stu-id="0dd76-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="0dd76-117">Als u Groep wilt selecteren, moet u klantprijsgroepen hebben ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0dd76-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="0dd76-118">Klik in het veld **Rekening selecteren** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0dd76-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0dd76-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0dd76-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="0dd76-120">Selecteer Tabel in het veld **Artikelcode**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="0dd76-121">Wanneer u een handelsovereenkomst van het type Prijs (verkoop) invoert, moet u alleen Tabel selecteren in het veld **Artikelcode**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="0dd76-122">Dit komt doordat een prijs een absolute waarde is en niet voor alle producten of groep producten hetzelfde kan zijn.</span><span class="sxs-lookup"><span data-stu-id="0dd76-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="0dd76-123">Klik in het veld **Artikelrelatie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0dd76-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0dd76-124">Selecteer in de lijst het product dat u in de overeenkomst wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="0dd76-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="0dd76-125">Maak een notitie van het product dat u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0dd76-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="0dd76-126">Voer in het veld **Van** een minimumhoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="0dd76-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="0dd76-127">Als de klant een minimumhoeveelheid moet bestellen voordat deze voor de nieuwe prijs in aanmerking komt, moet u die hoeveelheid hier opgeven.</span><span class="sxs-lookup"><span data-stu-id="0dd76-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="0dd76-128">Voer een waarde in het veld **Tot** in om de maximale hoeveelheid op te geven waarboven de prijs van de overeenkomst niet geldig is.</span><span class="sxs-lookup"><span data-stu-id="0dd76-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="0dd76-129">Als u prijzen en kortingen aanbiedt op basis van meerdere hoeveelheidscategorieën, geeft u elke hoeveelheidsbracket op als een minimum- en een maximumwaarde in het veld **Van** en het veld **Tot**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="0dd76-130">Voer in het veld **Bedrag in valuta** een prijs in.</span><span class="sxs-lookup"><span data-stu-id="0dd76-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="0dd76-131">Voer in de sectie **Details** in het veld **Begindatum** een datum in waarop deze overeenkomst geldig is.</span><span class="sxs-lookup"><span data-stu-id="0dd76-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="0dd76-132">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-132">Click **Save**.</span></span>
16. <span data-ttu-id="0dd76-133">Klik op **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-133">Click **Validate**.</span></span>
17. <span data-ttu-id="0dd76-134">Klik op **Geselecteerde regels valideren**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="0dd76-135">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-135">Click **OK**.</span></span>
19. <span data-ttu-id="0dd76-136">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-136">Click **Post**.</span></span>
20. <span data-ttu-id="0dd76-137">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="0dd76-138">Handelsovereenkomsten voor een product weergeven</span><span class="sxs-lookup"><span data-stu-id="0dd76-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="0dd76-139">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="0dd76-140">Zoek en selecteer in de lijst het product waarvan u de prijs zojuist hebt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0dd76-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="0dd76-141">Klik in het **actievenster** op **Verkopen**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="0dd76-142">Klik op **Handelsovereenkomsten weergeven**.</span><span class="sxs-lookup"><span data-stu-id="0dd76-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="0dd76-143">Controleer de gegevens van de prijshandelsovereenkomst die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0dd76-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="0dd76-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0dd76-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0dd76-145">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0dd76-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="0dd76-146">Whitepaper</span><span class="sxs-lookup"><span data-stu-id="0dd76-146">Whitepaper</span></span>
<span data-ttu-id="0dd76-147">Download de volgende whitepaper (geschreven ter ondersteuning van AX2012, maar is nog steeds van toepassing op Dynamics 365 Supply Chain Management) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0dd76-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>
- [<span data-ttu-id="0dd76-148">Handelsovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="0dd76-148">Trade agreements</span></span>](https://mbs.microsoft.com/files/public/CS/AX2012R3/TradeagreementsinAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="0dd76-149">Community-blogs</span><span class="sxs-lookup"><span data-stu-id="0dd76-149">Community blogs</span></span>
- [<span data-ttu-id="0dd76-150">Verkoopprijzen in Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0dd76-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]