---
title: 'ER: onderdelen van de nieuwe indeling toewijzen aan gegevensmodelelementen (november 2016)'
description: In dit onderwerp wordt beschreven hoe u gegevensmodelelementen toekent aan componenten van de gemaakte ER-configuratie (Electronic Reporting).
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c3c06abbd0b4cab5e672c83ccf9c28f2d148dae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751529"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="38192-103">ER: onderdelen van de nieuwe indeling toewijzen aan gegevensmodelelementen (november 2016)</span><span class="sxs-lookup"><span data-stu-id="38192-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38192-104">In de volgende procedure ziet u hoe een gebruiker in de rol van systeembeheerder of de ER-ontwikkelaar elementen van gegevensmodellen kan toewijzen aan onderdelen van de gemaakte ER-configuratie, waarin een elektronisch document voor het zakelijk domein van betalingen wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="38192-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="38192-105">Met deze indeling worden later elektronische documenten gegenereerd voor de verwerking van betalingen.</span><span class="sxs-lookup"><span data-stu-id="38192-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="38192-106">In dit voorbeeld maakt u een indelingsconfiguratie voor het voorbeeldbedrijf 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="38192-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="38192-107">Deze stappen kunnen in elk bedrijf worden uitgevoerd wanneer ER-configuraties tussen alle bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="38192-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="38192-108">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de taakbegeleiding "Een indelingsconfiguratie maken" uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="38192-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="38192-109">Een indelingsconfiguratie selecteren</span><span class="sxs-lookup"><span data-stu-id="38192-109">Select a format configuration</span></span>
1. <span data-ttu-id="38192-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="38192-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="38192-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="38192-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="38192-112">Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="38192-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="38192-113">Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="38192-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="38192-114">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="38192-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="38192-115">Indelingsonderdelen toewijzen aan gegevensmodelelementen</span><span class="sxs-lookup"><span data-stu-id="38192-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="38192-116">Klik op Uitvouwen/samenvouwen.</span><span class="sxs-lookup"><span data-stu-id="38192-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="38192-117">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="38192-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="38192-118">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="38192-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="38192-119">Selecteer in de structuur 'Xml\Message\ProcessingDate\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="38192-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="38192-120">Selecteer in de structuur 'model\ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="38192-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="38192-121">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-121">Click Bind.</span></span>
7. <span data-ttu-id="38192-122">Selecteer in de structuur 'Xml\Message\MessageId\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="38192-123">Selecteer in de structuur 'model\MessageIdentification'.</span><span class="sxs-lookup"><span data-stu-id="38192-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="38192-124">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-124">Click Bind.</span></span>
10. <span data-ttu-id="38192-125">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="38192-126">Selecteer in de structuur 'Xml\Message\Payments\Item\Amount\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="38192-127">Selecteer in de structuur 'model\Payments\InstructedAmount'.</span><span class="sxs-lookup"><span data-stu-id="38192-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="38192-128">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-128">Click Bind.</span></span>
14. <span data-ttu-id="38192-129">Selecteer in de structuur 'Xml\Message\Payments\Item\TransDate\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="38192-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="38192-130">Selecteer in de structuur 'model\Payments\TransactionDate'.</span><span class="sxs-lookup"><span data-stu-id="38192-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="38192-131">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-131">Click Bind.</span></span>
17. <span data-ttu-id="38192-132">Selecteer in de structuur 'Xml\Message\Payments\Item\Description\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="38192-133">Selecteer "model\Payments\Description" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="38192-134">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-134">Click Bind.</span></span>
20. <span data-ttu-id="38192-135">Selecteer in de structuur 'Xml\Message\Payments\Item\Currency\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="38192-136">Selecteer 'model\Payments\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="38192-137">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-137">Click Bind.</span></span>
23. <span data-ttu-id="38192-138">Selecteer in de structuur 'Xml\Message\Payments\Item\Id'.</span><span class="sxs-lookup"><span data-stu-id="38192-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="38192-139">Selecteer in de structuur 'model\Payments\End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="38192-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="38192-140">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-140">Click Bind.</span></span>
26. <span data-ttu-id="38192-141">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="38192-142">Vouw "model\Payments\Creditor\Account" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="38192-143">Vouw "model\Payments\Creditor\Agent" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="38192-144">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="38192-145">Selecteer "model\Payments\Creditor\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="38192-146">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-146">Click Bind.</span></span>
32. <span data-ttu-id="38192-147">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="38192-148">Selecteer in de structuur 'model\Payments\Creditor\Agent\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="38192-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="38192-149">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-149">Click Bind.</span></span>
35. <span data-ttu-id="38192-150">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="38192-151">Selecteer "model\Payments\Creditor\Account\Number" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="38192-152">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-152">Click Bind.</span></span>
38. <span data-ttu-id="38192-153">Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="38192-154">Vouw "model\Payments\Debtor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="38192-155">Vouw "model\Payments\Debtor\Account" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="38192-156">Vouw "model\Payments\Debtor\Agent" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="38192-157">Selecteer "model\Payments\Debtor\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="38192-158">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-158">Click Bind.</span></span>
44. <span data-ttu-id="38192-159">Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="38192-160">Selecteer in de structuur 'model\Payments\Debtor\Agent\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="38192-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="38192-161">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-161">Click Bind.</span></span>
47. <span data-ttu-id="38192-162">Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="38192-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="38192-163">Selecteer "model\Payments\Debtor\Account\Number" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="38192-164">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-164">Click Bind.</span></span>
50. <span data-ttu-id="38192-165">Selecteer in de structuur 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="38192-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="38192-166">Selecteer "model\Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38192-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="38192-167">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="38192-167">Click Bind.</span></span>
53. <span data-ttu-id="38192-168">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="38192-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="38192-169">Indelingstoewijzing valideren</span><span class="sxs-lookup"><span data-stu-id="38192-169">Validate format mapping</span></span>
1. <span data-ttu-id="38192-170">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="38192-170">Click Validate.</span></span>
    * <span data-ttu-id="38192-171">De nieuwe toewijzing valideren om te controleren of alle bindingen in orde zijn.</span><span class="sxs-lookup"><span data-stu-id="38192-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="38192-172">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="38192-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="38192-173">Status van de huidige versie van de indelingsconfiguratie wijzigen</span><span class="sxs-lookup"><span data-stu-id="38192-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="38192-174">In de volgende stappen gaat u de status van de indelingsconfiguratie wijzigen van Concept naar Voltooid, om deze beschikbaar te maken voor het genereren van betalingsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="38192-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="38192-175">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="38192-175">Click Change status.</span></span>
