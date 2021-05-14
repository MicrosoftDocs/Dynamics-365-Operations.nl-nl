---
title: Een nomenclatuur met productnummers maken voor geconfigureerde productvarianten
description: In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921006"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="5b366-103">Een nomenclatuur met productnummers maken voor geconfigureerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="5b366-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b366-104">In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt.</span><span class="sxs-lookup"><span data-stu-id="5b366-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="5b366-105">In deze procedure ziet u ook hoe u een configuratienomenclatuur samenstelt voor een component van een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="5b366-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="5b366-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="5b366-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5b366-107">De nieuwe productnummernomenclatuur is toegewezen aan het productmodel D0004.</span><span class="sxs-lookup"><span data-stu-id="5b366-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="5b366-108">Deze taak wordt meestal uitgevoerd door een productontwerper.</span><span class="sxs-lookup"><span data-stu-id="5b366-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="5b366-109">Een productvariantnummer-nomenclatuur maken</span><span class="sxs-lookup"><span data-stu-id="5b366-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="5b366-110">Ga naar **Productgegevensbeheer \> Instellingen \> Productnomenclatuur**.</span><span class="sxs-lookup"><span data-stu-id="5b366-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="5b366-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5b366-111">Select **New**.</span></span>
1. <span data-ttu-id="5b366-112">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="5b366-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="5b366-113">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="5b366-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="5b366-114">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-114">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-115">Selecteer **Nummer van productmodel**.</span><span class="sxs-lookup"><span data-stu-id="5b366-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="5b366-116">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-116">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-117">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="5b366-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="5b366-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-119">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="5b366-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5b366-120">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-120">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-121">Selecteer **Configuratie**.</span><span class="sxs-lookup"><span data-stu-id="5b366-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="5b366-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5b366-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="5b366-123">De productnummernomenclatuur toewijzen aan een productmodel</span><span class="sxs-lookup"><span data-stu-id="5b366-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="5b366-124">Ga naar **Productgegevensbeheer \> Producten \> Productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="5b366-125">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="5b366-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5b366-126">Filter bijvoorbeeld het veld **Productnummer** op de waarde 'D'.</span><span class="sxs-lookup"><span data-stu-id="5b366-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="5b366-127">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5b366-128">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="5b366-128">Select **Edit**.</span></span>
1. <span data-ttu-id="5b366-129">Selecteer *Ja* in het veld **Nomenclatuur gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="5b366-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="5b366-130">Typ of selecteer een waarde in het veld **Productvariantnummer-nomenclatuur**.</span><span class="sxs-lookup"><span data-stu-id="5b366-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="5b366-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5b366-131">Close the page.</span></span>
1. <span data-ttu-id="5b366-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5b366-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="5b366-133">Een nomenclatuur maken voor een productconfiguratiemodelcomponent</span><span class="sxs-lookup"><span data-stu-id="5b366-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="5b366-134">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="5b366-135">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5b366-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="5b366-136">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5b366-137">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="5b366-137">Select **Edit**.</span></span>
1. <span data-ttu-id="5b366-138">Selecteer *Ja* in het veld **Configuratienomenclatuur gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="5b366-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="5b366-139">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-139">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-140">Selecteer **Kenmerkwaarde**.</span><span class="sxs-lookup"><span data-stu-id="5b366-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5b366-141">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-142">Typ of selecteer een waarde in het veld **Kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="5b366-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5b366-143">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-143">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-144">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="5b366-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="5b366-145">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-146">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="5b366-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5b366-147">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-147">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-148">Selecteer **Kenmerkwaarde**.</span><span class="sxs-lookup"><span data-stu-id="5b366-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5b366-149">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-150">Typ of selecteer een waarde in het veld **Kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="5b366-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5b366-151">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-151">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-152">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="5b366-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="5b366-153">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-154">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="5b366-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5b366-155">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-155">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-156">Selecteer **Kenmerkwaarde**.</span><span class="sxs-lookup"><span data-stu-id="5b366-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5b366-157">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-158">Typ of selecteer een waarde in het veld **Kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="5b366-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5b366-159">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-159">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-160">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="5b366-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="5b366-161">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-162">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="5b366-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5b366-163">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-163">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-164">Selecteer **Kenmerkwaarde**.</span><span class="sxs-lookup"><span data-stu-id="5b366-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5b366-165">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-166">Typ of selecteer een waarde in het veld **Kenmerk**.</span><span class="sxs-lookup"><span data-stu-id="5b366-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5b366-167">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-167">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-168">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="5b366-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="5b366-169">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-170">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="5b366-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5b366-171">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5b366-171">Select **Add**.</span></span>
1. <span data-ttu-id="5b366-172">Selecteer **Nummerreekswaarde**.</span><span class="sxs-lookup"><span data-stu-id="5b366-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="5b366-173">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5b366-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5b366-174">Typ of selecteer een waarde in het veld **Nummerreeks**.</span><span class="sxs-lookup"><span data-stu-id="5b366-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="5b366-175">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5b366-175">Close the page.</span></span>
1. <span data-ttu-id="5b366-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5b366-176">Close the page.</span></span>
1. <span data-ttu-id="5b366-177">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5b366-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]