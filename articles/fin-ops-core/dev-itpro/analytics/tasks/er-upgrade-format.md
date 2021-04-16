---
title: ER Uw indeling upgraden door een nieuwe basisversie van die indeling aan te nemen
description: In dit onderwerp wordt uitgelegd hoe u een indelingsconfiguratie voor Elektronische rapportage (ER) onderhoudt.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05f8562bcab50a303b58174d177c6058f9417294
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744934"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="9b5ba-103">ER Uw indeling upgraden door een nieuwe basisversie van die indeling aan te nemen</span><span class="sxs-lookup"><span data-stu-id="9b5ba-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b5ba-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan onderhouden voor elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="9b5ba-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="9b5ba-105">In deze procedure wordt uitgelegd hoe een aangepaste versie kan worden gemaakt op basis van een indeling die is ontvangen van een configuratieprovider (CP).</span><span class="sxs-lookup"><span data-stu-id="9b5ba-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="9b5ba-106">Ook wordt beschreven hoe u een nieuwe basisversie van die indeling kunt aannemen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="9b5ba-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedures "Een configuratieprovider maken en als actief markeren" en "Gemaakte indeling gebruiken om elektronische documenten voor betalingen te genereren".</span><span class="sxs-lookup"><span data-stu-id="9b5ba-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="9b5ba-108">Deze stappen kunnen in het GBSI-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="9b5ba-109">Indelingsconfiguratie voor aanpassing selecteren</span><span class="sxs-lookup"><span data-stu-id="9b5ba-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="9b5ba-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="9b5ba-111">In dit voorbeeld doet voorbeeldbedrijf Litware, Inc. (https://www.litware.com) dienst als een configuratieprovider die indelingsconfiguraties voor elektronische betalingen ondersteunt voor een bepaald land.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="9b5ba-112">Het voorbeeldbedrijf Proseware, Inc. (http://www.proseware.com) fungeert als een gebruiker van de indelingsconfiguratie die is verstrekt door Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="9b5ba-113">Proseware, Inc. gebruikt indelingen in bepaalde regio's van dat land.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="9b5ba-114">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9b5ba-115">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-115">Click Show filters.</span></span>
4. <span data-ttu-id="9b5ba-116">Pas de volgende filter toe: voer in het veld 'Naam' de waarde "BACS (UK fictief)" in met de filteroperator 'begint met'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="9b5ba-117">De geselecteerde indelingsconfiguratie BACS (UK fictief) is eigendom van de provider Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="9b5ba-118">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-118">Click Show filters.</span></span>
6. <span data-ttu-id="9b5ba-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9b5ba-120">De versie van de indeling met de status Voltooid wordt door Proseware, Inc. gebruikt om aan te passen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="9b5ba-121">Een nieuwe configuratie voor uw aangepaste indeling van elektronisch documenten maken</span><span class="sxs-lookup"><span data-stu-id="9b5ba-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="9b5ba-122">Proseware, Inc. heeft versie 1.1 van de configuratie (UK fictief) ontvangen die de oorspronkelijke indeling bevat om elektronische betalingsdocumenten van Litware, Inc. te genereren in overeenstemming met hun serviceabonnement.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="9b5ba-123">Proseware, Inc. wil deze als standaard gaan gebruiken voor hun land, maar er is enige aanpassing vereist om specifieke regionale vereisten te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="9b5ba-124">Proseware, Inc. wil ook de mogelijkheid behouden om een aangepaste indeling als een nieuwe versie ervan te upgraden (met wijzigingen om nieuwe landspecifieke vereisten te ondersteunen) van Litware, Inc. en ze willen deze upgrade tegen zo laag mogelijke kosten uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="9b5ba-125">Hiervoor moet Proseware, Inc. een configuratie maken met behulp van de configuratie Litware, Inc. BACS (UK fictief) als basis.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="9b5ba-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-126">Close the page.</span></span>
2. <span data-ttu-id="9b5ba-127">Selecteer Proseware, Inc. en maak hiervan een actieve leverancier.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="9b5ba-128">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-128">Click Set active.</span></span>
4. <span data-ttu-id="9b5ba-129">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9b5ba-130">Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9b5ba-131">Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="9b5ba-132">Selecteer de configuratie BACS (UK fictief) van Litware, Inc. Proseware, Inc. gebruikt versie 1.1 als basis voor de aangepaste versie.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="9b5ba-133">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="9b5ba-134">Zo kunt u een nieuwe configuratie voor een aangepaste betalingsindeling maken.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="9b5ba-135">Voer in het veld Nieuw "Afleiden van naam: BACS (UK fictief) Litware, inc." in.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="9b5ba-136">Selecteer de optie Afleiden om het gebruik van BACS (UK fictief) te bevestigen als basis voor het maken van de aangepaste versie.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="9b5ba-137">Typ "BACS (UK fictief en aangepast)" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="9b5ba-138">Typ in het veld Beschrijving: "BACS voor leveranciersbetalingen (UK fictief en aangepast)".</span><span class="sxs-lookup"><span data-stu-id="9b5ba-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="9b5ba-139">De actieve configuratieprovider (Proseware, Inc.) wordt hier automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="9b5ba-140">Deze provider kan deze configuratie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="9b5ba-141">Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="9b5ba-142">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="9b5ba-143">Uw indeling voor elektronisch documenten aanpassen</span><span class="sxs-lookup"><span data-stu-id="9b5ba-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="9b5ba-144">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-144">Click Designer.</span></span>
2. <span data-ttu-id="9b5ba-145">Klik op Uitvouwen/samenvouwen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="9b5ba-146">Klik op Uitvouwen/samenvouwen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="9b5ba-147">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="9b5ba-148">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="9b5ba-149">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="9b5ba-150">Typ "IBAN" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="9b5ba-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-151">Click OK.</span></span>
9. <span data-ttu-id="9b5ba-152">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="9b5ba-153">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="9b5ba-154">Selecteer "Text\String" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="9b5ba-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-155">Click OK.</span></span>
13. <span data-ttu-id="9b5ba-156">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="9b5ba-157">Voer in het veld Maximumlengte '60' in.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="9b5ba-158">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="9b5ba-159">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="9b5ba-160">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="9b5ba-161">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="9b5ba-162">Vouw "model\Payments\Creditor\Account" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="9b5ba-163">Selecteer in de structuur 'model\Payments\Creditor\Account\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="9b5ba-164">Selecteer in de structuur 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\IBAN\String'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="9b5ba-165">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-165">Click Bind.</span></span>
23. <span data-ttu-id="9b5ba-166">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="9b5ba-167">De aangepaste indeling valideren</span><span class="sxs-lookup"><span data-stu-id="9b5ba-167">Validate the customized format</span></span>
1. <span data-ttu-id="9b5ba-168">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-168">Click Validate.</span></span>

    <span data-ttu-id="9b5ba-169">Valideer de aangepaste indeling en gegevenstoewijzingswijzigingen om ervoor te zorgen dat alle bindingen in orde zijn.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="9b5ba-170">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="9b5ba-171">De status van de huidige versie van de configuratie van de aangepaste indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="9b5ba-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="9b5ba-172">Wijzig de status van de ontworpen indelingsconfiguratie van Concept in Voltooid om deze beschikbaar te maken voor het genereren van betalingsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="9b5ba-173">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-173">Click Change status.</span></span>

    <span data-ttu-id="9b5ba-174">De huidige versie van de geselecteerde configuratie heeft de status Concept.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9b5ba-175">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-175">Click Complete.</span></span>
3. <span data-ttu-id="9b5ba-176">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9b5ba-177">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-177">Click OK.</span></span>
5. <span data-ttu-id="9b5ba-178">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9b5ba-179">Merk op dat de gemaakte configuratie wordt opgeslagen als voltooide versie 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="9b5ba-180">Dit houdt in dat het versie 1 van de aangepaste BACS-indeling (UK fictief en aangepast) is, die is gebaseerd op versie 1 van de BACS-indeling (UK fictief), die is gebaseerd op versie 1 van het gegevensmodel Betalingen (vereenvoudigd model).</span><span class="sxs-lookup"><span data-stu-id="9b5ba-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="9b5ba-181">De aangepaste indeling testen om betalingsbestanden te genereren</span><span class="sxs-lookup"><span data-stu-id="9b5ba-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="9b5ba-182">Voer de stappen van de procedure "Gemaakte indeling gebruiken om elektronische documenten voor betalingen te genereren" uit in een parallelle Finance and Operations-sessie.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="9b5ba-183">Selecteer de indeling BACS (UK fictief) in parameters voor elektronische betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="9b5ba-184">Zorg ervoor dat het gemaakte betalingsbestand het zojuist geïntroduceerde XML-knooppunt bevat dat de IBAN-code in overeenstemming met regionale vereisten weergeeft.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="9b5ba-185">De bestaande landspecifieke configuratie bijwerken</span><span class="sxs-lookup"><span data-stu-id="9b5ba-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="9b5ba-186">Litware, Inc. moet de configuratie BACS (UK fictief) bijwerken en nieuwe landvereisten aannemen voor het beheren van de indeling van het elektronische document.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="9b5ba-187">Later wordt deze in een nieuwe versie van deze configuratie ingesloten die wordt aangeboden voor serviceabonnees, inclusief Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="9b5ba-188">In de echte service-inrichtingsgerelateerde processen kan elke nieuwe versie van BACS (UK fictief) worden geïmporteerd door Proseware, Inc. uit de LCS-opslagplaats met configuraties van Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="9b5ba-189">In deze procedure wordt dit gesimuleerd door BACS (UK fictief) namens een serviceprovider.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="9b5ba-190">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-190">Close the page.</span></span>
2. <span data-ttu-id="9b5ba-191">Selecteer Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="9b5ba-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="9b5ba-192">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-192">Click Set active.</span></span>
4. <span data-ttu-id="9b5ba-193">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9b5ba-194">Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9b5ba-195">Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="9b5ba-196">De conceptversie in bezit van de provider Litware, Inc. BACS (UK fictief) wordt geselecteerd om wijzigingen aan te brengen ter ondersteuning van nieuwe landspecifieke vereisten.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="9b5ba-197">De basisindeling van elektronisch documenten lokaliseren</span><span class="sxs-lookup"><span data-stu-id="9b5ba-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="9b5ba-198">Stel dat er nieuwe land/regio-specifieke behoeften moeten worden ondersteund door Litware, Inc.:</span><span class="sxs-lookup"><span data-stu-id="9b5ba-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="9b5ba-199">Een waarde voor de bank-SWIFT-code van de crediteur in elke betalingstransactie.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="9b5ba-200">Een limiet van 100 tekens voor de lengte van de tekst voor de naam van de leverancier in een bestand dat wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="9b5ba-201">Nieuwe landspecifieke vereisten</span><span class="sxs-lookup"><span data-stu-id="9b5ba-201">New country-specific requirements</span></span>  
- <span data-ttu-id="9b5ba-202">Selecteer de conceptversie van de gewenste configuratie om de vereiste wijzigingen te introduceren.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="9b5ba-203">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-203">Click Designer.</span></span>
2. <span data-ttu-id="9b5ba-204">Klik op Uitvouwen/samenvouwen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="9b5ba-205">Klik op Uitvouwen/samenvouwen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="9b5ba-206">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="9b5ba-207">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="9b5ba-208">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="9b5ba-209">Typ "SWIFT" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="9b5ba-210">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-210">Click OK.</span></span>
9. <span data-ttu-id="9b5ba-211">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="9b5ba-212">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="9b5ba-213">Selecteer "Text\String" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="9b5ba-214">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-214">Click OK.</span></span>
13. <span data-ttu-id="9b5ba-215">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="9b5ba-216">Voer in het veld Maximumlengte '100' in.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="9b5ba-217">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="9b5ba-218">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="9b5ba-219">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="9b5ba-220">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="9b5ba-221">Vouw "model\Payments\Creditor\Agent" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="9b5ba-222">Selecteer in de structuur 'model\Payments\Creditor\Agent\SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="9b5ba-223">Selecteer in de structuur 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\SWIFT\String'.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="9b5ba-224">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-224">Click Bind.</span></span>
23. <span data-ttu-id="9b5ba-225">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="9b5ba-226">De gelokaliseerde indeling valideren</span><span class="sxs-lookup"><span data-stu-id="9b5ba-226">Validate the localized format</span></span>
1. <span data-ttu-id="9b5ba-227">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-227">Click Validate.</span></span>
2. <span data-ttu-id="9b5ba-228">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="9b5ba-229">De status van de huidige versie van de basisindelingsconfiguratie wijzigen</span><span class="sxs-lookup"><span data-stu-id="9b5ba-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="9b5ba-230">Wijzig de status van de bijgewerkte configuratie van de basisindeling van Concept in Voltooid om deze beschikbaar te maken voor het genereren van betalingsdocumenten en updates van indelingsconfiguraties die ervan zijn afgeleid.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="9b5ba-231">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-231">Click Change status.</span></span>

    <span data-ttu-id="9b5ba-232">De huidige versie van de geselecteerde configuratie heeft de status Concept.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9b5ba-233">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-233">Click Complete.</span></span>
3. <span data-ttu-id="9b5ba-234">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9b5ba-235">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-235">Click OK.</span></span>
5. <span data-ttu-id="9b5ba-236">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="9b5ba-237">De basisversie voor de configuratie van de aangepaste indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="9b5ba-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="9b5ba-238">Proseware, Inc. wordt geïnformeerd dat een nieuwe versie 1.2 van de configuratie BACS (UK fictief UK) beschikbaar is voor het genereren van elektronische betalingsdocumenten in overeenstemming met de recent aangekondigde landspecifieke vereisten.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="9b5ba-239">Proseware, Inc. wil deze als standaard voor het land gaan gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="9b5ba-240">Hiervoor moet Proseware, Inc. de versie van de basisconfiguratie voor de aangepaste configuratie BACS (UK fictief en aangepast) wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="9b5ba-241">Gebruik in plaats van versie 1.1 van BACS (UK fictief) de nieuwe versie 1.2.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="9b5ba-242">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9b5ba-243">Selecteer Proseware, Inc. en maak hiervan een actieve leverancier.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="9b5ba-244">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-244">Click Set active.</span></span>
4. <span data-ttu-id="9b5ba-245">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9b5ba-246">Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9b5ba-247">Vouw 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="9b5ba-248">Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)\BACS (UK fictief en aangepast)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="9b5ba-249">Selecteer de configuratie BACS (UK fictief en aangepast) waarvan Proseware, Inc. eigenaar is.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="9b5ba-250">Gebruik de conceptversie van de geselecteerde configuratie om de vereiste wijzigingen te introduceren.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="9b5ba-251">Klik op Rebase.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-251">Click Rebase.</span></span>

    <span data-ttu-id="9b5ba-252">Selecteer de nieuwe versie 1.2 van de basisconfiguratie die als een nieuwe basis moet worden toegepast voor het bijwerken van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="9b5ba-253">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-253">Click OK.</span></span>

    <span data-ttu-id="9b5ba-254">Er zijn enkele conflicten geconstateerd tussen het samenvoegen van de aangepaste versie en een nieuwe basisversie. Dit betreft enkele indelingswijzigingen die niet automatisch kunnen worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="9b5ba-255">Rebaseconflicten oplossen</span><span class="sxs-lookup"><span data-stu-id="9b5ba-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="9b5ba-256">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-256">Click Designer.</span></span>
    
    <span data-ttu-id="9b5ba-257">Wijzigingen in de limiet voor de tekstlengte van de naam van de leverancier kunnen niet automatisch worden opgelost.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="9b5ba-258">Daarom wordt dit aangegeven in een lijst met conflicten.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="9b5ba-259">Voor elk conflict van het type Update zijn de volgende opties beschikbaar: - Pas een eerdere basiswaarde (knop boven aan het raster) toe om de vorige waarde van de basisversie te gebruiken (0 in ons geval).</span><span class="sxs-lookup"><span data-stu-id="9b5ba-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="9b5ba-260">- Pas een basiswaarde (knop boven aan het raster) om de nieuwe waarde van de basisversie te gebruiken (100 in ons geval).</span><span class="sxs-lookup"><span data-stu-id="9b5ba-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="9b5ba-261">- Behoud uw eigen (aangepaste) waarde (60 in dit geval).</span><span class="sxs-lookup"><span data-stu-id="9b5ba-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="9b5ba-262">Kik op Basiswaarde toepassen om een landspecifieke limiet van 100 tekens voor de tekstlengte van leveranciersnamen toe te passen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="9b5ba-263">Proseware, Inc. en Litware, Inc. hebben aangepaste en lokale versies van deze indeling waarin IBAN- en SWIFT-codes worden gebruikt met gerelateerde componenten die automatisch worden samengevoegd in de indeling.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="9b5ba-264">Klik op Basiswaarde toepassen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-264">Click Apply base value.</span></span>

    <span data-ttu-id="9b5ba-265">Kik op Basiswaarde toepassen om de landspecifieke limiet van 100 tekens voor leveranciersnamen toe te passen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="9b5ba-266">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-266">Click Save.</span></span>

    <span data-ttu-id="9b5ba-267">Als u de indeling opslaat, worden opgeloste conflicten uit de lijst met conflicten verwijderd.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="9b5ba-268">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="9b5ba-269">De status van de nieuwe versie van de configuratie van de aangepaste indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="9b5ba-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="9b5ba-270">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-270">Click Change status.</span></span>

    <span data-ttu-id="9b5ba-271">Wijzig de status van de bijgewerkte, aangepaste indelingsconfiguratie van Concept in Voltooid.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="9b5ba-272">Hierdoor wordt de indelingsconfiguratie beschikbaar voor het genereren van betalingsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="9b5ba-273">De huidige versie van de geselecteerde configuratie heeft de status Concept.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9b5ba-274">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-274">Click Complete.</span></span>