2. <span data-ttu-id="38192-176">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="38192-176">Click Complete.</span></span>
3. <span data-ttu-id="38192-177">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="38192-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="38192-178">Bijvoorbeeld: 'versie 1'.</span><span class="sxs-lookup"><span data-stu-id="38192-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="38192-179">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="38192-179">Click OK.</span></span>
5. <span data-ttu-id="38192-180">Selecteer de ingevulde versie van de huidige configuratie.</span><span class="sxs-lookup"><span data-stu-id="38192-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="38192-181">Merk op dat de configuratie wordt opgeslagen als voltooide versie 1.1: versie 1 van de indeling, gebaseerd op versie 1 van het gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="38192-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="38192-182">Ingangsdatum voor voltooide versie van indeling definiëren</span><span class="sxs-lookup"><span data-stu-id="38192-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="38192-183">Elke indelingsversie kan worden geconfigureerd als beschikbaar voor gebruik vanaf een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="38192-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="38192-184">Wanneer meer dan één indelingsversie actief is op een bepaalde datum, wordt de meest recente indeling (op basis van versienummer) geselecteerd voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="38192-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="38192-185">De waarde van de sessiedatum wordt gebruikt voor selectie van de juiste versie.</span><span class="sxs-lookup"><span data-stu-id="38192-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="38192-186">Toegang tot gemaakte indeling van bedrijven beperken</span><span class="sxs-lookup"><span data-stu-id="38192-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="38192-187">Vouw de sectie ISO-land-/regiocodes uit.</span><span class="sxs-lookup"><span data-stu-id="38192-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="38192-188">Elke indelingstoegang kan worden beperkt door bepaalde landen/regio's te identificeren waarin een indeling van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="38192-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="38192-189">Als de lijst met landen/regio's voor een specifieke indeling leeg is, kan deze indeling worden gebruikt in elk bedrijf.</span><span class="sxs-lookup"><span data-stu-id="38192-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="38192-190">Als enkele ISO-land-/regiocodes worden ingevoegd in de lijst met landen/regio's, kan deze indeling alleen in bedrijven worden gebruikt waarvan het primaire adres in de land-/regiocode uit die lijst is gelegen.</span><span class="sxs-lookup"><span data-stu-id="38192-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]