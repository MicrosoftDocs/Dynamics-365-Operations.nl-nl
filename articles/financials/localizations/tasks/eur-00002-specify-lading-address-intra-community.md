---
title: EUR-00002 Een vrachtadres opgeven voor een intracommunautaire transactie
description: Deze procedure laat zien hoe u een vrachtadres opgeeft voor een intracommunautaire handelstransactie.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4db22444bee1590770a47ca5946941b530ae85ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564411"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="b9368-103">EUR-00002 Een vrachtadres opgeven voor een intracommunautaire transactie</span><span class="sxs-lookup"><span data-stu-id="b9368-103">EUR-00002 Specifying a lading address for an intra-community transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9368-104">Deze procedure laat zien hoe u een vrachtadres opgeeft voor een intracommunautaire handelstransactie.</span><span class="sxs-lookup"><span data-stu-id="b9368-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="b9368-105">Bijvoorbeeld een Duits bedrijf bestelt artikelen bij een leverancier met een adres in Duitsland.</span><span class="sxs-lookup"><span data-stu-id="b9368-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="b9368-106">Deze leverancier heeft een magazijn in Italië en verzendt de artikelen vandaaruit.</span><span class="sxs-lookup"><span data-stu-id="b9368-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="b9368-107">Deze levering moet in Intrastat worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="b9368-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="b9368-108">Hetzelfde gedrag geldt voor klantretouren.</span><span class="sxs-lookup"><span data-stu-id="b9368-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="b9368-109">Deze procedure is van toepassing op alle Europese landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="b9368-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="b9368-110">De taak werd gemaakt met het demobedrijf DEMF met een primair adres in Duitsland.</span><span class="sxs-lookup"><span data-stu-id="b9368-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="b9368-111">Voordat u deze procedure kunt uitvoeren, moet u Intrastat-rapporten configureren.</span><span class="sxs-lookup"><span data-stu-id="b9368-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="b9368-112">Deze procedure is alleen bedoeld voor accountants.</span><span class="sxs-lookup"><span data-stu-id="b9368-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="b9368-113">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="b9368-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="b9368-114">Ga naar Leveranciers > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="b9368-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="b9368-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b9368-115">Click New.</span></span>
3. <span data-ttu-id="b9368-116">Typ of selecteer een waarde</span><span class="sxs-lookup"><span data-stu-id="b9368-116">Enter or select a value</span></span>
    * <span data-ttu-id="b9368-117">Selecteer bijvoorbeeld DE-001.</span><span class="sxs-lookup"><span data-stu-id="b9368-117">For example, select DE-001.</span></span> <span data-ttu-id="b9368-118">Deze leverancier heeft een Duits adres.</span><span class="sxs-lookup"><span data-stu-id="b9368-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="b9368-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9368-119">Click OK.</span></span>
5. <span data-ttu-id="b9368-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b9368-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b9368-121">Typ of selecteer een waarde D0001 in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="b9368-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="b9368-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b9368-122">Click Save.</span></span>
8. <span data-ttu-id="b9368-123">Klik in het actievenster op Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="b9368-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="b9368-124">Klik op Transportgegevens.</span><span class="sxs-lookup"><span data-stu-id="b9368-124">Click Transportation details.</span></span>
10. <span data-ttu-id="b9368-125">Typ in het veld Laaddatum en -tijd de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="b9368-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="b9368-126">Klik op Een nieuw adres toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b9368-126">Click Add address.</span></span>
12. <span data-ttu-id="b9368-127">Klik op Nieuw en maak een nieuw adres met als doel Vracht.</span><span class="sxs-lookup"><span data-stu-id="b9368-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="b9368-128">Typ Italiaans in het veld Naam of omschrijving.</span><span class="sxs-lookup"><span data-stu-id="b9368-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="b9368-129">Selecteer Vracht als de waarde.</span><span class="sxs-lookup"><span data-stu-id="b9368-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="b9368-130">Merk op dat het adresdoel Vracht moet zijn.</span><span class="sxs-lookup"><span data-stu-id="b9368-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="b9368-131">Typ of selecteer een waarde ITA in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="b9368-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="b9368-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b9368-132">Click Save.</span></span>
17. <span data-ttu-id="b9368-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9368-133">Close the page.</span></span>
18. <span data-ttu-id="b9368-134">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b9368-134">Click Save.</span></span>
    * <span data-ttu-id="b9368-135">Controleer of het vrachtadres juist is.</span><span class="sxs-lookup"><span data-stu-id="b9368-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="b9368-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9368-136">Close the page.</span></span>
20. <span data-ttu-id="b9368-137">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="b9368-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="b9368-138">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b9368-138">Click Confirm.</span></span>
22. <span data-ttu-id="b9368-139">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="b9368-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="b9368-140">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="b9368-140">Click Invoice.</span></span>
24. <span data-ttu-id="b9368-141">Typ een waarde in het veld Nummer.</span><span class="sxs-lookup"><span data-stu-id="b9368-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="b9368-142">Voer een datum in het veld Factuurdatum in.</span><span class="sxs-lookup"><span data-stu-id="b9368-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="b9368-143">Klik op Standaard vanaf: Hoeveelheid productontvangstbon om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="b9368-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="b9368-144">Selecteer Bestelde hoeveelheid in het veld Standaardhoeveelheid voor regels.</span><span class="sxs-lookup"><span data-stu-id="b9368-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="b9368-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9368-145">Click OK.</span></span>
29. <span data-ttu-id="b9368-146">Klik op Transportgegevens.</span><span class="sxs-lookup"><span data-stu-id="b9368-146">Click Transportation details.</span></span>
    * <span data-ttu-id="b9368-147">Controleer of de goederen uit Italië zijn verzonden.</span><span class="sxs-lookup"><span data-stu-id="b9368-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="b9368-148">Bewerk indien nodig de vrachtdetails.</span><span class="sxs-lookup"><span data-stu-id="b9368-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="b9368-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9368-149">Close the page.</span></span>
31. <span data-ttu-id="b9368-150">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="b9368-150">Click Post.</span></span>
32. <span data-ttu-id="b9368-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9368-151">Close the page.</span></span>
33. <span data-ttu-id="b9368-152">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b9368-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="b9368-153">Klik op Overbrengen.</span><span class="sxs-lookup"><span data-stu-id="b9368-153">Click Transfer.</span></span>
35. <span data-ttu-id="b9368-154">Selecteer Ja in het veld Leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="b9368-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="b9368-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9368-155">Click OK.</span></span>
37. <span data-ttu-id="b9368-156">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="b9368-156">Click the General tab.</span></span>
    * <span data-ttu-id="b9368-157">Zoek een nieuwe regel en controleer of de afzender de goederen uit Italië heeft verzonden.</span><span class="sxs-lookup"><span data-stu-id="b9368-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  

