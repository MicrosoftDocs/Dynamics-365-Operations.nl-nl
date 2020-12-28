---
title: Activa verplaatsen, vervangen en installeren
description: In dit onderwerp wordt uitgelegd hoe u activa verplaatst, vervangt en installeert in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425500"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="80572-103">Activa verplaatsen, vervangen en installeren</span><span class="sxs-lookup"><span data-stu-id="80572-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="80572-104">In dit onderwerp wordt uitgelegd hoe u activa verplaatst, vervangt en installeert in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="80572-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="80572-105">U kunt afzonderlijke activa maken die geen relaties hebben met andere activa, of u kunt een activastructuur maken die een bovenliggend activum (op het hoogste niveau) en gerelateerde onderliggende activa (subactiva) bevat.</span><span class="sxs-lookup"><span data-stu-id="80572-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="80572-106">In Activabeheer zijn er drie benaderingen voor het verplaatsen en wijzigen van de locatie van een activum:</span><span class="sxs-lookup"><span data-stu-id="80572-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="80572-107">**Verplaatsen**: een activum verplaatsen naar een andere activastructuur of naar een andere locatie in dezelfde activastructuur.</span><span class="sxs-lookup"><span data-stu-id="80572-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="80572-108">**Vervangen**: tijdelijk een activum verwijderen uit een activastructuur zodat het kan worden gerepareerd of gereviseerd, en vervolgens het gereviseerde activum weer aan de activastructuur toevoegen.</span><span class="sxs-lookup"><span data-stu-id="80572-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="80572-109">U kunt ook een gebruikt activum permanent vervangen door een nieuw activum.</span><span class="sxs-lookup"><span data-stu-id="80572-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="80572-110">**Installeren**: een bovenliggend activum en alle gerelateerde onderliggende activa op een functionele locatie installeren.</span><span class="sxs-lookup"><span data-stu-id="80572-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="80572-111">Het activum dat u verplaatst, vervangt of installeert, is mogelijk gerelateerd aan een andere functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="80572-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="80572-112">In dat geval kan het activum financiële dimensies van de functionele locatie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="80572-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="80572-113">Op de pagina **Functionele locatietypen** stelt u de verwerking van financiële dimensies in op functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="80572-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="80572-114">Activum verplaatsen</span><span class="sxs-lookup"><span data-stu-id="80572-114">Move asset</span></span>

<span data-ttu-id="80572-115">Gebruik de functie **Activum verplaatsen** om een activum te verplaatsen naar een andere activastructuur of naar een andere locatie in dezelfde activastructuur.</span><span class="sxs-lookup"><span data-stu-id="80572-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="80572-116">U kunt een activum ook uit een activastructuur verplaatsen, zodat het een zelfstandig activum wordt dat geen structuurrelaties heeft.</span><span class="sxs-lookup"><span data-stu-id="80572-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="80572-117">Gebruik deze functie niet als activa worden gerepareerd of tijdelijk worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="80572-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="80572-118">Gebruik in plaats daarvan de functie **Activum vervangen** die verderop in dit onderwerp wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="80572-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="80572-119">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="80572-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="80572-120">Selecteer in de lijst het activum dat u wilt verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="80572-120">In the list, select the asset to move.</span></span> <span data-ttu-id="80572-121">Als het activum onderliggende activa heeft, verplaatst u deze activa ook.</span><span class="sxs-lookup"><span data-stu-id="80572-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="80572-122">Selecteer **Activum verplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="80572-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="80572-123">Als u het activum wilt verplaatsen zodat het onderdeel wordt van een activastructuur, selecteert u het nieuwe bovenliggende activum in het veld **Bovenliggend activum**.</span><span class="sxs-lookup"><span data-stu-id="80572-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="80572-124">Als u een onderliggend element verplaatst en u daarvan een zelfstandig activum wilt maken dat geen structuurrelaties heeft, laat u het veld **Bovenliggend activum** leeg.</span><span class="sxs-lookup"><span data-stu-id="80572-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="80572-125">Standaard is het veld **Geldig vanaf** ingesteld op de huidige datum en tijd.</span><span class="sxs-lookup"><span data-stu-id="80572-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="80572-126">U kunt echter een andere datum en tijd selecteren waarop de activaverplaatsing geldig wordt.</span><span class="sxs-lookup"><span data-stu-id="80572-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="80572-127">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="80572-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="80572-128">Activum vervangen</span><span class="sxs-lookup"><span data-stu-id="80572-128">Replace asset</span></span>

