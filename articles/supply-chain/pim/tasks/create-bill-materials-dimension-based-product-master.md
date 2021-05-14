---
title: Een stuklijst maken voor een op dimensies gebaseerd productmodel
description: Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920700"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="df6c7-103">Een stuklijst maken voor een op dimensies gebaseerd productmodel</span><span class="sxs-lookup"><span data-stu-id="df6c7-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df6c7-104">Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="df6c7-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="df6c7-105">Met de eerste 4 registraties zijn gegevens ingesteld die nodig zijn om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="df6c7-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="df6c7-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="df6c7-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="df6c7-107">Deze taak wordt doorgaans afgehandeld door de productontwerper.</span><span class="sxs-lookup"><span data-stu-id="df6c7-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="df6c7-108">Het product selecteren</span><span class="sxs-lookup"><span data-stu-id="df6c7-108">Select the product</span></span>

1. <span data-ttu-id="df6c7-109">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="df6c7-110">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df6c7-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="df6c7-111">Zoek het vrijgegeven productmodel met op dimensies gebaseerde configuratietechnologie die u in de eerste taakbegeleider in deze reeks hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="df6c7-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="df6c7-112">Selecteer in het actievenster de optie **Technicus**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="df6c7-113">Selecteer **Stuklijstversies**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="df6c7-114">Een nieuwe stuklijst en stuklijstversie maken</span><span class="sxs-lookup"><span data-stu-id="df6c7-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="df6c7-115">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-115">Select **New**.</span></span>
1. <span data-ttu-id="df6c7-116">Selecteer **Stuklijst en stuklijstversie**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="df6c7-117">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="df6c7-118">Een vestiging instellen</span><span class="sxs-lookup"><span data-stu-id="df6c7-118">Setting a site</span></span>  
    * <span data-ttu-id="df6c7-119">In deze procedure wordt geen specifieke vestiging voor de stuklijst ingesteld.</span><span class="sxs-lookup"><span data-stu-id="df6c7-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="df6c7-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-120">Select **OK**.</span></span>
1. <span data-ttu-id="df6c7-121">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-121">Select **New**.</span></span>
    * <span data-ttu-id="df6c7-122">In deze procedure worden vier regels aan de stuklijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="df6c7-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="df6c7-123">Twee regels staan voor kabelopties en twee regels staan voor behuizingsopties.</span><span class="sxs-lookup"><span data-stu-id="df6c7-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="df6c7-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df6c7-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df6c7-125">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="df6c7-126">Selecteer artikelnummer A0001, HDMI 6' kabels.</span><span class="sxs-lookup"><span data-stu-id="df6c7-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="df6c7-127">Typ of selecteer een waarde in het veld **Configuratiegroep**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df6c7-128">Selecteer de kabelconfiguratiegroep die is gemaakt in guide 4 in deze reeks.</span><span class="sxs-lookup"><span data-stu-id="df6c7-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="df6c7-129">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-129">Select **New**.</span></span>
    * <span data-ttu-id="df6c7-130">Selecteer artikelnummer A0002, HDMI 12' kabels.</span><span class="sxs-lookup"><span data-stu-id="df6c7-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="df6c7-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df6c7-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df6c7-132">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="df6c7-133">Typ of selecteer een waarde in het veld **Configuratiegroep**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df6c7-134">Selecteer de kabelconfiguratiegroep opnieuw.</span><span class="sxs-lookup"><span data-stu-id="df6c7-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="df6c7-135">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-135">Select **New**.</span></span>
1. <span data-ttu-id="df6c7-136">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df6c7-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df6c7-137">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="df6c7-138">Selecteer artikelnummer D0002 behuizing</span><span class="sxs-lookup"><span data-stu-id="df6c7-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="df6c7-139">Typ of selecteer een waarde in het veld **Configuratiegroep**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df6c7-140">Selecteer de behuizingsconfiguratiegroep voor deze stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="df6c7-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="df6c7-141">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-141">Select **New**.</span></span>
1. <span data-ttu-id="df6c7-142">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df6c7-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df6c7-143">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="df6c7-144">Selecteer artikelnummer M0007 standaardbehuizing als de laatste stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="df6c7-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="df6c7-145">Typ of selecteer een waarde in het veld **Configuratiegroep**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df6c7-146">Selecteer de behuizingsconfiguratiegroep voor de laatste stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="df6c7-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="df6c7-147">Goedkeuren en activeren</span><span class="sxs-lookup"><span data-stu-id="df6c7-147">Approve and activate</span></span>

1. <span data-ttu-id="df6c7-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="df6c7-148">Close the page.</span></span>
1. <span data-ttu-id="df6c7-149">Selecteer **Goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-149">Select **Approve**.</span></span>
1. <span data-ttu-id="df6c7-150">Typ of selecteer een waarde in het veld **Goedgekeurd door**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="df6c7-151">Selecteer *Ja* in het veld **Wilt u ook de stuklijst goedkeuren?**</span><span class="sxs-lookup"><span data-stu-id="df6c7-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="df6c7-152">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-152">Select **OK**.</span></span>
1. <span data-ttu-id="df6c7-153">Selecteer **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="df6c7-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]