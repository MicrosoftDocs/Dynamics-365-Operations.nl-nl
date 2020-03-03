---
title: De optimale combinatie van overlappende kortingen bepalen
description: Als kortingen elkaar overlappen, moet u bepalen welke combinatie van overlappende kortingen leidt tot het laagste totaalbedrag voor de transactie of de hoogste totale korting. Wanneer het kortingsbedrag varieert afhankelijk van de prijs van de producten die worden aangeschaft, zoals in de veelgebruikte retailkorting 'koop 1, krijg 1 met X procent korting' (BOGO), wordt dit proces een kwestie van combinatorische optimalisatie.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 565722da65cbb711acedb5acf7de4edfbd615314
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022190"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a><span data-ttu-id="b87c8-104">De optimale combinatie van overlappende kortingen bepalen</span><span class="sxs-lookup"><span data-stu-id="b87c8-104">Determine the optimal combination of overlapping discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b87c8-105">Als kortingen elkaar overlappen, moet u bepalen welke combinatie van overlappende kortingen leidt tot het laagste totaalbedrag voor de transactie of de hoogste totale korting.</span><span class="sxs-lookup"><span data-stu-id="b87c8-105">When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</span></span> <span data-ttu-id="b87c8-106">Wanneer het kortingsbedrag varieert afhankelijk van de prijs van de producten die worden aangeschaft, zoals in de veelgebruikte retailkorting 'Koop 1, krijg 1 met X procent korting' (BOGO), wordt dit proces een kwestie van combinatorische optimalisatie.</span><span class="sxs-lookup"><span data-stu-id="b87c8-106">When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</span></span>

<span data-ttu-id="b87c8-107">Dit artikel is van toepassing op Microsoft Dynamics AX 2012 R3 met KB 3105973 (uitgebracht op 2 november 2015) of hoger, en op Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b87c8-107">This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Dynamics 365 Commerce.</span></span> <span data-ttu-id="b87c8-108">Om de combinatie van overlappende kortingen die u wilt toepassen snel te bepalen, hebben we een methode voor het toepassen van overlappende kortingen ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="b87c8-108">To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</span></span> <span data-ttu-id="b87c8-109">We noemen deze nieuwe methode **marginale-waardeclassificatie**.</span><span class="sxs-lookup"><span data-stu-id="b87c8-109">We call this new method **marginal value ranking**.</span></span> <span data-ttu-id="b87c8-110">Marginale-waardeclassificatie wordt gebruikt wanneer de tijd die nodig is om mogelijke combinaties van overlappende kortingen te evalueren een drempel overschrijdt die u kunt configureren op de pagina **Commerce-parameters**.</span><span class="sxs-lookup"><span data-stu-id="b87c8-110">Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the **Commerce parameters** page.</span></span> <span data-ttu-id="b87c8-111">In de methode voor marginale-waardeclassificatie wordt een waarde berekend voor elke overlappende korting door middel van de waarde van de korting op de gedeelde producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-111">In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</span></span> <span data-ttu-id="b87c8-112">De overlappende kortingen worden dan toegepast, vanaf de hoogste relatieve waarde tot de laagste relatieve waarde.</span><span class="sxs-lookup"><span data-stu-id="b87c8-112">The overlapped discounts are then applied from the highest relative value to the lowest relative value.</span></span> <span data-ttu-id="b87c8-113">Zie de sectie 'Marginale waarde' verderop in dit artikel voor meer informatie over de nieuwe methode.</span><span class="sxs-lookup"><span data-stu-id="b87c8-113">For details about the new method, see the "Marginal value" section, later in this article.</span></span> <span data-ttu-id="b87c8-114">Marginale-waardeclassificatie wordt niet gebruikt wanneer de kortingsbedragen voor een product niet worden beïnvloed door een ander product in de transactie.</span><span class="sxs-lookup"><span data-stu-id="b87c8-114">Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</span></span> <span data-ttu-id="b87c8-115">Deze methode wordt bijvoorbeeld niet gebruikt voor twee eenvoudige kortingen of voor een eenvoudige korting en een kwantumkorting voor een enkel product.</span><span class="sxs-lookup"><span data-stu-id="b87c8-115">For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</span></span>

