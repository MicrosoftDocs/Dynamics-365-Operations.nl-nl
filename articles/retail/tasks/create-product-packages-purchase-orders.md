---
title: " Productpakketten voor inkooporders maken"
description: Deze procedure doorloopt het maken van een productpakket en het gebruik ervan in een inkooporder.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a7386a9be15f4eeef7aaab73cb320b71994eea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "360435"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="1d466-103"> Productpakketten voor inkooporders maken</span><span class="sxs-lookup"><span data-stu-id="1d466-103">Create product packages for purchase orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1d466-104">Deze procedure doorloopt het maken van een productpakket en het gebruik ervan in een inkooporder.</span><span class="sxs-lookup"><span data-stu-id="1d466-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="1d466-105">De inkooporder wordt gebruikt om een order te maken voor een vooraf gedefinieerde set producten.</span><span class="sxs-lookup"><span data-stu-id="1d466-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="1d466-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="1d466-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="1d466-107">Een productpakket maken</span><span class="sxs-lookup"><span data-stu-id="1d466-107">Create a product package</span></span>
1. <span data-ttu-id="1d466-108">Ga naar Kleinhandel en commerce > Voorraadbeheer > Aanvulling > Productpakketten.</span><span class="sxs-lookup"><span data-stu-id="1d466-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="1d466-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1d466-109">Click New.</span></span>
3. <span data-ttu-id="1d466-110">Typ een waarde in het veld Pakketnummer.</span><span class="sxs-lookup"><span data-stu-id="1d466-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="1d466-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="1d466-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1d466-112">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d466-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1d466-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d466-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="1d466-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1d466-114">Click Add.</span></span>
8. <span data-ttu-id="1d466-115">Typ '0160' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1d466-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="1d466-116">Klik in het veld Grootte op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d466-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="1d466-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d466-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="1d466-118">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="1d466-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="1d466-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1d466-119">Click Add.</span></span>
13. <span data-ttu-id="1d466-120">Typ '0160' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1d466-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="1d466-121">Klik in het veld Variantnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d466-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="1d466-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d466-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="1d466-123">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="1d466-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="1d466-124">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1d466-124">Click Add.</span></span>
18. <span data-ttu-id="1d466-125">Typ '0175' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1d466-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="1d466-126">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="1d466-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="1d466-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1d466-127">Click Save.</span></span>
21. <span data-ttu-id="1d466-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1d466-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="1d466-129">Pakket toevoegen aan inkooporder</span><span class="sxs-lookup"><span data-stu-id="1d466-129">Add package to purchase order</span></span>
1. <span data-ttu-id="1d466-130">Ga naar Leveranciers > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="1d466-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="1d466-131">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1d466-131">Click New.</span></span>
3. <span data-ttu-id="1d466-132">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d466-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1d466-133">Selecteer in de lijst dezelfde leverancier voor wie het productpakket eerder is gemaakt, als er een leverancier was geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1d466-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="1d466-134">Schakel de uitbreiding van de sectie Algemeen om.</span><span class="sxs-lookup"><span data-stu-id="1d466-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="1d466-135">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d466-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1d466-136">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d466-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1d466-137">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1d466-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="1d466-138">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1d466-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="1d466-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1d466-139">Click OK.</span></span>
11. <span data-ttu-id="1d466-140">Schakel de uitbreiding van de sectie Regeldetails om.</span><span class="sxs-lookup"><span data-stu-id="1d466-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="1d466-141">Klik op het tabblad Productpakketten.</span><span class="sxs-lookup"><span data-stu-id="1d466-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="1d466-142">Klik op Inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="1d466-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="1d466-143">Klik op Regels maken op basis van verpakking.</span><span class="sxs-lookup"><span data-stu-id="1d466-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="1d466-144">Zoek en selecteer in de lijst het productpakket dat in de vorige stap is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1d466-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="1d466-145">Voer een getal in het veld Hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="1d466-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="1d466-146">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="1d466-146">Click Create.</span></span>
18. <span data-ttu-id="1d466-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1d466-147">Click Save.</span></span>

