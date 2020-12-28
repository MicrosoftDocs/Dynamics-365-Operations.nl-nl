---
title: Een vrijgaveorder voor inkoop maken wanneer de inkooporder wordt gemaakt
description: Deze procedure laat zien hoe u een inkoopovereenkomst gebruikt wanneer u een inkooporder maakt.
author: mkirknel
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3e02bd4aaef8da7838c92199c28b1e298078c57
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425385"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="783b4-103">Een vrijgaveorder voor inkoop maken wanneer de inkooporder wordt gemaakt</span><span class="sxs-lookup"><span data-stu-id="783b4-103">Create a purchase release order when creating the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="783b4-104">Deze procedure laat zien hoe u een inkoopovereenkomst gebruikt wanneer u een inkooporder maakt.</span><span class="sxs-lookup"><span data-stu-id="783b4-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="783b4-105">De inkoopovereenkomst moet worden toegepast wanneer u de inkooporder maakt omdat er algemene voorwaarden zijn die naar de koptekst van de inkooporder moeten worden gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="783b4-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="783b4-106">Deze taak worden meestal uitgevoerd door een inkoopagent.</span><span class="sxs-lookup"><span data-stu-id="783b4-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="783b4-107">Als vereiste voor deze taakbegeleiding moet u een effectieve inkoopovereenkomst met een toezegging van een producthoeveelheid hebben voor een leverancier en voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="783b4-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="783b4-108">Dezelfde procedure kan worden gebruikt als u een inkoopovereenkomst met andere typen toezeggingen hebt.</span><span class="sxs-lookup"><span data-stu-id="783b4-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="783b4-109">U kunt deze handleiding uitvoeren in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="783b4-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="783b4-110">Als u USMF gebruikt, kunt u eerst de begeleiding "Een inkoopovereenkomst maken" uitvoeren om de benodigde condities voor deze begeleiding in te stellen.</span><span class="sxs-lookup"><span data-stu-id="783b4-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="783b4-111">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="783b4-111">Create a purchase order</span></span>
1. <span data-ttu-id="783b4-112">Open het werkgebied voor het voorbereiden van inkooporders.</span><span class="sxs-lookup"><span data-stu-id="783b4-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="783b4-113">Klik op Nieuwe inkooporder.</span><span class="sxs-lookup"><span data-stu-id="783b4-113">Click New purchase order.</span></span>
3. <span data-ttu-id="783b4-114">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="783b4-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="783b4-115">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="783b4-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="783b4-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="783b4-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="783b4-117">Schakel de uitbreiding van de sectie Algemeen om.</span><span class="sxs-lookup"><span data-stu-id="783b4-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="783b4-118">Klik in het veld Inkoopovereenkomst op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="783b4-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="783b4-119">Alle beschikbare overeenkomsten voor de leverancier worden hier weergegeven.</span><span class="sxs-lookup"><span data-stu-id="783b4-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="783b4-120">Zoek de effectieve overeenkomst die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="783b4-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="783b4-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="783b4-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="783b4-122">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="783b4-122">Click Yes.</span></span>
10. <span data-ttu-id="783b4-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="783b4-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="783b4-124">Een regel toevoegen</span><span class="sxs-lookup"><span data-stu-id="783b4-124">Add a line</span></span>
1. <span data-ttu-id="783b4-125">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="783b4-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="783b4-126">Als er specifieke voorraad- of locatiedimensies in de toezegging zijn, moet u dezelfde waarden invoeren op de inkooporderregel om de overeenkomst te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="783b4-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="783b4-127">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="783b4-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="783b4-128">De locatie kan al gevuld zijn met de standaardwaarde van de order, of van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="783b4-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="783b4-129">Als dit het geval is, slaat u deze stap over.</span><span class="sxs-lookup"><span data-stu-id="783b4-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="783b4-130">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="783b4-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="783b4-131">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="783b4-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="783b4-132">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="783b4-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="783b4-133">Controleer of de prijs uit de toezegging is gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="783b4-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="783b4-134">De toezegging opzoeken</span><span class="sxs-lookup"><span data-stu-id="783b4-134">Look up the commitment</span></span>
1. <span data-ttu-id="783b4-135">Klik op Regel bijwerken.</span><span class="sxs-lookup"><span data-stu-id="783b4-135">Click Update line.</span></span>
2. <span data-ttu-id="783b4-136">Klik op Gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="783b4-136">Click Attached.</span></span>
    * <span data-ttu-id="783b4-137">Hier kunt u gegevens voor de inkoopovereenkomst opvragen.</span><span class="sxs-lookup"><span data-stu-id="783b4-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="783b4-138">U kunt bijvoorbeeld de prijs zien en of de prijs en korting vast zijn, wat betekent dat als u de prijs of korting op de inkooporder wijzigt in een andere waarde dan in de toezegging, het systeem de koppeling verwijdert zodat de inkooporderregel niet aan de toezegging voldoet.</span><span class="sxs-lookup"><span data-stu-id="783b4-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="783b4-139">U kunt ook zien of de optie Max is afgedwongen is geselecteerd, wat aangeeft dat de hoeveelheid in de toezegging niet kan worden overschreden door alle inkopen op te tellen die aan de toezegging voldoen.</span><span class="sxs-lookup"><span data-stu-id="783b4-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="783b4-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="783b4-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="783b4-141">De inkoopovereenkomst opzoeken</span><span class="sxs-lookup"><span data-stu-id="783b4-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="783b4-142">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="783b4-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="783b4-143">Klik op Inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="783b4-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="783b4-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="783b4-144">Close the page.</span></span>
4. <span data-ttu-id="783b4-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="783b4-145">Close the page.</span></span>