3. <span data-ttu-id="9b5ba-275">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9b5ba-276">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-276">Click OK.</span></span>

    <span data-ttu-id="9b5ba-277">De gemaakte configuratie wordt als voltooide versie 1.2.2 opgeslagen: versie 2 van de basisindeling BACS (UK fictief en aangepast), die is gebaseerd op versie 2 van basisindeling BACS (UK fictief), die is gebaseerd op versie 1 van het gegevensmodel Betalingen (vereenvoudigd model).</span><span class="sxs-lookup"><span data-stu-id="9b5ba-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="9b5ba-278">De aangepaste indeling testen om betalingsbestanden te genereren</span><span class="sxs-lookup"><span data-stu-id="9b5ba-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="9b5ba-279">Voer de stappen van de procedure "Gemaakte indeling gebruiken om elektronische documenten voor betalingen te genereren" uit in een parallelle Finance and Operations-sessie.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="9b5ba-280">Selecteer de gemaakte indeling 'BACS (UK fictief en aangepast)' in parameters voor elektronische betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="9b5ba-281">Zorg ervoor dat het gemaakte betalingsbestand het zojuist door Proseware, Inc. geïntroduceerde XML-knooppunt bevat dat de IBAN-rekeningcode in overeenstemming met regionale vereisten weergeeft.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="9b5ba-282">Het bestand moet ook het onlangs door Litware, Inc. geïntroduceerde XML-knooppunt met de SWIFT-bankcode bevatten conform de landvereisten.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]