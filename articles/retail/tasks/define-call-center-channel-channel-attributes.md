--- 
title: "Callcenterkanalen maken en kanaalkenmerken definiëren"
description: "Deze procedure doorloopt het maken van een nieuw detailhandelkanaal en het definiëren van kanaalkenmerken."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 7ef094535214ecf4c65f95c36a93455446d7e388
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="f5a23-103">Callcenterkanalen maken en kanaalkenmerken definiëren</span><span class="sxs-lookup"><span data-stu-id="f5a23-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f5a23-104">Deze procedure doorloopt het maken van een nieuw detailhandelkanaal en het definiëren van kanaalkenmerken.</span><span class="sxs-lookup"><span data-stu-id="f5a23-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="f5a23-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="f5a23-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f5a23-106">Deze procedure is bedoeld voor de detailhandel-IT-rol.</span><span class="sxs-lookup"><span data-stu-id="f5a23-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="f5a23-107">Nieuwe winkel maken</span><span class="sxs-lookup"><span data-stu-id="f5a23-107">Create new store</span></span>
1. <span data-ttu-id="f5a23-108">Ga naar Alle werkruimten > Kanaalimplementatie.</span><span class="sxs-lookup"><span data-stu-id="f5a23-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="f5a23-109">Klik op Nieuw kanaal.</span><span class="sxs-lookup"><span data-stu-id="f5a23-109">Click New channel.</span></span>
3. <span data-ttu-id="f5a23-110">Klik op Winkel.</span><span class="sxs-lookup"><span data-stu-id="f5a23-110">Click Store.</span></span>
4. <span data-ttu-id="f5a23-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f5a23-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f5a23-112">Typ een waarde in het veld Winkelnummer.</span><span class="sxs-lookup"><span data-stu-id="f5a23-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="f5a23-113">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f5a23-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f5a23-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f5a23-116">Selecteer een optie in het veld Winkeltijdzone.</span><span class="sxs-lookup"><span data-stu-id="f5a23-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="f5a23-117">Klik in het veld Afzetkanaalprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f5a23-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f5a23-119">Klik in het veld Taal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f5a23-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f5a23-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="f5a23-122">Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="f5a23-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="f5a23-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f5a23-125">Klik in het veld Adresboek klant op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f5a23-126">Selecteer het adresboek dat wordt gebruikt om klanten te koppelen aan deze winkel.</span><span class="sxs-lookup"><span data-stu-id="f5a23-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="f5a23-127">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="f5a23-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="f5a23-129">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="f5a23-129">Click Select.</span></span>
22. <span data-ttu-id="f5a23-130">Klik in het veld Adresboek van werknemer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f5a23-131">Selecteer het adresboek dat wordt gebruikt om kassiers te koppelen aan dit kanaal.</span><span class="sxs-lookup"><span data-stu-id="f5a23-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="f5a23-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="f5a23-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="f5a23-134">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="f5a23-134">Click Select.</span></span>
26. <span data-ttu-id="f5a23-135">Klik in het veld Standaardklant op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="f5a23-136">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="f5a23-137">Vouw de sectie Schermindeling uit of samen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="f5a23-138">Klik in het veld Schermindelings-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f5a23-139">Selecteer de standaard POS-schermindeling voor deze winkel.</span><span class="sxs-lookup"><span data-stu-id="f5a23-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="f5a23-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="f5a23-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="f5a23-142">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="f5a23-143">Klik op Afzetkanaalkenmerken.</span><span class="sxs-lookup"><span data-stu-id="f5a23-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="f5a23-144">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f5a23-144">Click New.</span></span>
35. <span data-ttu-id="f5a23-145">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="f5a23-146">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="f5a23-147">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="f5a23-148">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f5a23-148">Click Save.</span></span>
39. <span data-ttu-id="f5a23-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f5a23-149">Close the page.</span></span>
40. <span data-ttu-id="f5a23-150">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="f5a23-151">Klik op Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="f5a23-151">Click Payment methods.</span></span>
42. <span data-ttu-id="f5a23-152">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f5a23-152">Click New.</span></span>
43. <span data-ttu-id="f5a23-153">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="f5a23-154">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="f5a23-155">Vouw de sectie Boeking uit of samen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="f5a23-156">Geef in het veld Rekeningnummer de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="f5a23-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="f5a23-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f5a23-157">Click Save.</span></span>
48. <span data-ttu-id="f5a23-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f5a23-158">Close the page.</span></span>
49. <span data-ttu-id="f5a23-159">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="f5a23-160">Klik op Contantdeclaratie.</span><span class="sxs-lookup"><span data-stu-id="f5a23-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="f5a23-161">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f5a23-161">Click New.</span></span>
52. <span data-ttu-id="f5a23-162">Typ een getal in het veld Bedrag in transactievaluta.</span><span class="sxs-lookup"><span data-stu-id="f5a23-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="f5a23-163">Klik in het veld Valuta op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="f5a23-164">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="f5a23-165">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="f5a23-166">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f5a23-166">Click Save.</span></span>
57. <span data-ttu-id="f5a23-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f5a23-167">Close the page.</span></span>
58. <span data-ttu-id="f5a23-168">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="f5a23-169">Klik op Toewijzing van winkellocatorgroep.</span><span class="sxs-lookup"><span data-stu-id="f5a23-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="f5a23-170">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f5a23-170">Click New.</span></span>
61. <span data-ttu-id="f5a23-171">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="f5a23-172">Klik in het veld Locatorgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f5a23-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="f5a23-173">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f5a23-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="f5a23-174">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5a23-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="f5a23-175">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f5a23-175">Click Save.</span></span>
66. <span data-ttu-id="f5a23-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f5a23-176">Close the page.</span></span>


