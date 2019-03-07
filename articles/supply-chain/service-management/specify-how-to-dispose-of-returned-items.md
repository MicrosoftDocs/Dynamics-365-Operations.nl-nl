---
title: Opgeven op welke wijze retourartikelen moeten worden afgestoten
description: Geef op op welke wijze retourartikelen moeten worden afgestoten.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6fcdfec083aeb9c58d63f6e03542758e4d07e4d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "325061"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="3aa90-103">Opgeven op welke wijze retourartikelen moeten worden afgestoten</span><span class="sxs-lookup"><span data-stu-id="3aa90-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3aa90-104">Wanneer u een retourorder verwerkt, moet u een retourredencode opgeven om aan te geven waarom het product is geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="3aa90-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="3aa90-105">U moet ook een beschikkingscode en een beschikkingsactie opgeven om te bepalen wat er moet gebeuren met het geretourneerde product.</span><span class="sxs-lookup"><span data-stu-id="3aa90-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="3aa90-106">U kunt een beschikkingscode toepassen wanneer u de retourorder maakt, de artikelontvangst registreert of de pakbon voor een artikelontvangst bijwerkt en een quarantaineorder beëindigt.</span><span class="sxs-lookup"><span data-stu-id="3aa90-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="3aa90-107">U kunt alle beschikkingscodes maken die u nodig hebt ter ondersteuning van de bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="3aa90-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="3aa90-108">De volgende tabel bevat een set codes die meestal wordt gebruikt voor het toewijzen van een retourartikelbeschikking.</span><span class="sxs-lookup"><span data-stu-id="3aa90-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3aa90-109">Beschikkingstype</span><span class="sxs-lookup"><span data-stu-id="3aa90-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="3aa90-110">Algemene code</span><span class="sxs-lookup"><span data-stu-id="3aa90-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="3aa90-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="3aa90-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-112">Afstoting</span><span class="sxs-lookup"><span data-stu-id="3aa90-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="3aa90-113">SC</span><span class="sxs-lookup"><span data-stu-id="3aa90-113">SC</span></span></p></td>
<td><p><span data-ttu-id="3aa90-114">Uitval/vernietiging</span><span class="sxs-lookup"><span data-stu-id="3aa90-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-115">Afstoting</span><span class="sxs-lookup"><span data-stu-id="3aa90-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="3aa90-116">DC</span><span class="sxs-lookup"><span data-stu-id="3aa90-116">DC</span></span></p></td>
<td><p><span data-ttu-id="3aa90-117">Donaties aan liefdadigheidsinstelling</span><span class="sxs-lookup"><span data-stu-id="3aa90-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-118">Afstoting</span><span class="sxs-lookup"><span data-stu-id="3aa90-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="3aa90-119">TD</span><span class="sxs-lookup"><span data-stu-id="3aa90-119">TD</span></span></p></td>
<td><p><span data-ttu-id="3aa90-120">Afstoting door derden</span><span class="sxs-lookup"><span data-stu-id="3aa90-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-121">Afstoting</span><span class="sxs-lookup"><span data-stu-id="3aa90-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="3aa90-122">SL</span><span class="sxs-lookup"><span data-stu-id="3aa90-122">SL</span></span></p></td>
<td><p><span data-ttu-id="3aa90-123">Hergebruik</span><span class="sxs-lookup"><span data-stu-id="3aa90-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-124">Afstoting</span><span class="sxs-lookup"><span data-stu-id="3aa90-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="3aa90-125">TS</span><span class="sxs-lookup"><span data-stu-id="3aa90-125">TS</span></span></p></td>
<td><p><span data-ttu-id="3aa90-126">Verkoop aan derden (secundaire markten)</span><span class="sxs-lookup"><span data-stu-id="3aa90-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-127">Repareren/aanpassen</span><span class="sxs-lookup"><span data-stu-id="3aa90-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="3aa90-128">RW</span><span class="sxs-lookup"><span data-stu-id="3aa90-128">RW</span></span></p></td>
<td><p><span data-ttu-id="3aa90-129">Opnieuw maken</span><span class="sxs-lookup"><span data-stu-id="3aa90-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-130">Repareren/aanpassen</span><span class="sxs-lookup"><span data-stu-id="3aa90-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="3aa90-131">RF</span><span class="sxs-lookup"><span data-stu-id="3aa90-131">RF</span></span></p></td>
<td><p><span data-ttu-id="3aa90-132">Opnieuw produceren/opknappen</span><span class="sxs-lookup"><span data-stu-id="3aa90-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-133">Repareren/aanpassen</span><span class="sxs-lookup"><span data-stu-id="3aa90-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="3aa90-134">MD</span><span class="sxs-lookup"><span data-stu-id="3aa90-134">MD</span></span></p></td>
<td><p><span data-ttu-id="3aa90-135">Aanpassen</span><span class="sxs-lookup"><span data-stu-id="3aa90-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-136">Repareren/aanpassen</span><span class="sxs-lookup"><span data-stu-id="3aa90-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="3aa90-137">RP</span><span class="sxs-lookup"><span data-stu-id="3aa90-137">RP</span></span></p></td>
<td><p><span data-ttu-id="3aa90-138">Repareren</span><span class="sxs-lookup"><span data-stu-id="3aa90-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-139">Repareren/aanpassen</span><span class="sxs-lookup"><span data-stu-id="3aa90-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="3aa90-140">RV</span><span class="sxs-lookup"><span data-stu-id="3aa90-140">RV</span></span></p></td>
<td><p><span data-ttu-id="3aa90-141">Retour naar leverancier</span><span class="sxs-lookup"><span data-stu-id="3aa90-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-142">Overige</span><span class="sxs-lookup"><span data-stu-id="3aa90-142">Other</span></span></p></td>
<td><p><span data-ttu-id="3aa90-143">AI</span><span class="sxs-lookup"><span data-stu-id="3aa90-143">AI</span></span></p></td>
<td><p><span data-ttu-id="3aa90-144">In huidige staat gebruiken</span><span class="sxs-lookup"><span data-stu-id="3aa90-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-145">Overige</span><span class="sxs-lookup"><span data-stu-id="3aa90-145">Other</span></span></p></td>
<td><p><span data-ttu-id="3aa90-146">RS</span><span class="sxs-lookup"><span data-stu-id="3aa90-146">RS</span></span></p></td>
<td><p><span data-ttu-id="3aa90-147">Herverkoop</span><span class="sxs-lookup"><span data-stu-id="3aa90-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-148">Overige</span><span class="sxs-lookup"><span data-stu-id="3aa90-148">Other</span></span></p></td>
<td><p><span data-ttu-id="3aa90-149">EX</span><span class="sxs-lookup"><span data-stu-id="3aa90-149">EX</span></span></p></td>
<td><p><span data-ttu-id="3aa90-150">Uitwisselen</span><span class="sxs-lookup"><span data-stu-id="3aa90-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-151">Overige</span><span class="sxs-lookup"><span data-stu-id="3aa90-151">Other</span></span></p></td>
<td><p><span data-ttu-id="3aa90-152">MS</span><span class="sxs-lookup"><span data-stu-id="3aa90-152">MS</span></span></p></td>
<td><p><span data-ttu-id="3aa90-153">Overige</span><span class="sxs-lookup"><span data-stu-id="3aa90-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3aa90-154">Voor elke beschikkingscode die u definieert, moet u een beschikkingsactie selecteren.</span><span class="sxs-lookup"><span data-stu-id="3aa90-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="3aa90-155">De beschikkingsactie definieert de fysieke en financiële implicaties van beschikkingscodes.</span><span class="sxs-lookup"><span data-stu-id="3aa90-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="3aa90-156">Bijvoorbeeld, bepaalt de beschikkingsactie de fysieke behandeling van het geretourneerde artikel, het financiële effect van het geretourneerde artikel, en of een vervangingsartikel aan de klant moet worden verstuurd.</span><span class="sxs-lookup"><span data-stu-id="3aa90-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="3aa90-157">U kunt een onbeperkt aantal beschikkingscodes volgens uw bedrijfsbehoeften definiëren, maar zijn er slechts zes voorafgedefinieerde beschikkingsacties waaruit u kunt kiezen.</span><span class="sxs-lookup"><span data-stu-id="3aa90-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="3aa90-158">De volgende tabel bevat de beschikkingsacties en hun definities.</span><span class="sxs-lookup"><span data-stu-id="3aa90-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3aa90-159">Beschikkingsactie</span><span class="sxs-lookup"><span data-stu-id="3aa90-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="3aa90-160">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="3aa90-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-161"><strong>Credit</strong></span><span class="sxs-lookup"><span data-stu-id="3aa90-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="3aa90-162">Retourneer het artikel naar de voorraad en crediteer de klant.</span><span class="sxs-lookup"><span data-stu-id="3aa90-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-163"><strong>Alleen credit</strong></span><span class="sxs-lookup"><span data-stu-id="3aa90-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="3aa90-164">Crediteer de klant zonder te vereisen of te verwachten dat het artikel wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="3aa90-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-165"><strong>Uitval</strong></span><span class="sxs-lookup"><span data-stu-id="3aa90-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="3aa90-166">Schrap het artikel en crediteer de klant.</span><span class="sxs-lookup"><span data-stu-id="3aa90-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-167"><strong>Vervangen en crediteren</strong></span><span class="sxs-lookup"><span data-stu-id="3aa90-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="3aa90-168">Retourneer het artikel naar de voorraad, maak een vervangingsorder en crediteer de klant.</span><span class="sxs-lookup"><span data-stu-id="3aa90-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa90-169"><strong>Vervangen en uitvallen</strong></span><span class="sxs-lookup"><span data-stu-id="3aa90-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="3aa90-170">Schrap het artikel, maak een vervangingsorder en crediteer de klant.</span><span class="sxs-lookup"><span data-stu-id="3aa90-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa90-171"><strong>Retour naar klant</strong></span><span class="sxs-lookup"><span data-stu-id="3aa90-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="3aa90-172">Weiger het artikel en retourneer het aan de klant.</span><span class="sxs-lookup"><span data-stu-id="3aa90-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="3aa90-173">Een beschikkingscode selecteren voor een quarantaineorder</span><span class="sxs-lookup"><span data-stu-id="3aa90-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="3aa90-174">Klik op **Voorraadbeheer** \> **Periodiek** \> **Kwaliteitsbeheer** \> **Quarantaineorders**.</span><span class="sxs-lookup"><span data-stu-id="3aa90-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="3aa90-175">Voor een bestaande quarantaineorder selecteert u een actie in het veld **Beschikkingscode** op het tabblad **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="3aa90-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="3aa90-176">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3aa90-176">See also</span></span>

<span data-ttu-id="3aa90-177">[Quarantaineorder (formulier)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="3aa90-177">[Quarantine order (form)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="3aa90-178">[Beschikkingscodes (formulier)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="3aa90-178">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

  


