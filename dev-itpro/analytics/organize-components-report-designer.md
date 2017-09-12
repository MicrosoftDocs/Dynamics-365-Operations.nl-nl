---
title: Rapportonderdelen indelen in Report Designer
description: Nadat u bouwstenen hebt ontworpen en rapporten hebt gegenereerd, is het handig om deze objecten te ordenen zodat gebruikers ze eenvoudig kunnen vinden. In dit artikel wordt uitgelegd hoe u bestaande rapporten, bouwstenen en objecten in Report Designer kunt organiseren.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fade9e2acdb94daa6a908d949c578fd7ed439882
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="c9709-104">Rapportonderdelen indelen in Report Designer</span><span class="sxs-lookup"><span data-stu-id="c9709-104">Organize report components in report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c9709-105">Nadat u bouwstenen hebt ontworpen en rapporten hebt gegenereerd, is het handig om deze objecten te ordenen zodat gebruikers ze eenvoudig kunnen vinden.</span><span class="sxs-lookup"><span data-stu-id="c9709-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="c9709-106">In dit artikel wordt uitgelegd hoe u bestaande rapporten, bouwstenen en objecten in Report Designer kunt organiseren.</span><span class="sxs-lookup"><span data-stu-id="c9709-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="c9709-107">U kunt de naam van mappen, rapporten, bouwstenen en andere objecten in Report Designer wijzigen om te helpen uw bestanden in te delen.</span><span class="sxs-lookup"><span data-stu-id="c9709-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="c9709-108">Afhankelijk van het type object waarvan u de naam wijzigt, moet u mogelijk koppelingen met dat object bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c9709-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="c9709-109">De naam van een map of bouwsteen wijzigen in Report Designer</span><span class="sxs-lookup"><span data-stu-id="c9709-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="c9709-110">In Report Designer kunt u de naam van mappen, rapportdefinities, rijdefinities, kolomdefinities en rapportagestructuurdefinities wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c9709-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="c9709-111">**Opmerking:** wanneer u de naam van een bouwsteen wijzigt, moet u rapportagedefinities bijwerken die gebruikmaken van de bouwsteen.</span><span class="sxs-lookup"><span data-stu-id="c9709-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="c9709-112">Anders kan geen nieuw rapport worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c9709-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="c9709-113">De naam van een map of bouwsteen wijzigen in Report Designer</span><span class="sxs-lookup"><span data-stu-id="c9709-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="c9709-114">Gebruik in Report Designer het navigatievenster om de map of het object te zoeken waarvan u de naam wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c9709-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="c9709-115">Klik met de rechtermuisknop op de map of het object en klik vervolgens op **Naam wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="c9709-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="c9709-116">Het veld **Naam** in het navigatievenster komt beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="c9709-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="c9709-117">Typ een nieuwe naam en druk vervolgens op Enter.</span><span class="sxs-lookup"><span data-stu-id="c9709-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="c9709-118">Als de bouwsteen een rijdefinitie, kolomdefinitie of rapportagestructuurdefinitie is, moet u andere bouwstenen bijwerken die hieraan zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c9709-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="c9709-119">Klik met de rechtermuisknop op de bouwsteen waarvan u de naam hebt gewijzigd in stap 3, selecteer **Koppelingen** en selecteer vervolgens een item in de lijst om het bij te werken.</span><span class="sxs-lookup"><span data-stu-id="c9709-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="c9709-120">Herhaal stap 4 tot alle gekoppelde artikelen zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="c9709-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="c9709-121">Rapportgroepen maken en beheren</span><span class="sxs-lookup"><span data-stu-id="c9709-121">Create and manage report groups</span></span>
<span data-ttu-id="c9709-122">U kunt rapportdefinities groeperen om meerdere rapporten tegelijk te genereren.</span><span class="sxs-lookup"><span data-stu-id="c9709-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="c9709-123">Als u rapportgroepen wilt maken, wijzigen, verwijderen en genereren, moet u de rol van ontwerper of beheerder hebben.</span><span class="sxs-lookup"><span data-stu-id="c9709-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="c9709-124">Gebruikers die de rol van generator hebben, kunnen rapportgroepen genereren en kunnen ook de instelling van gebruikerrapportdefinities wijzigen voor rapportgroepen.</span><span class="sxs-lookup"><span data-stu-id="c9709-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="c9709-125">Een rapportgroep maken</span><span class="sxs-lookup"><span data-stu-id="c9709-125">Create a report group</span></span>

