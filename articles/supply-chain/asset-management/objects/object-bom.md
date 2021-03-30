---
title: Activumstuklijsten
description: Dit onderwerp beschrijft activumstuklijsten in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e5d6d6245f27534d176ac03ca762aff91afb0ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253177"
---
# <a name="asset-boms"></a><span data-ttu-id="b3622-103">Activumstuklijsten</span><span class="sxs-lookup"><span data-stu-id="b3622-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b3622-104">Dit onderwerp beschrijft activumstuklijsten in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="b3622-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="b3622-105">Op de pagina **Activumstuklijst** wordt een lijst weergegeven met alle artikelen (reserveonderdelen en andere artikelen) die gedurende de hele levensduur op een activum worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3622-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="b3622-106">Wanneer u een nieuw activum maakt, moet u overwegen om een activumstuklijst in te stellen als onderdeel van de instellingsprocedure.</span><span class="sxs-lookup"><span data-stu-id="b3622-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="b3622-107">Op deze manier kunt u de artikelhistorie voor het activum bijhouden vanaf de aanmaakdatum.</span><span class="sxs-lookup"><span data-stu-id="b3622-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="b3622-108">Nadat u een onderhoudstaak hebt voltooid en het artikelverbruik is geregistreerd op een werkorder, kunt u het verbruik van reserveonderdelen en andere artikelen bijhouden die voor het activum zijn gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3622-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="b3622-109">Met deze functionaliteit kunt u een volledig artikelverbruikrecord bijhouden voor al uw activa.</span><span class="sxs-lookup"><span data-stu-id="b3622-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="b3622-110">U kunt de record bijvoorbeeld gebruiken om te controleren of een specifiek reserveonderdeel vaak wordt vervangen of om de reserveonderdelen of andere artikelen bij te houden die momenteel voor een activum worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3622-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="b3622-111">Op een werkorder kan artikelverbruik zowel reserveonderdelen als andere extra artikelen bevatten, zoals smeermiddelen, bouten en pakkingen.</span><span class="sxs-lookup"><span data-stu-id="b3622-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="b3622-112">Een activumstuklijst kan automatisch worden bijgewerkt op basis van de instellingen in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="b3622-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="b3622-113">Als de levenscyclusstatus van een werkorder is gemaakt voor het afhandelen van afgeronde of voltooide werkorders en als de optie **Activumstuklijst bijwerken** voor de levenscyclusstatus van de werkorder is ingesteld op **Ja** op de pagina **Levenscyclusstatussen van werkorders**, worden alle artikelen die op de werkorder zijn gebruikt, automatisch bijgewerkt op de pagina **Activumstuklijst** wanneer de werkorder wordt bijgewerkt naar die levenscyclusstatus.</span><span class="sxs-lookup"><span data-stu-id="b3622-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="b3622-114">U kunt een activumstuklijst ook handmatig bijwerken door nieuwe artikelregels te maken op de pagina **Activumstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b3622-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="b3622-115">Op de pagina **Activumstuklijst** kunt u de historie van reserveonderdelen bijhouden voor activa nadat het artikelverbruik is geregistreerd op een werkorder.</span><span class="sxs-lookup"><span data-stu-id="b3622-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="b3622-116">Als u deze functionaliteit wilt gebruiken, moet u de artikelgroepen selecteren die moeten worden gebruikt voor de registratie van reserveonderdelen op de pagina **Artikelgroepen reserveonderdelen**.</span><span class="sxs-lookup"><span data-stu-id="b3622-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="b3622-117">Als u de functionaliteit activumstuklijst wilt gebruiken, moet u eerst de vereiste artikelgroepen voor reserveonderdelen instellen.</span><span class="sxs-lookup"><span data-stu-id="b3622-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="b3622-118">Als u vervolgens wilt dat de activumstuklijst automatisch wordt bijgewerkt wanneer een werkorder is voltooid, kunt u een levenscyclusstatus van een werkorder instellen om die update af te handelen.</span><span class="sxs-lookup"><span data-stu-id="b3622-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="b3622-119">Artikelengroepen voor reserveonderdelen instellen</span><span class="sxs-lookup"><span data-stu-id="b3622-119">Set up spare parts item groups</span></span>

