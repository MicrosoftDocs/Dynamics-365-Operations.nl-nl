---
title: Verkoopovereenkomsten afhandelen
description: Deze procedure toont hoe u een verkoopovereenkomst vervult door er verkooporders aan te koppelen.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3a35c7140b886f931df48e583b1582201b6547
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425245"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="37758-103">Verkoopovereenkomsten afhandelen</span><span class="sxs-lookup"><span data-stu-id="37758-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37758-104">Deze procedure toont hoe u een verkoopovereenkomst vervult door er verkooporders aan te koppelen.</span><span class="sxs-lookup"><span data-stu-id="37758-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="37758-105">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="37758-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="37758-106">Voordat u deze guide start, moet u ervoor zorgen u een effectieve verkoopovereenkomst van het type 'Toezegging productwaarde' hebt.</span><span class="sxs-lookup"><span data-stu-id="37758-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="37758-107">Anders kunt u de taakbegeleider met de naam 'Verkoopovereenkomsten maken' uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="37758-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="37758-108">Een verkooporder uit de overeenkomst vrijgeven</span><span class="sxs-lookup"><span data-stu-id="37758-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="37758-109">Ga naar Verkoop en marketing > Verkoopovereenkomsten > Verkoopovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="37758-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="37758-110">Open in de lijst de overeenkomst waarvoor u de order wilt vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="37758-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="37758-111">Klik in het actievenster op Verkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="37758-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="37758-112">Klik op Vrijgaveorder.</span><span class="sxs-lookup"><span data-stu-id="37758-112">Click Release order.</span></span>
    * <span data-ttu-id="37758-113">Zoals de tekst bovenaan de pagina Vrijgaveorder maken aangeeft, verschillen de details die vereist zijn voor de verkooporderregels, afhankelijk van of de overeenkomst is gebaseerd op hoeveelheid of waarde.</span><span class="sxs-lookup"><span data-stu-id="37758-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="37758-114">De overeenkomst in deze guide is van het type 'Toezegging productwaarde'.</span><span class="sxs-lookup"><span data-stu-id="37758-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="37758-115">Daarom is de sectie Regels van deze pagina leeg.</span><span class="sxs-lookup"><span data-stu-id="37758-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="37758-116">Als de toezegging was gebaseerd op hoeveelheid, zou de regelinformatie vanuit de overeenkomst worden gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="37758-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="37758-117">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="37758-117">Click Create.</span></span>
    * <span data-ttu-id="37758-118">Het bericht meldt u dat er nu een verkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="37758-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="37758-119">Omdat de order geen regels bevat, moet u orderregeldetails toevoegen om het vrijgaveproces te voltooien.</span><span class="sxs-lookup"><span data-stu-id="37758-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="37758-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37758-120">Close the page.</span></span>
7. <span data-ttu-id="37758-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37758-121">Close the page.</span></span>
8. <span data-ttu-id="37758-122">Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="37758-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="37758-123">Zoek in de lijst en open de order die werd gemaakt als resultaat van de ordervrijgave in de vorige taak.</span><span class="sxs-lookup"><span data-stu-id="37758-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="37758-124">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="37758-124">Click Add line.</span></span>
11. <span data-ttu-id="37758-125">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="37758-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="37758-126">Typ of selecteer in het veld Artikelnummer het artikel dat is opgegeven in de gekoppelde verkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="37758-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="37758-127">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="37758-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="37758-128">Zorg ervoor dat u een hoeveelheid invoert die het Nettobedrag onder de waarde van de gekoppelde verkoopovereenkomst brengt.</span><span class="sxs-lookup"><span data-stu-id="37758-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="37758-129">Omdat de verkooporder aan de overeenkomst is gekoppeld, wordt het overeengekomen kortingspercentage op de orderregel toegepast.</span><span class="sxs-lookup"><span data-stu-id="37758-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="37758-130">Klik op Regel bijwerken.</span><span class="sxs-lookup"><span data-stu-id="37758-130">Click Update line.</span></span>
15. <span data-ttu-id="37758-131">Klik op Gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="37758-131">Click Attached.</span></span>
    * <span data-ttu-id="37758-132">De pagina Bijgevoegde overeenkomst toont de id en voorwaarden van de overeenkomst waarvan de regel worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="37758-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="37758-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37758-133">Close the page.</span></span>
17. <span data-ttu-id="37758-134">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="37758-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="37758-135">Klik op Gekoppelde verkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="37758-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="37758-136">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="37758-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="37758-137">Klik op het tabblad Vervulling.</span><span class="sxs-lookup"><span data-stu-id="37758-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="37758-138">Het tabblad Vervulling geeft een overzicht van alle verkooporderregels die aan deze toezegging zijn gekoppeld en hun vervullingsstatus, het bedrag dat of de hoeveelheid die nog niet is vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="37758-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="37758-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37758-139">Close the page.</span></span>
22. <span data-ttu-id="37758-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37758-140">Close the page.</span></span>
23. <span data-ttu-id="37758-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37758-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="37758-142">Een verkoopovereenkomst toepassen in het orderproces</span><span class="sxs-lookup"><span data-stu-id="37758-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="37758-143">Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="37758-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="37758-144">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="37758-144">Click New.</span></span>
3. <span data-ttu-id="37758-145">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="37758-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="37758-146">Zoek in de lijst en selecteer de klant die op de verkoopovereenkomst wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="37758-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="37758-147">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="37758-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="37758-148">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="37758-148">Expand the General section.</span></span>
7. <span data-ttu-id="37758-149">Klik in het veld Verkoopovereenkomst-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="37758-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="37758-150">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="37758-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="37758-151">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="37758-151">Click Yes.</span></span>
10. <span data-ttu-id="37758-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="37758-152">Click OK.</span></span>
11. <span data-ttu-id="37758-153">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="37758-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="37758-154">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="37758-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="37758-155">Typ of selecteer in het veld Artikelnummer het artikel dat is opgegeven in de gekoppelde verkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="37758-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="37758-156">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="37758-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="37758-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="37758-157">Click Save.</span></span>
16. <span data-ttu-id="37758-158">Klik in het actievenster op Verzamelen en inpakken.</span><span class="sxs-lookup"><span data-stu-id="37758-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="37758-159">Klik op Pakbon boeken.</span><span class="sxs-lookup"><span data-stu-id="37758-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="37758-160">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="37758-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="37758-161">Selecteer Ja in het veld Boeking.</span><span class="sxs-lookup"><span data-stu-id="37758-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="37758-162">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="37758-162">Click OK.</span></span>
21. <span data-ttu-id="37758-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="37758-163">Click OK.</span></span>
22. <span data-ttu-id="37758-164">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="37758-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="37758-165">Klik op Gekoppelde verkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="37758-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="37758-166">Klik op het tabblad Vervulling.</span><span class="sxs-lookup"><span data-stu-id="37758-166">Click the Fulfillment tab.</span></span>