1.  <span data-ttu-id="c9709-126">Klik in Report Designer in het navigatievenster op **Rapportgroepen**.</span><span class="sxs-lookup"><span data-stu-id="c9709-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="c9709-127">Klik in het menu **Bestand** op **Nieuw** &gt; **Rapportgroepdefinitie** om een nieuwe groep in het venster van de viewer te openen.</span><span class="sxs-lookup"><span data-stu-id="c9709-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="c9709-128">U kunt ook klikken op de knop **Rapportgroep** ![Rapportgroep](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapportgroep") op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="c9709-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="c9709-129">Klik op het tabblad **Rapportgroep** op.</span><span class="sxs-lookup"><span data-stu-id="c9709-129">Click the **Report Group** tab.</span></span> <span data-ttu-id="c9709-130">Als u de informatie over de afzonderlijke rapportdefinities wilt negeren voor het genereren van dit rapport, selecteert u het selectievakje **Instellingen voor bedrijf, gegevens en datum uit afzonderlijke rapportdefinities negeren**.</span><span class="sxs-lookup"><span data-stu-id="c9709-130">To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="c9709-131">De bedrijfsnaam, het detailniveau, voorlopige instellingen en datumgegevens worden automatisch ingevuld, maar u kunt wel updates uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c9709-131">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="c9709-132">Als u meerdere rapporten wilt genereren die de aangiftevaluta tonen, schakelt u het selectievakje **Alle aangiftevaluta opnemen** in.</span><span class="sxs-lookup"><span data-stu-id="c9709-132">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="c9709-133">U kunt vervolgens meerdere weergaven openen door op de knop **Valuta** te klikken in de Web Viewer wanneer u het rapport weergeeft.</span><span class="sxs-lookup"><span data-stu-id="c9709-133">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="c9709-134">Klik in het veld **Rapporten in groep** op **Toevoegen** om de rapporten te selecteren die u in de rapportgroep wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="c9709-134">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="c9709-135">Als u meerdere rapporten wilt selecteren in het dialoogvenster **Toevoegen**, houdt u de toets Ctrl ingedrukt terwijl u rapporten selecteert.</span><span class="sxs-lookup"><span data-stu-id="c9709-135">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="c9709-136">Wanneer u klaar bent met het selecteren van rapporten, klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9709-136">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="c9709-137">Klik op **Bestand** &gt; **Opslaan** om de nieuwe rapportgroep op te slaan.</span><span class="sxs-lookup"><span data-stu-id="c9709-137">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="c9709-138">Een rapportgroep wijzigen</span><span class="sxs-lookup"><span data-stu-id="c9709-138">Modify a report group</span></span>

1.  <span data-ttu-id="c9709-139">Klik in Report Designer in het navigatievenster op **Rapportgroepen**.</span><span class="sxs-lookup"><span data-stu-id="c9709-139">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="c9709-140">Dubbelklik op de rapportgroep die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c9709-140">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="c9709-141">Breng de gewenste wijzigingen aan op het tabblad **Rapportgroep**.</span><span class="sxs-lookup"><span data-stu-id="c9709-141">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="c9709-142">Klik in het menu **Bestand** op **Opslaan** om de gewijzigde rapportgroep op te slaan of klik op de knop **Opslaan** ![Opslaan](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Opslaan") in de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="c9709-142">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="c9709-143">**Opmerking:** als u rapporten hebt gepland die met ingestelde intervallen moeten worden gegenereerd, kunt u die instellingen negeren en onmiddellijk een rapport genereren.</span><span class="sxs-lookup"><span data-stu-id="c9709-143">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="c9709-144">Een rapportgroeprapport genereren</span><span class="sxs-lookup"><span data-stu-id="c9709-144">Generate a report group report</span></span>

