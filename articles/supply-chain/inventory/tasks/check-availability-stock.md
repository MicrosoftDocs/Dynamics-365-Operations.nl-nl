---
title: De beschikbaarheid van voorraad controleren
description: Deze procedure laat zien hoe u voorhanden en fysieke voorraad voor een specifiek artikelnummer kunt controleren.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2153117d9c921b43658edeade49a8403553e371
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238057"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="e48e1-103">De beschikbaarheid van voorraad controleren</span><span class="sxs-lookup"><span data-stu-id="e48e1-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e48e1-104">Deze procedure laat zien hoe u voorhanden en fysieke voorraad voor een specifiek artikelnummer kunt controleren.</span><span class="sxs-lookup"><span data-stu-id="e48e1-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="e48e1-105">Het geeft ook weer hoe u aanbodinformatie voor een artikel krijgt.</span><span class="sxs-lookup"><span data-stu-id="e48e1-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="e48e1-106">De fysieke voorhanden voorraad is de voorhanden voorraad die beschikbaar is, dat wil zeggen dat de voorraad is ingekocht, ontvangen en geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="e48e1-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="e48e1-107">De voorhanden voorraad bevat de beschikbare voorraad, maar ook de voorraad die is besteld en wordt verwacht, maar nog niet is ontvangen of geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="e48e1-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="e48e1-108">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e48e1-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="e48e1-109">Als u USMF gebruikt, kunt u de voorbeeldwaarden gebruiken die worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e48e1-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="e48e1-110">Deze taken worden meestal uitgevoerd door een magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="e48e1-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="e48e1-111">Voorhanden voorraad voor een artikel controleren</span><span class="sxs-lookup"><span data-stu-id="e48e1-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="e48e1-112">Ga naar **Navigatievenster > Modules > Voorraadbeheer > Query's en rapporten > Voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="e48e1-113">Selecteer de rij **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-113">Select the **Item number** row.</span></span> <span data-ttu-id="e48e1-114">Om de voorhanden voorraad op artikelnummer op te vragen, selecteert u de rij waar de tabel op **Voorhanden voorraad** is ingesteld en het veld op **Artikelnummer** is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e48e1-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="e48e1-115">Selecteer in het veld **Criteria** het artikel waarvoor u een query wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e48e1-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="e48e1-116">Als u het USMF-demobedrijf gebruikt, kunt u 'M9201' selecteren.</span><span class="sxs-lookup"><span data-stu-id="e48e1-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="e48e1-117">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-117">Click **OK**.</span></span>
5. <span data-ttu-id="e48e1-118">Klik in het **actievenster** op **Dimensies**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="e48e1-119">Met het tabblad **Dimensies** selecteert u hoeveel details u wilt zien over de voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="e48e1-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="e48e1-120">Als u gegevens met betrekking tot reserveringen nodig hebt, moet u alle voorraaddimensies voor de artikelen weergeven die geavanceerde magazijnbeheerprocessen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e48e1-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="e48e1-121">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-121">Click **OK**.</span></span>
7. <span data-ttu-id="e48e1-122">Klik in het **actievenster** op **Gerelateerde informatie**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="e48e1-123">Als deze optie niet wordt weergegeven, kunt u op de knop met weglatingstekens (...) klikken om extra actievensteropties te bekijken.</span><span class="sxs-lookup"><span data-stu-id="e48e1-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="e48e1-124">Klik op **Aanbodoverzicht**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-124">Click **Supply overview**.</span></span> <span data-ttu-id="e48e1-125">Het tabblad **Aanbodoverzicht** biedt aanbodinformatie voor een bepaald artikel, zoals de voorhanden hoeveelheid, doorlooptijd, en leveranciersgegevens.</span><span class="sxs-lookup"><span data-stu-id="e48e1-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="e48e1-126">Vouw de sectie **Voorhanden** uit.</span><span class="sxs-lookup"><span data-stu-id="e48e1-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="e48e1-127">Vouw de sectie **Leveranciers** uit.</span><span class="sxs-lookup"><span data-stu-id="e48e1-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="e48e1-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e48e1-128">Close the page.</span></span>
12. <span data-ttu-id="e48e1-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e48e1-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="e48e1-130">Fysieke voorhanden voorraad controleren</span><span class="sxs-lookup"><span data-stu-id="e48e1-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="e48e1-131">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Query's en rapporten > Fysieke voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="e48e1-132">Typ een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="e48e1-133">U kunt Locatie en Magazijn gebruiken om de lijst met artikelen te filteren.</span><span class="sxs-lookup"><span data-stu-id="e48e1-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="e48e1-134">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="e48e1-134">Refresh the page.</span></span>
4. <span data-ttu-id="e48e1-135">Klik in het **actievenster** op **Dimensies weergeven**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="e48e1-136">Met het tabblad Dimensies weergeven selecteert u hoeveel details u wilt zien over de voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="e48e1-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="e48e1-137">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-137">Click **OK**.</span></span>
6. <span data-ttu-id="e48e1-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e48e1-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="e48e1-139">De voorhanden voorraad per locatie controleren</span><span class="sxs-lookup"><span data-stu-id="e48e1-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="e48e1-140">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Query's en rapporten > Voorhanden voorraad per locatie**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="e48e1-141">Typ een waarde in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="e48e1-142">Als u het USMF-bedrijf van de demogegevens gebruikt, kunt u 51 gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e48e1-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="e48e1-143">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="e48e1-143">Refresh the page.</span></span>
4. <span data-ttu-id="e48e1-144">Klik op **Dimensies weergeven**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="e48e1-145">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e48e1-145">Click **OK**.</span></span>
6. <span data-ttu-id="e48e1-146">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e48e1-146">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]