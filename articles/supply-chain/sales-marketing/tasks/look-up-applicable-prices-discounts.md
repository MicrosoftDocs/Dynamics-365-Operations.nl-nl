---
title: Van toepassing zijnde prijzen en kortingen opzoeken
description: Deze procedure laat zien hoe u de prijs en/of de korting vindt voor een product dat momenteel geldig is voor een specifieke klant, zonder een verkooporder te maken.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ea4c7db203d0b47c59b241c9d89c69c71cf6cb1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211923"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="a4019-103">Van toepassing zijnde prijzen en kortingen opzoeken</span><span class="sxs-lookup"><span data-stu-id="a4019-103">Look up applicable prices and discounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4019-104">Deze procedure laat zien hoe u de prijs en/of de korting vindt voor een product dat momenteel geldig is voor een specifieke klant, zonder een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="a4019-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="a4019-105">De procedure doorloopt een specifiek voorbeeld en u moet het voorbeeld met het demobedrijf USMF volgen om de benodigde waarden te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a4019-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="a4019-106">De toepasselijke prijs zoeken</span><span class="sxs-lookup"><span data-stu-id="a4019-106">Find the applicable price</span></span>
1. <span data-ttu-id="a4019-107">Ga naar Verkoop en marketing > Prijzen en kortingen > Prijzen zoeken.</span><span class="sxs-lookup"><span data-stu-id="a4019-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="a4019-108">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="a4019-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a4019-109">Zoek en selecteer in de lijst klant US-001.</span><span class="sxs-lookup"><span data-stu-id="a4019-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="a4019-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4019-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a4019-111">Typ in het veld Artikelnummer de waarde 'T0004'.</span><span class="sxs-lookup"><span data-stu-id="a4019-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="a4019-112">Standaard is het veld Hoeveelheid ingesteld op 1.</span><span class="sxs-lookup"><span data-stu-id="a4019-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="a4019-113">Echter, als u de grootte van de order weet die de klant van plan is voor het product te plaatsen, gebruikt u in plaats daarvan deze waarde.</span><span class="sxs-lookup"><span data-stu-id="a4019-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="a4019-114">Deze informatie is alleen relevant als de handelsovereenkomsten met de klant hoeveelheidscategorieën bevatten, dat wil zeggen dat de prijs van het product afhankelijk is van de aangeschafte minimumhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="a4019-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="a4019-115">Voer in het datumveld een datum in voor wanneer de klant verwacht een order te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="a4019-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="a4019-116">De datum kan de datum van vandaag of een datum in de toekomst zijn.</span><span class="sxs-lookup"><span data-stu-id="a4019-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="a4019-117">Het systeem retourneert nu de prijs die geldig is voor het geselecteerde product als het wordt gekocht door de geselecteerde klant op de geselecteerde datum met een opgegeven hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="a4019-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="a4019-118">Als klant US-001 in dit voorbeeld vandaag 1 eenheid van product T0004 koopt, wordt CAD 350 per eenheid in rekening gebracht.</span><span class="sxs-lookup"><span data-stu-id="a4019-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="a4019-119">Deze prijs komt uit een bestaande en actieve handelsovereenkomst met de klant.</span><span class="sxs-lookup"><span data-stu-id="a4019-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="a4019-120">Andere velden op de pagina bevatten meer details over de productprijs en de productkosten (indien ingesteld in het productmodel), en berekende rentabiliteit.</span><span class="sxs-lookup"><span data-stu-id="a4019-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="a4019-121">Als de optie Verwante productvarianten weergeven is ingeschakeld, betekent dit dat er extra handelsovereenkomsten voor varianten van het product zijn.</span><span class="sxs-lookup"><span data-stu-id="a4019-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="a4019-122">Klik op het selectievakje Verwante productvarianten weergeven.</span><span class="sxs-lookup"><span data-stu-id="a4019-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="a4019-123">Een lijst van de productvarianten wordt weergegeven, met informatie over de dimensies ervan.</span><span class="sxs-lookup"><span data-stu-id="a4019-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="a4019-124">Markeer in de lijst de regel die de kleur wit voorstelt.</span><span class="sxs-lookup"><span data-stu-id="a4019-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="a4019-125">De productprijs verschilt nu van de prijs die eerder werd weergegeven, toen deze niet per dimensie was opgegeven.</span><span class="sxs-lookup"><span data-stu-id="a4019-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="a4019-126">Klik op Verkoopprijzen weergeven.</span><span class="sxs-lookup"><span data-stu-id="a4019-126">Click View sales prices.</span></span>
    * <span data-ttu-id="a4019-127">De pagina Prijs (verkoop) bevat alle handelsovereenkomsten die van toepassing zijn op het product, inclusief de varianten ervan.</span><span class="sxs-lookup"><span data-stu-id="a4019-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="a4019-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4019-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="a4019-129">De toepasselijke korting zoeken</span><span class="sxs-lookup"><span data-stu-id="a4019-129">Find the applicable discount</span></span>
<span data-ttu-id="a4019-130">Zorg ervoor dat het veld Klantrekening klantnummer US-001 bevat. </span><span class="sxs-lookup"><span data-stu-id="a4019-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="a4019-131">Typ in het veld Artikelnummer de waarde 'T0012'.</span><span class="sxs-lookup"><span data-stu-id="a4019-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="a4019-132">Zorg dat het veld Hoeveelheid is ingesteld op 1.</span><span class="sxs-lookup"><span data-stu-id="a4019-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="a4019-133">De volgende prijsgegevens die worden weergegeven voor product T0012, komen uit een of meerdere handelsovereenkomsten: de eenheidsprijs is CAD 1,000 en het kortingspercentage is 5.</span><span class="sxs-lookup"><span data-stu-id="a4019-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="a4019-134">Stel Hoeveelheid in op '20'.</span><span class="sxs-lookup"><span data-stu-id="a4019-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="a4019-135">De verhoogde orderhoeveelheid leidt ertoe dat de regelkorting die aan de klant wordt aangeboden, verandert van 5 in 7 procent.</span><span class="sxs-lookup"><span data-stu-id="a4019-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="a4019-136">Het nettobedrag wordt berekend op basis van de eenheidsprijs, de korting en de totale hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="a4019-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="a4019-137">Klik op Regelkorting weergeven.</span><span class="sxs-lookup"><span data-stu-id="a4019-137">Click View line discount.</span></span>
    * <span data-ttu-id="a4019-138">Er zijn twee regelkortingovereenkomsten voor product T0012, die een korting van 5% opgeven voor een orderregelhoeveelheid van 1 tot 10, en een korting van 7% voor orderhoeveelheden boven 10.</span><span class="sxs-lookup"><span data-stu-id="a4019-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="a4019-139">Merk op dat de kortingen worden toegepast op een groep producten, in dit voorbeeld groepscode 01, waarvan product T0012 lid is.</span><span class="sxs-lookup"><span data-stu-id="a4019-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="a4019-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4019-140">Close the page.</span></span>