## <a name="discount-examples"></a><span data-ttu-id="b87c8-116">Kortingsvoorbeelden</span><span class="sxs-lookup"><span data-stu-id="b87c8-116">Discount examples</span></span>

<span data-ttu-id="b87c8-117">U kunt een onbeperkt aantal kortingen voor een gemeenschappelijke set van producten maken.</span><span class="sxs-lookup"><span data-stu-id="b87c8-117">You can create an unlimited number of discounts on a common set of products.</span></span> <span data-ttu-id="b87c8-118">Omdat er geen limiet is, kunnen echter prestatieproblemen optreden wanneer u probeert om de kortingen te berekenen die moeten worden gebruikt voor de verschillende producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-118">However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</span></span> <span data-ttu-id="b87c8-119">In de volgende voorbeelden wordt deze kwestie nader toegelicht.</span><span class="sxs-lookup"><span data-stu-id="b87c8-119">The following examples illustrate this issue in more detail.</span></span> <span data-ttu-id="b87c8-120">In voorbeeld 1 beginnen we met twee producten en twee overlappende kortingen.</span><span class="sxs-lookup"><span data-stu-id="b87c8-120">In example 1, we start with two products and two overlapping discounts.</span></span> <span data-ttu-id="b87c8-121">Vervolgens wordt in voorbeeld 2 getoond hoe het probleem uitdijt wanneer meer producten worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b87c8-121">Then, in example 2, we show how the issue evolves as more products are added.</span></span>

### <a name="example-1-two-products-and-two-discounts"></a><span data-ttu-id="b87c8-122">Voorbeeld 1: Twee producten en twee kortingen</span><span class="sxs-lookup"><span data-stu-id="b87c8-122">Example 1: Two products and two discounts</span></span>

<span data-ttu-id="b87c8-123">In dit voorbeeld zijn twee producten nodig om in aanmerking te komen voor elke korting en de kortingen kunnen niet worden gecombineerd.</span><span class="sxs-lookup"><span data-stu-id="b87c8-123">In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</span></span> <span data-ttu-id="b87c8-124">De kortingen in dit voorbeeld zijn **Beste prijs**-kortingen.</span><span class="sxs-lookup"><span data-stu-id="b87c8-124">The discounts in this example are **Best price** discounts.</span></span> <span data-ttu-id="b87c8-125">Beide producten komen in aanmerking voor beide kortingen.</span><span class="sxs-lookup"><span data-stu-id="b87c8-125">Both products qualify for both discounts.</span></span> <span data-ttu-id="b87c8-126">Dit zijn de twee kortingen.</span><span class="sxs-lookup"><span data-stu-id="b87c8-126">Here are the two discounts.</span></span>

![Voorbeeld van twee Beste prijs-kortingen](./media/overlapping-discount-combo-01.jpg)

<span data-ttu-id="b87c8-128">Voor elke combinatie van twee producten is de beste van deze twee kortingen afhankelijk van de prijzen van de twee producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-128">For any two products, the better of these two discounts depends on the prices of the two products.</span></span> <span data-ttu-id="b87c8-129">Wanneer de prijs van beide producten bijna gelijk of gelijk is, is korting 1 beter.</span><span class="sxs-lookup"><span data-stu-id="b87c8-129">When the price of both products is equal or almost equal, discount 1 is better.</span></span> <span data-ttu-id="b87c8-130">Wanneer de prijs van een product aanzienlijk lager is dan de prijs van het andere product, is korting 2 beter.</span><span class="sxs-lookup"><span data-stu-id="b87c8-130">When the price of one product is significantly less than the price of the other product, discount 2 is better.</span></span> <span data-ttu-id="b87c8-131">Hier volgt de wiskundige regel voor het evalueren van de twee kortingen ten opzichte van elkaar.</span><span class="sxs-lookup"><span data-stu-id="b87c8-131">Here is the mathematical rule for evaluating these two discounts against each other.</span></span>

