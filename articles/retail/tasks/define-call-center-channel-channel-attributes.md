--- 
title: " Kanaal en kanaalkenmerken definiëren voor callcenters"
description: "Deze procedure doorloopt het maken van een nieuw detailhandelkanaal en het definiëren van kanaalkenmerken."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: b2741885418de5c2a2c9ed97e5c6146c824857df
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---
# <a name="define-call-center-channel-and-channel-attributes"></a><span data-ttu-id="b5e12-103"> Kanaal en kanaalkenmerken definiëren voor callcenters</span><span class="sxs-lookup"><span data-stu-id="b5e12-103">Define call center channel and channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b5e12-104">Deze procedure doorloopt het maken van een nieuw detailhandelkanaal en het definiëren van kanaalkenmerken.</span><span class="sxs-lookup"><span data-stu-id="b5e12-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="b5e12-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="b5e12-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="b5e12-106">Deze procedure is bedoeld voor de detailhandel-IT-rol.</span><span class="sxs-lookup"><span data-stu-id="b5e12-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="b5e12-107">Nieuwe winkel maken</span><span class="sxs-lookup"><span data-stu-id="b5e12-107">Create new store</span></span>
1. <span data-ttu-id="b5e12-108">Ga naar Alle werkruimten > Kanaalimplementatie.</span><span class="sxs-lookup"><span data-stu-id="b5e12-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="b5e12-109">Klik op Nieuw kanaal.</span><span class="sxs-lookup"><span data-stu-id="b5e12-109">Click New channel.</span></span>
3. <span data-ttu-id="b5e12-110">Klik op Winkel.</span><span class="sxs-lookup"><span data-stu-id="b5e12-110">Click Store.</span></span>
4. <span data-ttu-id="b5e12-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b5e12-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b5e12-112">Typ een waarde in het veld Winkelnummer.</span><span class="sxs-lookup"><span data-stu-id="b5e12-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="b5e12-113">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b5e12-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="b5e12-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b5e12-116">Selecteer een optie in het veld Winkeltijdzone.</span><span class="sxs-lookup"><span data-stu-id="b5e12-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="b5e12-117">Klik in het veld Afzetkanaalprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b5e12-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b5e12-119">Klik in het veld Taal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="b5e12-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b5e12-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="b5e12-122">Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="b5e12-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b5e12-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b5e12-125">Klik in het veld Adresboek klant op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b5e12-126">Selecteer het adresboek dat wordt gebruikt om klanten te koppelen aan deze winkel.</span><span class="sxs-lookup"><span data-stu-id="b5e12-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="b5e12-127">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="b5e12-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="b5e12-129">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="b5e12-129">Click Select.</span></span>
22. <span data-ttu-id="b5e12-130">Klik in het veld Adresboek van werknemer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b5e12-131">Selecteer het adresboek dat wordt gebruikt om kassiers te koppelen aan dit kanaal.</span><span class="sxs-lookup"><span data-stu-id="b5e12-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="b5e12-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="b5e12-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="b5e12-134">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="b5e12-134">Click Select.</span></span>
26. <span data-ttu-id="b5e12-135">Klik in het veld Standaardklant op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="b5e12-136">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="b5e12-137">Vouw de sectie Schermindeling uit of samen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="b5e12-138">Klik in het veld Schermindelings-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b5e12-139">Selecteer de standaard POS-schermindeling voor deze winkel.</span><span class="sxs-lookup"><span data-stu-id="b5e12-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="b5e12-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="b5e12-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="b5e12-142">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="b5e12-143">Klik op Afzetkanaalkenmerken.</span><span class="sxs-lookup"><span data-stu-id="b5e12-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="b5e12-144">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b5e12-144">Click New.</span></span>
35. <span data-ttu-id="b5e12-145">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="b5e12-146">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="b5e12-147">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="b5e12-148">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b5e12-148">Click Save.</span></span>
39. <span data-ttu-id="b5e12-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5e12-149">Close the page.</span></span>
40. <span data-ttu-id="b5e12-150">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="b5e12-151">Klik op Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="b5e12-151">Click Payment methods.</span></span>
42. <span data-ttu-id="b5e12-152">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b5e12-152">Click New.</span></span>
43. <span data-ttu-id="b5e12-153">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="b5e12-154">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="b5e12-155">Vouw de sectie Boeking uit of samen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="b5e12-156">Geef in het veld Rekeningnummer de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="b5e12-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="b5e12-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b5e12-157">Click Save.</span></span>
48. <span data-ttu-id="b5e12-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5e12-158">Close the page.</span></span>
49. <span data-ttu-id="b5e12-159">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="b5e12-160">Klik op Contantdeclaratie.</span><span class="sxs-lookup"><span data-stu-id="b5e12-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="b5e12-161">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b5e12-161">Click New.</span></span>
52. <span data-ttu-id="b5e12-162">Typ een getal in het veld Bedrag in transactievaluta.</span><span class="sxs-lookup"><span data-stu-id="b5e12-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="b5e12-163">Klik in het veld Valuta op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="b5e12-164">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="b5e12-165">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="b5e12-166">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b5e12-166">Click Save.</span></span>
57. <span data-ttu-id="b5e12-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5e12-167">Close the page.</span></span>
58. <span data-ttu-id="b5e12-168">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="b5e12-169">Klik op Toewijzing van winkellocatorgroep.</span><span class="sxs-lookup"><span data-stu-id="b5e12-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="b5e12-170">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b5e12-170">Click New.</span></span>
61. <span data-ttu-id="b5e12-171">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="b5e12-172">Klik in het veld Locatorgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b5e12-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="b5e12-173">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5e12-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="b5e12-174">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5e12-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="b5e12-175">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b5e12-175">Click Save.</span></span>
66. <span data-ttu-id="b5e12-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5e12-176">Close the page.</span></span>