<span data-ttu-id="80572-129">Gebruik de functie **Activum vervangen** in verband met reparaties, revisie of permanente vervanging van een versleten activum door een nieuw activum.</span><span class="sxs-lookup"><span data-stu-id="80572-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="80572-130">Deze functie wordt gebruikt om onderliggende activa in een activastructuur te vervangen.</span><span class="sxs-lookup"><span data-stu-id="80572-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="80572-131">Voor bovenliggende activa (dat zijn activa die momenteel geen bovenliggend activum hebben), wordt deze vervanging uitgevoerd op een functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="80572-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="80572-132">Zie [Activa installeren op functionele locaties](../functional-locations/install-objects-on-functional-locations.md) voor meer informatie over het vervangen van bovenliggende activa op een functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="80572-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="80572-133">Als een reparatiewerkplaats is gerelateerd aan uw productieafdeling, kunt u functionele locaties zoals **reparatie**, **uitval** en **opslag** maken om de reparatie en vervanging van activa te verwerken.</span><span class="sxs-lookup"><span data-stu-id="80572-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="80572-134">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="80572-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="80572-135">Selecteer in de lijst het onderliggende activum dat wordt vervangen.</span><span class="sxs-lookup"><span data-stu-id="80572-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="80572-136">Als het activum onderliggende activa heeft, vervangt u deze activa ook.</span><span class="sxs-lookup"><span data-stu-id="80572-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="80572-137">Selecteer **Activum vervangen**.</span><span class="sxs-lookup"><span data-stu-id="80572-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="80572-138">Het veld **Structuurwijziging** bevat de laatste datum en tijd waarop het geselecteerde activum en de bijbehorende onderliggende activa zijn verplaatst in de activastructuur.</span><span class="sxs-lookup"><span data-stu-id="80572-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="80572-139">Selecteer in de sectie **Geselecteerd activum** in het veld **Doel functionele locatie** de functionele locatie waarnaar u het activum wilt verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="80572-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="80572-140">Selecteer bijvoorbeeld de locatie van de **reparatie** of **uitval**.</span><span class="sxs-lookup"><span data-stu-id="80572-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="80572-141">In de sectie **Bovenliggend activum** bevat het veld **Geldig vanaf** de laatste datum en tijd waarop het bovenliggende activum en de bijbehorende onderliggende activa zijn geïnstalleerd of verplaatst op de huidige functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="80572-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="80572-142">Selecteer in de sectie **Nieuw activum** in het veld **Activum** het activum dat u wilt invoegen als tijdelijke of permanente vervanging voor het geselecteerde activum.</span><span class="sxs-lookup"><span data-stu-id="80572-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="80572-143">Dit activum kan zich momenteel bevinden op een andere functionele locatie, zoals **opslag**.</span><span class="sxs-lookup"><span data-stu-id="80572-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="80572-144">In de sectie **Geldig vanaf** is het veld **Geldig vanaf** standaard ingesteld op de huidige datum en tijd.</span><span class="sxs-lookup"><span data-stu-id="80572-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="80572-145">U kunt echter een andere datum en tijd selecteren waarop de activavervanging geldig wordt.</span><span class="sxs-lookup"><span data-stu-id="80572-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="80572-146">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="80572-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="80572-147">Activum installeren</span><span class="sxs-lookup"><span data-stu-id="80572-147">Install asset</span></span>

<span data-ttu-id="80572-148">Gebruik de functie **Activum installeren** om een activastructuur op een functionele locatie te installeren.</span><span class="sxs-lookup"><span data-stu-id="80572-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="80572-149">Selecteer altijd een bovenliggend activum.</span><span class="sxs-lookup"><span data-stu-id="80572-149">Always select a parent asset.</span></span> <span data-ttu-id="80572-150">Het bovenliggende activum en de bijbehorende onderliggende activa worden verplaatst naar de geselecteerde functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="80572-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="80572-151">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="80572-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="80572-152">Selecteer in de lijst het bovenliggende activum dat u wilt installeren op een andere functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="80572-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="80572-153">Selecteer **Activum installeren**.</span><span class="sxs-lookup"><span data-stu-id="80572-153">Select **Install asset**.</span></span>

    <span data-ttu-id="80572-154">De sectie **Kenmerken** geeft de activumkenmerken weer die zijn ingesteld voor het bovenliggende activum.</span><span class="sxs-lookup"><span data-stu-id="80572-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="80572-155">Selecteer de nieuwe locatie in het veld **Functionele locatie**.</span><span class="sxs-lookup"><span data-stu-id="80572-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="80572-156">Standaard is het veld **Geldig vanaf** ingesteld op de huidige datum en tijd.</span><span class="sxs-lookup"><span data-stu-id="80572-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="80572-157">U kunt echter een andere datum en tijd selecteren waarop de installatie in de activastructuur geldig wordt.</span><span class="sxs-lookup"><span data-stu-id="80572-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="80572-158">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="80572-158">Select **OK**.</span></span>
