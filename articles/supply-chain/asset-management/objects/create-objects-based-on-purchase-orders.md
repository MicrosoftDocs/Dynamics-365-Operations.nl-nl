---
title: Activa maken op basis van inkooporders
description: In dit onderwerp wordt uitgelegd hoe u een lijst met activumartikelen maakt die kunnen worden gebruikt als basis voor het maken van activa voor onderhoudstaken in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83419fa5c6b6aee0b321c526565c3518deaf4bd0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016979"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="0acb7-103">Activa maken op basis van inkooporders</span><span class="sxs-lookup"><span data-stu-id="0acb7-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0acb7-104">In dit onderwerp wordt uitgelegd hoe u een lijst met activumartikelen maakt die kunnen worden gebruikt als basis voor het maken van activa voor onderhoudstaken in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="0acb7-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="0acb7-105">Op basis van de activumartikelen kunt u een lijst weergeven van de inkooporderregels die voor die artikelen zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0acb7-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="0acb7-106">Het doel van deze functionaliteit is om op basis van een inkooporder eenvoudig een activum te maken in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="0acb7-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="0acb7-107">Eerst stelt u vanuit een inkooporder in **Activumartikelen** de artikelen in die moeten worden gebruikt voor het maken van activa.</span><span class="sxs-lookup"><span data-stu-id="0acb7-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="0acb7-108">Nadat u een inkooporderregel hebt gemaakt, maakt u de activa in **Activa in behandeling**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="0acb7-109">Het is mogelijk om te bepalen in welk stadium van de inkooporder het activum moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0acb7-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="0acb7-110">Activumtypen selecteren</span><span class="sxs-lookup"><span data-stu-id="0acb7-110">Select asset items</span></span>

1. <span data-ttu-id="0acb7-111">Klik op **Activabeheer** > **Instellen** > **Activa** > **Artikelen**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="0acb7-112">Klik op **Nieuw** om een nieuwe activumartikel te maken.</span><span class="sxs-lookup"><span data-stu-id="0acb7-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="0acb7-113">Selecteer het artikel in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="0acb7-114">Wanneer u dit veld verlaat, wordt de artikelnaam automatisch ingevoegd in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="0acb7-115">Selecteer op het sneltabblad **Algemeen** een activumtype voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="0acb7-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="0acb7-116">Selecteer de fabrikant en het model van het activumartikel.</span><span class="sxs-lookup"><span data-stu-id="0acb7-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="0acb7-117">Sla het artikel op.</span><span class="sxs-lookup"><span data-stu-id="0acb7-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="0acb7-118">Activa maken van activa in behandeling</span><span class="sxs-lookup"><span data-stu-id="0acb7-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="0acb7-119">Klik op **Activabeheer** > **Algemeen** > **Activa** > **Activa in behandeling**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="0acb7-120">U ziet een bijgewerkte lijst van de inkooporders op basis van de artikelen die zijn geselecteerd in **Activumartikelen**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="0acb7-121">U kunt de status van inkooporders filteren om te selecteren in welke levenscyclusstatus het activum moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0acb7-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="0acb7-122">U wilt bijvoorbeeld alleen activa maken wanneer een productontvangstbon voor een inkooporder is geboekt.</span><span class="sxs-lookup"><span data-stu-id="0acb7-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="0acb7-123">Selecteer de koppeling **Referentienummer** op een inkooporderregel om gedetailleerde informatie over het artikel weer te geven.</span><span class="sxs-lookup"><span data-stu-id="0acb7-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="0acb7-124">Als u wilt bewerken welke dimensies worden weergegeven op het sneltabblad **Voorraaddimensies**, klikt u op de knop **Dimensies weergeven** en maakt u uw selecties.</span><span class="sxs-lookup"><span data-stu-id="0acb7-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="0acb7-125">Als u een activum wilt maken op basis van een inkooporderregel, schakelt u het selectievakje in de kolom **Markeren** voor die regel in op de lijstpagina en klikt u op **Activa maken**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="0acb7-126">Er wordt een bericht weergegeven met informatie over de activum-id.</span><span class="sxs-lookup"><span data-stu-id="0acb7-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="0acb7-127">Selecteer het activum in de lijst **Alle activa** en klik op **Bewerken** als u meer informatie aan het activum wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0acb7-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="0acb7-128">Als u in **Activa in behandeling** een regel wilt verwijderen omdat u geen activum wilt maken, schakelt u het selectievakje in de kolom **Markeren** voor die regel in en klikt u op **Activa in behandeling verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="0acb7-129">Er wordt een bericht weergegeven met informatie over de activum-id.</span><span class="sxs-lookup"><span data-stu-id="0acb7-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="0acb7-130">U verwijdert de inkooporder of verkooporder niet, maar alleen de record op basis waarvan u een activum had kunnen maken in **Activabeheer**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="0acb7-131">Alle productdimensies (grootte, kleur, configuratie, enzovoort) worden automatisch overgebracht naar de kenmerken van het activum.</span><span class="sxs-lookup"><span data-stu-id="0acb7-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="0acb7-132">Traceringsdimensies (serienummer) worden rechtstreeks in het activum opgeslagen wanneer het activum wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0acb7-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="0acb7-133">Activa in behandeling zoeken</span><span class="sxs-lookup"><span data-stu-id="0acb7-133">Find pending assets</span></span>

<span data-ttu-id="0acb7-134">U kunt de functie **Activa in behandeling tellen** uitvoeren om te controleren op activa in behandeling.</span><span class="sxs-lookup"><span data-stu-id="0acb7-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="0acb7-135">Deze functie kan bijvoorbeeld worden gebruikt als u een melding wilt ontvangen telkens wanneer een activum in behandeling gereed is om als een activum te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0acb7-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="0acb7-136">Klik op **Activabeheer** > **Periodiek** > **Activa** > **Activa in behandeling tellen**.</span><span class="sxs-lookup"><span data-stu-id="0acb7-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="0acb7-137">Klik op **OK** om de taak uit te voeren en de lijst in **Activa in behandeling** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="0acb7-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="0acb7-138">U kunt deze taak zo instellen dat deze als een batchtaak wordt uitgevoerd, bijvoorbeeld eenmaal per dag.</span><span class="sxs-lookup"><span data-stu-id="0acb7-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="0acb7-139">**Waarschuwing:** als gegevens op een inkooporder worden gewijzigd *nadat* u een activum hebt gemaakt op basis van het betreffende artikel, worden deze wijzigingen niet doorgevoerd in het activum.</span><span class="sxs-lookup"><span data-stu-id="0acb7-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
