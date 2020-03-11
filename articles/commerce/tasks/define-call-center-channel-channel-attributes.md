---
title: Callcenterkanalen maken en kanaalkenmerken definiëren
description: Deze procedure doorloopt het maken van een nieuw kanaal en het definiëren van kanaalkenmerken.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62075c01ad7e2a4c393e9658fa67f8b536654aec
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057149"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="64958-103">Callcenterkanalen maken en kanaalkenmerken definiëren</span><span class="sxs-lookup"><span data-stu-id="64958-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="64958-104">Deze procedure doorloopt het maken van een nieuw Commerce-kanaal en het definiëren van kanaalkenmerken.</span><span class="sxs-lookup"><span data-stu-id="64958-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="64958-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="64958-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="64958-106">Deze procedure is bedoeld voor de Commerce-IT-rol.</span><span class="sxs-lookup"><span data-stu-id="64958-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="64958-107">Nieuwe winkel maken</span><span class="sxs-lookup"><span data-stu-id="64958-107">Create new store</span></span>
1. <span data-ttu-id="64958-108">Ga naar Alle werkruimten > Kanaalimplementatie.</span><span class="sxs-lookup"><span data-stu-id="64958-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="64958-109">Klik op Nieuw kanaal.</span><span class="sxs-lookup"><span data-stu-id="64958-109">Click New channel.</span></span>
3. <span data-ttu-id="64958-110">Klik op Winkel.</span><span class="sxs-lookup"><span data-stu-id="64958-110">Click Store.</span></span>
4. <span data-ttu-id="64958-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="64958-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="64958-112">Typ een waarde in het veld Winkelnummer.</span><span class="sxs-lookup"><span data-stu-id="64958-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="64958-113">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="64958-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="64958-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="64958-116">Selecteer een optie in het veld Winkeltijdzone.</span><span class="sxs-lookup"><span data-stu-id="64958-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="64958-117">Klik in het veld Afzetkanaalprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="64958-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="64958-119">Klik in het veld Taal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="64958-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="64958-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="64958-122">Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="64958-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="64958-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="64958-125">Klik in het veld Adresboek klant op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="64958-126">Selecteer het adresboek dat wordt gebruikt om klanten te koppelen aan deze winkel.</span><span class="sxs-lookup"><span data-stu-id="64958-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="64958-127">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="64958-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="64958-129">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="64958-129">Click Select.</span></span>
22. <span data-ttu-id="64958-130">Klik in het veld Adresboek van werknemer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="64958-131">Selecteer het adresboek dat wordt gebruikt om kassiers te koppelen aan dit kanaal.</span><span class="sxs-lookup"><span data-stu-id="64958-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="64958-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="64958-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="64958-134">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="64958-134">Click Select.</span></span>
26. <span data-ttu-id="64958-135">Klik in het veld Standaardklant op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="64958-136">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="64958-137">Vouw de sectie Schermindeling uit of samen.</span><span class="sxs-lookup"><span data-stu-id="64958-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="64958-138">Klik in het veld Schermindelings-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="64958-139">Selecteer de standaard POS-schermindeling voor deze winkel.</span><span class="sxs-lookup"><span data-stu-id="64958-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="64958-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="64958-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="64958-142">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="64958-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="64958-143">Klik op Afzetkanaalkenmerken.</span><span class="sxs-lookup"><span data-stu-id="64958-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="64958-144">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="64958-144">Click New.</span></span>
35. <span data-ttu-id="64958-145">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="64958-146">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="64958-147">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="64958-148">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="64958-148">Click Save.</span></span>
39. <span data-ttu-id="64958-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="64958-149">Close the page.</span></span>
40. <span data-ttu-id="64958-150">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="64958-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="64958-151">Klik op Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="64958-151">Click Payment methods.</span></span>
42. <span data-ttu-id="64958-152">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="64958-152">Click New.</span></span>
43. <span data-ttu-id="64958-153">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="64958-154">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="64958-155">Vouw de sectie Boeking uit of samen.</span><span class="sxs-lookup"><span data-stu-id="64958-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="64958-156">Geef in het veld Rekeningnummer de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="64958-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="64958-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="64958-157">Click Save.</span></span>
48. <span data-ttu-id="64958-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="64958-158">Close the page.</span></span>
49. <span data-ttu-id="64958-159">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="64958-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="64958-160">Klik op Contantdeclaratie.</span><span class="sxs-lookup"><span data-stu-id="64958-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="64958-161">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="64958-161">Click New.</span></span>
52. <span data-ttu-id="64958-162">Typ een getal in het veld Bedrag in transactievaluta.</span><span class="sxs-lookup"><span data-stu-id="64958-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="64958-163">Klik in het veld Valuta op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="64958-164">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="64958-165">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="64958-166">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="64958-166">Click Save.</span></span>
57. <span data-ttu-id="64958-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="64958-167">Close the page.</span></span>
58. <span data-ttu-id="64958-168">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="64958-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="64958-169">Klik op Toewijzing van winkellocatorgroep.</span><span class="sxs-lookup"><span data-stu-id="64958-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="64958-170">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="64958-170">Click New.</span></span>
61. <span data-ttu-id="64958-171">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="64958-172">Klik in het veld Locatorgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="64958-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="64958-173">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="64958-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="64958-174">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="64958-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="64958-175">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="64958-175">Click Save.</span></span>
66. <span data-ttu-id="64958-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="64958-176">Close the page.</span></span>