<span data-ttu-id="b3622-120">Het instellen van de historie van reserveonderdelen is gebaseerd op artikelgroepen die zijn gemaakt in de module **Voorraad- en magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="b3622-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="b3622-121">In Activabeheer stelt u artikelgroepen in, zodat u de historie van reserveonderdelen voor de artikelen in de geselecteerde artikelgroepen kunt bijhouden.</span><span class="sxs-lookup"><span data-stu-id="b3622-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="b3622-122">Selecteer **Activabeheer** \> **Instellingen** \> **Activum** \> **Artikelgroepen reserveonderdelen**.</span><span class="sxs-lookup"><span data-stu-id="b3622-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="b3622-123">Selecteer **Nieuw** om een artikelgroep in te stellen.</span><span class="sxs-lookup"><span data-stu-id="b3622-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="b3622-124">Selecteer de groep in het veld **Artikelgroep**.</span><span class="sxs-lookup"><span data-stu-id="b3622-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="b3622-125">De naam van de groep wordt automatisch in het veld **Naam** ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="b3622-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="b3622-126">Activumstuklijsten weergeven en bijwerken</span><span class="sxs-lookup"><span data-stu-id="b3622-126">View and update asset BOMs</span></span>

<span data-ttu-id="b3622-127">Nadat u artikelverbruik op een werkorder hebt geboekt, kunt u het geregistreerde artikelverbruik weergeven op de pagina **Activumstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b3622-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="b3622-128">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="b3622-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="b3622-129">Selecteer het activum in de lijst en selecteer **Activumstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b3622-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b3622-130">Als u alle artikelverbruikregistraties voor alle activa wilt weergeven, selecteert u **Activabeheer** \> **Query's** \> **Activa** \> **Activumstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b3622-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="b3622-131">Selecteer **Activumstuklijst bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="b3622-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="b3622-132">U kunt desgewenst activa, activatypen en resources aan de update toevoegen met **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="b3622-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="b3622-133">Selecteer **OK** om de update te starten.</span><span class="sxs-lookup"><span data-stu-id="b3622-133">Select **OK** to start the update.</span></span> <span data-ttu-id="b3622-134">U kunt de functie Update ook instellen als batchtaak.</span><span class="sxs-lookup"><span data-stu-id="b3622-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="b3622-135">Als u meer informatie wilt zien die betrekking heeft op de artikelen, kunt u voorraaddimensies toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b3622-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="b3622-136">Selecteer **Voorraad** \> **Weergave van dimensies** en schakel vervolgens de selectievakjes in voor de dimensies die u wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="b3622-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="b3622-137">Als u deze instellingen voor alle activa op de pagina **Activumstuklijst** wilt behouden , stelt u de optie **Instellingen opslaan** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b3622-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="b3622-138">Voor een overzicht van waar in Activabeheer het artikel op de geselecteerde regel wordt gebruikt in relatie tot activa, standaardwaarden voor taaktypen, reserveonderdelen en werkorders, selecteert u **Artikel waar gebruikt**.</span><span class="sxs-lookup"><span data-stu-id="b3622-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="b3622-139">Als u alleen actieve artikelregels wilt zien, selecteert u **Weergeven** \> **Huidige**.</span><span class="sxs-lookup"><span data-stu-id="b3622-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="b3622-140">Als u alle artikelregels wilt zien, inclusief regels waarvan de vervaldatum vóór de huidige datum valt, selecteert u **Weergeven** \> **Alles**.</span><span class="sxs-lookup"><span data-stu-id="b3622-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="b3622-141">Wanneer u een werkorder hebt voltooid en bepaalde artikelen of reserveonderdelen die samenhangen met het gerelateerde activum, zijn verlopen of zijn vervangen door andere artikelen of reserveonderdelen, kunt u de activumstuklijst het beste ook bijwerken.</span><span class="sxs-lookup"><span data-stu-id="b3622-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="b3622-142">Een nieuwe artikelregel maken in een activumstuklijst</span><span class="sxs-lookup"><span data-stu-id="b3622-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="b3622-143">U kunt handmatig artikelregels voor activa maken.</span><span class="sxs-lookup"><span data-stu-id="b3622-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="b3622-144">Selecteer **Nieuw** op de pagina **Activumstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b3622-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="b3622-145">Selecteer in het veld **Activum** het activum waarvoor u een artikelregel wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b3622-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="b3622-146">Voer in het veld **Regelnummer** een volgnummer voor de regel in.</span><span class="sxs-lookup"><span data-stu-id="b3622-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="b3622-147">Selecteer een begindatum voor het artikel in het veld **Geldig vanaf**.</span><span class="sxs-lookup"><span data-stu-id="b3622-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="b3622-148">Als het artikel vervalt, geeft u een einddatum op in het veld **Vervaldatum**.</span><span class="sxs-lookup"><span data-stu-id="b3622-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="b3622-149">Selecteer het artikel in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="b3622-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="b3622-150">De naam wordt automatisch in het veld **Productnaam** ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="b3622-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="b3622-151">Voer in het veld **Hoeveelheid** de gebruikte hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="b3622-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="b3622-152">Het veld **Eenheid** wordt automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b3622-152">The **Unit** field is automatically updated.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]