1.  <span data-ttu-id="c9709-145">Klik in Report Designer in het navigatievenster op **Rapportgroepen**.</span><span class="sxs-lookup"><span data-stu-id="c9709-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="c9709-146">Open de rapportgroep die u wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="c9709-146">Open the report group to generate.</span></span>
3.  <span data-ttu-id="c9709-147">Klik op de knop **Rapport genereren** ![Rapport genereren](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Rapport genereren") om rapporten te genereren.</span><span class="sxs-lookup"><span data-stu-id="c9709-147">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="c9709-148">Een rapportgroep verwijderen</span><span class="sxs-lookup"><span data-stu-id="c9709-148">Delete a report group</span></span>

1.  <span data-ttu-id="c9709-149">Klik in Report Designer in het navigatievenster op **Rapportgroepen**.</span><span class="sxs-lookup"><span data-stu-id="c9709-149">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="c9709-150">Klik met de rechtermuisknop op de rapportgroep die u wilt verwijderen en selecteer vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="c9709-150">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="c9709-151">Wanneer een bevestigingsbericht wordt weergegeven, klikt u op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c9709-151">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="c9709-152">Besturingselementen op tabblad Rapportgroep</span><span class="sxs-lookup"><span data-stu-id="c9709-152">Report Group tab controls</span></span>
<span data-ttu-id="c9709-153">De volgende tabel bevat beschrijvingen van de besturingselementen op het tabblad **Rapportgroep**.</span><span class="sxs-lookup"><span data-stu-id="c9709-153">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9709-154">Controle</span><span class="sxs-lookup"><span data-stu-id="c9709-154">Control</span></span></th>
<th><span data-ttu-id="c9709-155">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c9709-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9709-156">Instellingen voor bedrijf, gegevens en datum uit afzonderlijke rapportdefinities negeren</span><span class="sxs-lookup"><span data-stu-id="c9709-156">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="c9709-157">Schakel dit selectievakje in om afzonderlijke rapportdefinities van de rapporten in deze rapportgroep te negeren voor alleen artikelgeneratie van deze rapporten.</span><span class="sxs-lookup"><span data-stu-id="c9709-157">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9709-158">Bedrijfsnaam</span><span class="sxs-lookup"><span data-stu-id="c9709-158">Company name</span></span></td>
<td><span data-ttu-id="c9709-159">Selecteer het bedrijf dat u voor de rapporten wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c9709-159">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9709-160">Detailniveau</span><span class="sxs-lookup"><span data-stu-id="c9709-160">Detail level</span></span></td>
<td><span data-ttu-id="c9709-161">Geef het gewenste detailniveau op voor de rapporten.</span><span class="sxs-lookup"><span data-stu-id="c9709-161">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="c9709-162"><strong>Financieel</strong>- Een samenvatting op hoog niveau.</span><span class="sxs-lookup"><span data-stu-id="c9709-162"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="c9709-163">U kunt rekeningen en dimensies niet in detail bekijken, behalve voor de rekeningen en dimensies die via een rapportagestructuur zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c9709-163">You can't drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="c9709-164"><strong>Financieel &amp; rekening</strong> − Een rapport dat een samenvatting op hoog niveau en rekeninggegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="c9709-164"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="c9709-165"><strong>Financieel, rekening &amp; transactie</strong> − Een rapport dat een samenvatting op hoog niveau en transactiegegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="c9709-165"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9709-166">Voorlopig</span><span class="sxs-lookup"><span data-stu-id="c9709-166">Provisional</span></span></td>
<td><span data-ttu-id="c9709-167">Geef de gewenste typen activiteit op voor de rapporten.</span><span class="sxs-lookup"><span data-stu-id="c9709-167">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="c9709-168"><strong>Alleen geboekte activiteit</strong> − Neem alleen de transacties en saldi op die in uw financiële gegevens zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="c9709-168"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="c9709-169"><strong>Geboekte en niet-geboekte activiteit</strong> − Neem alle transacties en saldi op die in uw financiële gegevens zijn ingevoerd en geboekt.</span><span class="sxs-lookup"><span data-stu-id="c9709-169"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="c9709-170"><strong>Alleen niet-geboekte activiteit</strong> − Neem alleen de transacties op die in uw financiële gegevens zijn ingevoerd maar nog niet geboekt.</span><span class="sxs-lookup"><span data-stu-id="c9709-170"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9709-171">Alle aangiftevaluta opnemen</span><span class="sxs-lookup"><span data-stu-id="c9709-171">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="c9709-172">Alle extra aangiftevaluta's die in uw Microsoft Dynamics ERP-systeem zijn geconfigureerd, worden deze hier vermeld.</span><span class="sxs-lookup"><span data-stu-id="c9709-172">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="c9709-173">Schakel dit selectievakje in om extra rapporten te genereren in de valuta's die worden aangegeven.</span><span class="sxs-lookup"><span data-stu-id="c9709-173">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="c9709-174">Als u deze rapporten wilt bekijken in de Web Viewer, klikt u op de knop <strong>Valuta</strong> en selecteert u vervolgens een valuta.</span><span class="sxs-lookup"><span data-stu-id="c9709-174">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9709-175">Datumgegevens die niet zijn opgeslagen met rapportdefinitie</span><span class="sxs-lookup"><span data-stu-id="c9709-175">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="c9709-176">Basisperiode</span><span class="sxs-lookup"><span data-stu-id="c9709-176">Base period</span></span></li>
<li><span data-ttu-id="c9709-177">Basisjaar</span><span class="sxs-lookup"><span data-stu-id="c9709-177">Base year</span></span></li>
<li><span data-ttu-id="c9709-178">Behandelde periode</span><span class="sxs-lookup"><span data-stu-id="c9709-178">Period covered</span></span></li>
</ul>
<span data-ttu-id="c9709-179">Alleen standaardinstellingen voor de basisperiode worden opgeslagen met de rapportdefinitie.</span><span class="sxs-lookup"><span data-stu-id="c9709-179">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9709-180">Datumgegevens die zijn opgeslagen met rapportdefinitie</span><span class="sxs-lookup"><span data-stu-id="c9709-180">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="c9709-181">Rapportdatum</span><span class="sxs-lookup"><span data-stu-id="c9709-181">Report date</span></span></li>
<li><span data-ttu-id="c9709-182">Standaardbasisperiode</span><span class="sxs-lookup"><span data-stu-id="c9709-182">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9709-183">Rapporten in groep</span><span class="sxs-lookup"><span data-stu-id="c9709-183">Reports in group</span></span></td>
<td><span data-ttu-id="c9709-184">U kunt in de rapportgroep rapporten toevoegen, verwijderen en herschikken.</span><span class="sxs-lookup"><span data-stu-id="c9709-184">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="c9709-185">Als u rapportdefinities aan de rapportgroep wilt toevoegen, dubbelklikt u op de rapportgroep om deze te openen en klikt u vervolgens op <strong>Toevoegen</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9709-185">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="c9709-186">Selecteer de rapporten die u in de rapportgroep wilt opnemen en klik vervolgens op <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9709-186">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="c9709-187">Als u een rapport uit de rapportgroep wilt verwijderen, selecteert u dit en klikt u op <strong>Verwijderen</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9709-187">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="c9709-188">Als u de volgorde wilt wijzigen waarin de rapporten worden gegenereerd, selecteert u een rapport in de lijst en klikt u vervolgens op <strong>Omhoog</strong> of <strong>Omlaag</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9709-188">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="c9709-189">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c9709-189">See also</span></span>
--------

[<span data-ttu-id="c9709-190">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="c9709-190">Financial reporting</span></span>](financial-reporting-intro.md)