![Regel voor het evalueren van de kortingen](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> <span data-ttu-id="b87c8-133">Wanneer de prijs van product 1 gelijk is aan tweederde van de prijs van product 2, zijn de twee kortingen gelijk.</span><span class="sxs-lookup"><span data-stu-id="b87c8-133">When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</span></span> <span data-ttu-id="b87c8-134">In dit voorbeeld varieert het effectieve kortingspercentage voor korting 1 van enkele procenten (wanneer de prijzen van de twee producten ver uit elkaar liggen) tot maximaal 25 procent (wanneer de twee producten dezelfde prijs hebben).</span><span class="sxs-lookup"><span data-stu-id="b87c8-134">In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</span></span> <span data-ttu-id="b87c8-135">Het effectieve kortingspercentage voor korting 2 ligt vast.</span><span class="sxs-lookup"><span data-stu-id="b87c8-135">The effective discount percentage for discount 2 is fixed.</span></span> <span data-ttu-id="b87c8-136">Dit bedraagt altijd 20 procent.</span><span class="sxs-lookup"><span data-stu-id="b87c8-136">It's always 20 percent.</span></span> <span data-ttu-id="b87c8-137">Aangezien het effectieve kortingspercentage voor korting 1 een bereik heeft waarin het hoger of lager kan liggen dan korting 2, is de beste korting afhankelijk van de prijzen van de twee producten waarop de korting wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="b87c8-137">Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</span></span> <span data-ttu-id="b87c8-138">In dit voorbeeld wordt de berekening is snel voltooid, omdat slechts twee kortingen worden toegepast op slechts twee producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-138">In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</span></span> <span data-ttu-id="b87c8-139">Er zijn slechts twee mogelijke combinaties: toepassing van korting 1 of toepassing van korting 2.</span><span class="sxs-lookup"><span data-stu-id="b87c8-139">There are only two possible combinations: one application of discount 1 or one application of discount 2.</span></span> <span data-ttu-id="b87c8-140">Er zijn geen permutaties die moeten worden berekend.</span><span class="sxs-lookup"><span data-stu-id="b87c8-140">There are no permutations to calculate.</span></span> <span data-ttu-id="b87c8-141">De waarde van elke korting wordt berekend met behulp van beide producten en de beste korting wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b87c8-141">The value of each discount is calculated by using both products, and the best discount is used.</span></span>

### <a name="example-2-four-products-and-two-discounts"></a><span data-ttu-id="b87c8-142">Voorbeeld 2: Vier producten en twee kortingen</span><span class="sxs-lookup"><span data-stu-id="b87c8-142">Example 2: Four products and two discounts</span></span>

<span data-ttu-id="b87c8-143">Vervolgens gebruiken we vier producten en dezelfde twee kortingen.</span><span class="sxs-lookup"><span data-stu-id="b87c8-143">Next, we will use four products and the same two discounts.</span></span> <span data-ttu-id="b87c8-144">Alle vier producten komen in aanmerking voor beide kortingen.</span><span class="sxs-lookup"><span data-stu-id="b87c8-144">All four products qualify for both discounts.</span></span> <span data-ttu-id="b87c8-145">Er zijn twaalf mogelijke combinaties.</span><span class="sxs-lookup"><span data-stu-id="b87c8-145">There are twelve possible combinations.</span></span> <span data-ttu-id="b87c8-146">Uiteindelijk worden twee kortingen toegepast op de transactie, in één van drie combinaties: twee toepassingen van korting 1, twee toepassingen van 2 of één toepassing van korting 1 en één toepassing van korting 2.</span><span class="sxs-lookup"><span data-stu-id="b87c8-146">In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</span></span> <span data-ttu-id="b87c8-147">Ter illustratie van de mogelijke combinaties gaan we twee verschillende sets bekijken van vier producten met verschillende prijzen:</span><span class="sxs-lookup"><span data-stu-id="b87c8-147">To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</span></span>

- <span data-ttu-id="b87c8-148">Alle vier producten hebben dezelfde prijs, namelijk € 15.00.</span><span class="sxs-lookup"><span data-stu-id="b87c8-148">All four products have the same price, $15.00.</span></span> <span data-ttu-id="b87c8-149">In dit geval bestaat de beste combinatie van kortingen uit twee toepassingen van korting 1.</span><span class="sxs-lookup"><span data-stu-id="b87c8-149">In this case, the best discount combination is two applications of discount 1.</span></span> <span data-ttu-id="b87c8-150">Twee producten hebben de volledige prijs en twee producten hebben een korting van 50 procent.</span><span class="sxs-lookup"><span data-stu-id="b87c8-150">Two products will be full price, and two will be 50 percent off.</span></span> <span data-ttu-id="b87c8-151">De totale korting voor de transactie is € 45 (15 + 15 + 7,50 + 7,50), € 15 (25 procent) lager dan het totaalbedrag zonder korting van € 60.</span><span class="sxs-lookup"><span data-stu-id="b87c8-151">The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</span></span> <span data-ttu-id="b87c8-152">Korting 2 bedraagt slechts € 12 (20 procent).</span><span class="sxs-lookup"><span data-stu-id="b87c8-152">Discount 2 is only $12 (20 percent).</span></span>
- <span data-ttu-id="b87c8-153">Twee producten zijn elk € 20, één product is € 15 en één product is € 5.</span><span class="sxs-lookup"><span data-stu-id="b87c8-153">Two products are $20 each, one product is $15, and one product is $5.</span></span> <span data-ttu-id="b87c8-154">In dit geval bestaat de beste combinatie van kortingen uit één toepassing van korting 2 en één toepassing van korting 1.</span><span class="sxs-lookup"><span data-stu-id="b87c8-154">In this case, the best discount combination is one application of discount 2 and one application of discount 1.</span></span> <span data-ttu-id="b87c8-155">In de volgende tabellen ziet u de kortingen uitgespeld.</span><span class="sxs-lookup"><span data-stu-id="b87c8-155">The following tables illustrates the discounts.</span></span>

<span data-ttu-id="b87c8-156">Om de tabellen te lezen moet u een product uit een rij nemen en een product uit een kolom.</span><span class="sxs-lookup"><span data-stu-id="b87c8-156">To read the tables, use one product from a row and one product from a column.</span></span> <span data-ttu-id="b87c8-157">In de tabel voor korting 1 krijgt u bijvoorbeeld € 10 korting als u de twee producten van € 20 combineert.</span><span class="sxs-lookup"><span data-stu-id="b87c8-157">For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</span></span> <span data-ttu-id="b87c8-158">In de tabel voor korting 2 krijgt u € 4 korting als u het product van € 15 combineert met het product van € 5.</span><span class="sxs-lookup"><span data-stu-id="b87c8-158">In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</span></span>

![Voorbeeld waarin vier producten voor dezelfde twee kortingen worden gebruikt](./media/overlapping-discount-combo-03.jpg)

<span data-ttu-id="b87c8-160">Allereerst zoeken we de grootste korting die beschikbaar is voor twee willekeurige producten door middel van een van beide kortingen.</span><span class="sxs-lookup"><span data-stu-id="b87c8-160">First, we find the largest discount that is available from any two products by using either discount.</span></span> <span data-ttu-id="b87c8-161">In de twee tabellen ziet u het kortingsbedrag voor alle combinaties van de twee producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-161">The two tables show the discount amount for all combinations of the two products.</span></span> <span data-ttu-id="b87c8-162">De gearceerde gedeelten van de tabellen staan voor gevallen waarin een product in combinatie met zichzelf wordt genomen, wat we niet mogen doen, of voor een omgekeerde combinatie van twee producten die hetzelfde kortingsbedrag oplevert en kan worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="b87c8-162">The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</span></span> <span data-ttu-id="b87c8-163">Als u de tabellen bekijkt, ziet u dat korting 1 voor de twee artikelen van € 20 de grootste korting is die beschikbaar is voor alle kortingen op alle vier producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-163">By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</span></span> <span data-ttu-id="b87c8-164">Deze korting is groen gemarkeerd in de eerste tabel. Zo blijven twee producten over: dat van € 15 en dat van € 5.</span><span class="sxs-lookup"><span data-stu-id="b87c8-164">(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</span></span> <span data-ttu-id="b87c8-165">Als u opnieuw de twee tabellen bekijkt, ziet u dat voor deze twee producten korting 1 resulteert in een korting van € 2,50, terwijl korting 2 een korting van € 4 oplevert.</span><span class="sxs-lookup"><span data-stu-id="b87c8-165">By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</span></span> <span data-ttu-id="b87c8-166">Daarom selecteren we korting 2.</span><span class="sxs-lookup"><span data-stu-id="b87c8-166">Therefore, we select discount 2.</span></span> <span data-ttu-id="b87c8-167">De totale korting bedraagt € 14.</span><span class="sxs-lookup"><span data-stu-id="b87c8-167">The total discount is $14.</span></span> <span data-ttu-id="b87c8-168">Om deze discussie makkelijker te visualiseren, vindt hier u twee extra tabellen die de het effectieve kortingspercentage weergeven voor alle mogelijke combinaties van twee producten voor zowel korting 1 als korting 2.</span><span class="sxs-lookup"><span data-stu-id="b87c8-168">To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</span></span> <span data-ttu-id="b87c8-169">Hierin is slechts de helft van de lijst met combinaties opgenomen, omdat voor deze twee kortingen de volgorde waarin de twee producten worden aangeboden in de korting niet van belang is.</span><span class="sxs-lookup"><span data-stu-id="b87c8-169">Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</span></span> <span data-ttu-id="b87c8-170">De hoogste effectieve korting (25 procent) is groen gemarkeerd. De laagste effectieve korting (10 procent) is rood gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="b87c8-170">The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</span></span>

![Effectieve kortingspercentage voor alle combinaties van twee producten voor beide kortingen](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> <span data-ttu-id="b87c8-172">Wanneer prijzen variëren en twee of meer kortingen concurreren, kan de beste combinatie van kortingen alleen worden gegarandeerd door beide kortingen te evalueren en met elkaar te vergelijken.</span><span class="sxs-lookup"><span data-stu-id="b87c8-172">When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</span></span>

## <a name="total-possible-combinations"></a><span data-ttu-id="b87c8-173">Totaal aantal mogelijke combinaties</span><span class="sxs-lookup"><span data-stu-id="b87c8-173">Total possible combinations</span></span>

<span data-ttu-id="b87c8-174">In deze sectie gaan we verder met het voorbeeld uit de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="b87c8-174">This section continues the example from the previous section.</span></span> <span data-ttu-id="b87c8-175">We voegen meer producten en nog een korting toe en zien hoeveel combinaties moeten worden berekend en vergeleken.</span><span class="sxs-lookup"><span data-stu-id="b87c8-175">We will add more products and another discount, and see how many combinations must be calculated and compared.</span></span> <span data-ttu-id="b87c8-176">In de volgende tabel ziet u het aantal mogelijke kortingscombinaties bij een toenemend aantal producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-176">The following table shows the number of possible discount combinations as the product quantity increases.</span></span> <span data-ttu-id="b87c8-177">U ziet hier wat er gebeurt wanneer er twee overlappende kortingen zijn zoals in het vorige voorbeeld, en ok wanneer er drie overlappende kortingen zijn.</span><span class="sxs-lookup"><span data-stu-id="b87c8-177">The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</span></span> <span data-ttu-id="b87c8-178">Het aantal mogelijke kortingscombinaties dat moet worden geëvalueerd neemt snel toe, en zelfs een krachtige computer kan dan de berekening en vergelijking niet snel genoeg uitvoeren om acceptabel zijn voor detailhandeltransacties.</span><span class="sxs-lookup"><span data-stu-id="b87c8-178">The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</span></span>

![Aantal mogelijke kortingscombinaties bij een toenemend aantal producten](./media/overlapping-discount-combo-05.jpg)

<span data-ttu-id="b87c8-180">Wanneer nog grotere hoeveelheden of meer overlappende kortingen worden toegepast, loopt het totale aantal mogelijke kortingscombinaties snel in de miljoenen. De tijd die nodig is om deze te evalueren en de best mogelijke combinatie te selecteren wordt dan snel merkbaar.</span><span class="sxs-lookup"><span data-stu-id="b87c8-180">When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</span></span> <span data-ttu-id="b87c8-181">Enige optimalisatie is doorgevoerd in de prijsengine om het totale aantal combinaties te verlagen dat moet worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="b87c8-181">Some optimizations have been done in the price engine to reduce the total number of combinations that must be evaluated.</span></span> <span data-ttu-id="b87c8-182">Omdat het aantal overlappende kortingen en de aantallen in een transactie niet worden beperkt, moet echter altijd een groot aantal combinaties worden geëvalueerd wanneer er overlappende kortingen zijn.</span><span class="sxs-lookup"><span data-stu-id="b87c8-182">However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</span></span> <span data-ttu-id="b87c8-183">Dit is het probleem waarop de de marginale-waardemethode zich richt.</span><span class="sxs-lookup"><span data-stu-id="b87c8-183">This issue is the issue that the marginal value ranking method addresses.</span></span>

## <a name="marginal-value-method"></a><span data-ttu-id="b87c8-184">Marginale-waardemethode</span><span class="sxs-lookup"><span data-stu-id="b87c8-184">Marginal value method</span></span>

<span data-ttu-id="b87c8-185">Om het probleem op te lossen van exponentieel toenemende aantallen combinaties die moeten worden geëvalueerd, bestaat een optimalisatie die de waarde berekent per gedeeld product van elke korting op de reeks producten waarop twee of meer kortingen kunnen worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="b87c8-185">To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</span></span> <span data-ttu-id="b87c8-186">Deze waarde noemen we de **marginale waarde** van de korting voor de gedeelde producten.</span><span class="sxs-lookup"><span data-stu-id="b87c8-186">We refer to this value as the **marginal value** of the discount for the shared products.</span></span> <span data-ttu-id="b87c8-187">De marginale waarde is de toename van het gemiddelde per product in het totale kortingsbedrag, wanneer de gedeelde producten worden opgenomen in elke korting.</span><span class="sxs-lookup"><span data-stu-id="b87c8-187">The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</span></span> <span data-ttu-id="b87c8-188">De marginale waarde wordt berekend door van het totale kortingsbedrag (DTotal) het kortingsbedrag zonder de gedeelde producten af te trekken (DMinus\\ Shared) en dit verschil te delen door het aantal gedeelde producten (ProductsShared).</span><span class="sxs-lookup"><span data-stu-id="b87c8-188">The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus\\ Shared), and dividing that difference by the number of shared products (ProductsShared).</span></span>

![Formule voor het berekenen van de marginale waarde](./media/overlapping-discount-combo-06.jpg)

<span data-ttu-id="b87c8-190">Nadat de marginale waarde van elke korting voor een gedeelde reeks producten is berekend, worden de kortingen toegepast op de gedeelde producten in de volledige volgorde van de hoogste marginale waarde tot de laagste marginale waarde.</span><span class="sxs-lookup"><span data-stu-id="b87c8-190">After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</span></span> <span data-ttu-id="b87c8-191">Bij deze methode worden niet telkens alle resterende kortingsmogelijkheden vergeleken zodra één exemplaar van een korting is toegepast.</span><span class="sxs-lookup"><span data-stu-id="b87c8-191">For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</span></span> <span data-ttu-id="b87c8-192">In plaats daarvan worden de overlappende kortingen eenmaal vergeleken en vervolgens op volgorde toegepast.</span><span class="sxs-lookup"><span data-stu-id="b87c8-192">Instead, the overlapping discounts are compared one time and then applied in order.</span></span> <span data-ttu-id="b87c8-193">Er worden geen extra vergelijkingen uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b87c8-193">No additional comparisons are done.</span></span> <span data-ttu-id="b87c8-194">U kunt de drempel voor overschakelen naar de marginale-waardemethode configureren op het tabblad **Korting** van de pagina **Commerce-parameters**.</span><span class="sxs-lookup"><span data-stu-id="b87c8-194">You can configure the threshold to switch to the marginal value method on the **Discount** tab of the **Commerce parameters** page.</span></span> <span data-ttu-id="b87c8-195">Welke tijd acceptabel is voor berekening van de totale korting, verschilt van sector tot sector.</span><span class="sxs-lookup"><span data-stu-id="b87c8-195">The acceptable time to calculate the total discount varies across retail industries.</span></span> <span data-ttu-id="b87c8-196">Deze tijd ligt echter over het algemeen ergens tussen enkele tientallen milliseconden tot één seconde.</span><span class="sxs-lookup"><span data-stu-id="b87c8-196">However, this time generally falls in the range of tens of milliseconds to one second.</span></span>