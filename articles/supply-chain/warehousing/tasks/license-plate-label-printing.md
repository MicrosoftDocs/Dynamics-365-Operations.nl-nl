---
title: Afdrukken van nummerplaatlabel inschakelen
description: In dit onderwerp wordt beschreven hoe u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) inschakelt nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e548e5e5528733412d47478dd740b87217cdac2
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016097"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="223d5-103">Afdrukken van nummerplaatlabel inschakelen</span><span class="sxs-lookup"><span data-stu-id="223d5-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="223d5-104">In dit onderwerp wordt beschreven hoe u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) inschakelt nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop.</span><span class="sxs-lookup"><span data-stu-id="223d5-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="223d5-105">U kunt deze procedure in het bedrijf USMF van de demogegevens uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="223d5-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="223d5-106">Als u het met behulp van uw eigen gegevens uitvoert, moet u een ingestelde nummerreeks voor nummerplaten hebben.</span><span class="sxs-lookup"><span data-stu-id="223d5-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="223d5-107">U moet een labelprinter instellen voordat u deze taak start.</span><span class="sxs-lookup"><span data-stu-id="223d5-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="223d5-108">Ga naar Organisatiebeheer > Instellingen > Netwerkprinters.</span><span class="sxs-lookup"><span data-stu-id="223d5-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="223d5-109">Klik in het actievenster op Opties en vervolgens op de knop Installatieprogramma van documentrouteringsagent downloaden.</span><span class="sxs-lookup"><span data-stu-id="223d5-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="223d5-110">Voer het installatieprogramma uit en zorg ervoor dat een netwerkprinter Actief is voordat u met de procedure vervolgt.</span><span class="sxs-lookup"><span data-stu-id="223d5-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="223d5-111">Het GS1-bedrijfsvoorvoegsel instellen</span><span class="sxs-lookup"><span data-stu-id="223d5-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="223d5-112">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="223d5-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="223d5-113">Geef in het veld **GS1-bedrijfsvoorvoegsel** het 7-cijferige GS1-bedrijfsnummer op.</span><span class="sxs-lookup"><span data-stu-id="223d5-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="223d5-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="223d5-114">Select **Save**.</span></span>
4. <span data-ttu-id="223d5-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="223d5-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="223d5-116">De nummerreeks voor het SSCC-nummerplaatnummer instellen</span><span class="sxs-lookup"><span data-stu-id="223d5-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="223d5-117">Ga naar **Navigatiedeelvenster > Modules > Organisatiebeheer > Nummerreeksen > Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="223d5-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="223d5-118">Selecteer een optie in het veld **Gebied**.</span><span class="sxs-lookup"><span data-stu-id="223d5-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="223d5-119">Selecteer een optie in het veld **Verwijzing**.</span><span class="sxs-lookup"><span data-stu-id="223d5-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="223d5-120">Typ een waarde in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="223d5-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="223d5-121">Vouw de sectie **Segmenten** uit.</span><span class="sxs-lookup"><span data-stu-id="223d5-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="223d5-122">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="223d5-122">Select **Edit**.</span></span>
7. <span data-ttu-id="223d5-123">Selecteer in de tabel **Segmenten** de eerste rij</span><span class="sxs-lookup"><span data-stu-id="223d5-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="223d5-124">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="223d5-124">Select **Remove**.</span></span>
9. <span data-ttu-id="223d5-125">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="223d5-125">Select **Remove**.</span></span>
10. <span data-ttu-id="223d5-126">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="223d5-126">Select **Save**.</span></span>
11. <span data-ttu-id="223d5-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="223d5-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="223d5-128">De documentrouteringsindeling maken</span><span class="sxs-lookup"><span data-stu-id="223d5-128">Create the document route layout</span></span>
1. <span data-ttu-id="223d5-129">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Documentroutering > Routeringsindelingen voor documenten**.</span><span class="sxs-lookup"><span data-stu-id="223d5-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="223d5-130">Schakel de SSCC-indeling in.</span><span class="sxs-lookup"><span data-stu-id="223d5-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="223d5-131">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="223d5-131">Select **New**.</span></span>
3. <span data-ttu-id="223d5-132">Typ een waarde in het veld **Indelings-id**.</span><span class="sxs-lookup"><span data-stu-id="223d5-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="223d5-133">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="223d5-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="223d5-134">Selecteer **Invoegen aan einde van tekst**.</span><span class="sxs-lookup"><span data-stu-id="223d5-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="223d5-135">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="223d5-135">Select **Save**.</span></span>
7. <span data-ttu-id="223d5-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="223d5-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="223d5-137">De documentroutering instellen</span><span class="sxs-lookup"><span data-stu-id="223d5-137">Set up the document routing</span></span>
1. <span data-ttu-id="223d5-138">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Documentroutering > Documentroutering**.</span><span class="sxs-lookup"><span data-stu-id="223d5-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="223d5-139">Selecteer een optie in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="223d5-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="223d5-140">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="223d5-140">Select **New**.</span></span>
4. <span data-ttu-id="223d5-141">Typ een waarde in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="223d5-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="223d5-142">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="223d5-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="223d5-143">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="223d5-143">Select **New**.</span></span>
7. <span data-ttu-id="223d5-144">Typ of selecteer een waarde in het veld **Indelings-id**.</span><span class="sxs-lookup"><span data-stu-id="223d5-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="223d5-145">Voer in het veld **Naam** de naam in van de printer die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="223d5-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="223d5-146">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="223d5-146">Select **Save**.</span></span>
10. <span data-ttu-id="223d5-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="223d5-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="223d5-148">Menu voor mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="223d5-148">Create mobile device menu</span></span>
1. <span data-ttu-id="223d5-149">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="223d5-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="223d5-150">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="223d5-150">Select **New**.</span></span>
3. <span data-ttu-id="223d5-151">Typ een waarde in het veld **Menuoptie**.</span><span class="sxs-lookup"><span data-stu-id="223d5-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="223d5-152">Typ een waarde in het veld **Titel**.</span><span class="sxs-lookup"><span data-stu-id="223d5-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="223d5-153">Selecteer een optie in het veld **Modus**.</span><span class="sxs-lookup"><span data-stu-id="223d5-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="223d5-154">Selecteer **Ja** in het veld **Bestaand werk gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="223d5-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="223d5-155">Selecteer **Ja** in het veld **Nummerplaat maken**.</span><span class="sxs-lookup"><span data-stu-id="223d5-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="223d5-156">Vouw de sectie **Werkklassensectie** uit.</span><span class="sxs-lookup"><span data-stu-id="223d5-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="223d5-157">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="223d5-157">Select **New**.</span></span>
10. <span data-ttu-id="223d5-158">Typ een waarde in het veld **Werkklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="223d5-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="223d5-159">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="223d5-159">Select **Save**.</span></span>
12. <span data-ttu-id="223d5-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="223d5-160">Close the page.</span></span>
13. <span data-ttu-id="223d5-161">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="223d5-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="223d5-162">Selecteer in de structuur de menuoptie die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="223d5-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="223d5-163">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="223d5-163">Select **Edit**.</span></span>
16. <span data-ttu-id="223d5-164">Selecteer de pijl om de menuoptie aan het menu toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="223d5-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="223d5-165">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="223d5-165">Select **Save**.</span></span>
18. <span data-ttu-id="223d5-166">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="223d5-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="223d5-167">Een werksjabloon bijwerken</span><span class="sxs-lookup"><span data-stu-id="223d5-167">Update a work template</span></span>
1. <span data-ttu-id="223d5-168">Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Werk >Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="223d5-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="223d5-169">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="223d5-169">Select **Edit**.</span></span>
3. <span data-ttu-id="223d5-170">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="223d5-170">Select **New**.</span></span>
4. <span data-ttu-id="223d5-171">Selecteer **Afdrukken** in het veld **Werktype**.</span><span class="sxs-lookup"><span data-stu-id="223d5-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="223d5-172">Typ of selecteer een waarde in het veld **Werkklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="223d5-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="223d5-173">Selecteer **Omhoog verplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="223d5-173">Select **Move up**.</span></span>
7. <span data-ttu-id="223d5-174">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="223d5-174">Select **Save**.</span></span>
8. <span data-ttu-id="223d5-175">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="223d5-175">Close the page.</span></span>

