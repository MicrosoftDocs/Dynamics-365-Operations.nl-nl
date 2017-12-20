---
title: "De datamart voor financiële rapportage opnieuw instellen"
description: "In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: nl-nl
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="7fdbd-103">De datamart voor financiële rapportage opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="7fdbd-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7fdbd-104">In dit onderwerp wordt uitgelegd hoe u de datamart voor financiële rapportage opnieuw instelt voor de volgende versies:</span><span class="sxs-lookup"><span data-stu-id="7fdbd-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="7fdbd-105">Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.2.6.0 en hoger</span><span class="sxs-lookup"><span data-stu-id="7fdbd-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="7fdbd-106">Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.0.10000.4 en hoger</span><span class="sxs-lookup"><span data-stu-id="7fdbd-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="7fdbd-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="7fdbd-108">Voor Finance and Operations Financial Reporting 7.2.6.0 kunt u KB 4052514 downloaden via <https://support.microsoft.com/en-us/help/4052514>.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="7fdbd-109">De datamart voor financiële rapportage opnieuw instellen voor Finance and Operations Financial Reporting 7.2.6.0 en hoger</span><span class="sxs-lookup"><span data-stu-id="7fdbd-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="7fdbd-110">De datamart voor financiële rapportage opnieuw instellen vanuit Rapportontwerper</span><span class="sxs-lookup"><span data-stu-id="7fdbd-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="7fdbd-111">De stappen in dit proces worden ondersteund voor Finance and Operations Financial Reporting 7.2.6.0 en hoger.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="7fdbd-112">Als u een oudere versie hebt, neemt u voor ondersteuning contact op met het ondersteuningsteam.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="7fdbd-113">In bepaalde gevallen moet u de datamart voor financiële rapportage mogelijk opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="7fdbd-114">U kunt deze taak voltooien in de client Rapportontwerper.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="7fdbd-115">Hier volgen enkele scenario's waarin u de datamart wellicht opnieuw moet instellen:</span><span class="sxs-lookup"><span data-stu-id="7fdbd-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="7fdbd-116">De Finance and Operations-database is opnieuw ingesteld, maar de database van de datamart niet.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="7fdbd-117">Gedurende een periode worden er onjuiste gegevens weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="7fdbd-118">Van de ondersteuning krijgt u instructies voor het opnieuw instellen van de datamart als onderdeel van een stap voor probleemoplossing.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="7fdbd-119">De datamart moet alleen opnieuw worden ingesteld op tijden dat de database relatief licht wordt belast.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="7fdbd-120">Financiële rapportage is niet beschikbaar tijdens het proces van opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="7fdbd-121">De datamart opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="7fdbd-121">Reset the data mart</span></span>

<span data-ttu-id="7fdbd-122">Als u de datamart opnieuw wilt instellen, selecteert u in Rapportontwerper in het menu **Extra** de optie **Datamart opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="7fdbd-123">Het dialoogvenster dat verschijnt, bevat twee secties: **Statistieken** en **Opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="7fdbd-124">[![Dialoogvenster Datamart opnieuw instellen](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="7fdbd-125">Integratiepogingen</span><span class="sxs-lookup"><span data-stu-id="7fdbd-125">Integration attempts</span></span>

<span data-ttu-id="7fdbd-126">In het raster **Integratiepogingen** ziet u hoe vaak het systeem heeft geprobeerd transacties te integreren.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="7fdbd-127">Als de eerste paar pogingen mislukken, blijft het systeem het enkele dagen proberen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="7fdbd-128">U weet dat de datamart opnieuw moet worden ingesteld als het aantal pogingen 8 of meer is en er veel dimensiecombinatie- of transactierecords zijn.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="7fdbd-129">In deze situatie worden de gegevens niet gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="7fdbd-130">Status gegevens</span><span class="sxs-lookup"><span data-stu-id="7fdbd-130">Data status</span></span>

<span data-ttu-id="7fdbd-131">Het raster **Status gegevens** biedt een momentopname van de transacties, wisselkoersen en dimensiewaarden in de datamart.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="7fdbd-132">Een groot aantal verouderde records duidt erop dat een groot aantal updates van de records is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="7fdbd-133">Deze situatie kan ertoe leiden dat rapporten langzamer worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="7fdbd-134">Onjuist uitgelijnde hoofdrekeningcategorieën</span><span class="sxs-lookup"><span data-stu-id="7fdbd-134">Misaligned main account categories</span></span>

<span data-ttu-id="7fdbd-135">Als u een oudere versie dan Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.2.1 gebruikt, moet u de datamart wellicht opnieuw instellen als u namen van rekeningen wijzigt en rekeningen tussen rekeningcategorieën verplaatst.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="7fdbd-136">Deze acties kunnen ertoe leiden dat hoofdrekeningcategorieën onjuist worden uitgelijnd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="7fdbd-137">In het veld **Onjuist uitgelijnde hoofdrekeningcategorieën** wordt aangegeven of dit probleem zich voordoet.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="7fdbd-138">De datamart opnieuw instellen in Finance and Operations Financial Reporting 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="7fdbd-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="7fdbd-139">Als u de datamart opnieuw wilt instellen in Finance and Operations Financial Reporting 7.2.6.0 of eerdere versies, schakelt u in het dialoogvenster **Datamart opnieuw instellen** het selectievakje **Datamart opnieuw instellen** in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="7fdbd-140">Stel de datamart alleen opnieuw in tijdens een geplande uitvaltijd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="7fdbd-141">[![Selectievakje Datamart opnieuw instellen](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="7fdbd-142">De datamart opnieuw instellen en een reden selecteren in Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.3.0</span><span class="sxs-lookup"><span data-stu-id="7fdbd-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="7fdbd-143">Als u vaststelt dat een datamart opnieuw moet worden ingesteld, schakelt u het selectievakje **Datamart opnieuw instellen** in en selecteert u een reden in het veld **Reden**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="7fdbd-144">De volgende opties zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="7fdbd-144">The following options are available:</span></span>

- <span data-ttu-id="7fdbd-145">**Ontbrekende of onjuiste gegevens**: op basis van de statistieken hebt u vastgesteld dat er mogelijk gegevens ontbreken.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="7fdbd-146">Voordat u doorgaat, wordt u aangeraden contact op te nemen met de ondersteuning om de hoofdoorzaak te achterhalen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="7fdbd-147">**Database herstellen**: de Finance and Operations-database is hersteld, maar de database van de datamart voor financiële rapportage niet.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="7fdbd-148">**Overige**: u herstelt de datamart om een andere reden.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="7fdbd-149">Als u vermoedt dat er een probleem is, moet u contact opnemen met de ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="7fdbd-150">Controleer voordat u de stappen voltooit of alle bestaande taken zijn geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="7fdbd-151">U kunt de status van de integratie weergeven door **Extra** &gt; **Integratiestatus** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="7fdbd-152">Gebruikers en bedrijven wissen</span><span class="sxs-lookup"><span data-stu-id="7fdbd-152">Clear users and companies</span></span>

<span data-ttu-id="7fdbd-153">Schakel het selectievakje **Gebruikers en bedrijven wissen** in als u uw database opnieuw hebt ingesteld, maar vervolgens wijzigingen hebt doorgevoerd in gebruikers of bedrijven.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="7fdbd-154">U hoeft dit selectievakje zelden in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="7fdbd-155">Wanneer u klaar bent om het proces voor opnieuw instellen te starten, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="7fdbd-156">U wordt gevraagd te bevestigen dat u het proces wilt starten.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="7fdbd-157">Houd er rekening mee dat financiële rapportage niet beschikbaar is tijdens het opnieuw instellen en de initiële gegevensintegratie daarna.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="7fdbd-158">Als u de status van de integratie wilt bekijken, selecteert u **Extra** &gt; **Integratiestatus** om na te gaan wanneer de integratie het laatst is uitgevoerd en de status te bekijken.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="7fdbd-159">[![De status van de integratie weergeven](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="7fdbd-160">De datamart voor financiële rapportage opnieuw instellen voor Finance and Operations Financial Reporting 7.0.10000.4 en hoger</span><span class="sxs-lookup"><span data-stu-id="7fdbd-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="7fdbd-161">Als u uw Finance and Operations-database opnieuw moet instellen vanaf een back-up of de database uit een andere omgeving kopieert, moet u de stappen in dit gedeelte volgen om te zorgen dat de datamart voor financiële rapportage correct gebruikmaakt van de opnieuw ingestelde Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="7fdbd-162">De stappen in dit proces worden ondersteund voor Microsoft Dynamics AX 7.0.1 (mei 2016) (toepassingsbuild 7.0.1265.23014 en Financial Reporting-build 7.0.10000.4) en hoger.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="7fdbd-163">Als u een eerdere versie van Finance and Operations hebt, neemt u voor hulp contact op met de ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="7fdbd-164">Rapportdefinities exporteren</span><span class="sxs-lookup"><span data-stu-id="7fdbd-164">Export report definitions</span></span>

<span data-ttu-id="7fdbd-165">Volg eerst deze stappen als u de rapportontwerpen wilt exporteren vanuit Rapportontwerper.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="7fdbd-166">Selecteer in Rapportontwerper de optie **Bedrijf** &gt; **Bouwsteengroepen**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="7fdbd-167">Selecteer de bouwsteengroep die u wilt exporteren en selecteer **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fdbd-168">Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="7fdbd-169">Selecteer de rapportdefinities die u wilt exporteren:</span><span class="sxs-lookup"><span data-stu-id="7fdbd-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="7fdbd-170">Als u alle rapportdefinities en de bijbehorende bouwstenen wilt exporteren, selecteert u **Alles selecteren**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="7fdbd-171">U kunt specifieke rapporten, rijen, kolommen, structuren of dimensiesets exporteren door het gewenste tabblad te selecteren en vervolgens de te exporteren items te selecteren.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="7fdbd-172">Druk op Ctrl en houd deze toets ingedrukt om meerdere artikelen op een tabblad te selecteren. Wanneer u rapporten selecteert om te exporteren, worden de bijbehorende rijen, kolommen, structuren en dimensiegroepen ook geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="7fdbd-173">Selecteer **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-173">Select **Export**.</span></span>
5. <span data-ttu-id="7fdbd-174">Voer een bestandsnaam in en selecteer de beveiligde locatie waar u de geëxporteerde rapportdefinities wilt opslaan.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="7fdbd-175">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-175">Select **Save**.</span></span>

<span data-ttu-id="7fdbd-176">U kunt het bestand naar een veilige locatie kopiëren of uploaden.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="7fdbd-177">Op deze manier kan het bestand later in een andere omgeving worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="7fdbd-178">Informatie over het gebruik van een Microsoft Azure-opslagaccount vindt u in het onderwerp [Gegevensoverdracht met het opdrachtregelprogramma AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="7fdbd-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="7fdbd-179">Microsoft biedt geen opslagaccount aan als onderdeel van uw Finance and Operations-abonnement.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="7fdbd-180">U moet een opslagaccount aanschaffen of een opslagaccount uit een separaat Azure-abonnement gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="7fdbd-181">Houd rekening met het gedrag van het station D op virtuele Azure-machines (VM's).</span><span class="sxs-lookup"><span data-stu-id="7fdbd-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="7fdbd-182">Sla uw geëxporteerde bouwsteengroepen niet permanent op station D op. Zie [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) voor meer informatie over tijdelijke stations.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="7fdbd-183">Services afstoppen</span><span class="sxs-lookup"><span data-stu-id="7fdbd-183">Stop services</span></span>

<span data-ttu-id="7fdbd-184">De volgende Microsoft Windows-services hebben openstaande verbindingen met de Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="7fdbd-185">Maak via Microsoft Extern bureaublad verbinding met alle computers in de omgeving en stop deze services met services.msc.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="7fdbd-186">World Wide Web Publishing-service (op alle AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="7fdbd-187">Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="7fdbd-188">Management Reporter 2012 Process Service (alleen op BI-computers)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="7fdbd-189">Opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="7fdbd-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="7fdbd-190">Het meest recente pakket met MinorVersionDataUpgrade.zip downloaden</span><span class="sxs-lookup"><span data-stu-id="7fdbd-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="7fdbd-191">Download het meest recente pakket met MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="7fdbd-192">Zie voor meer informatie over het zoeken en downloaden van de juiste versie van het gegevensupgradepakket [Downloaden van het meest recente bruikbare pakket met gegevensupgrade](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="7fdbd-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="7fdbd-193">Een upgrade is niet vereist voor het downloaden van het pakket MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="7fdbd-194">U hoeft alleen maar de stappen in het gedeelte Downloaden van het meest recente bruikbare pakket met gegevensupgrade van dat onderwerp te volgen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="7fdbd-195">U kunt de overige stappen in het onderwerp overslaan.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="7fdbd-196">Scripts uitvoeren op de Finance and Operations-database</span><span class="sxs-lookup"><span data-stu-id="7fdbd-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="7fdbd-197">Voer de volgende scripts uit op de Finance and Operations-database (niet op de database voor financiële rapportage):</span><span class="sxs-lookup"><span data-stu-id="7fdbd-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="7fdbd-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="7fdbd-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="7fdbd-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="7fdbd-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="7fdbd-200">Deze scripts zorgen ervoor dat de gebruikers, rollen en instellingen voor het bijhouden van wijzigingen juist zijn.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="7fdbd-201">Een Windows PowerShell-opdracht uitvoeren om de database opnieuw in te stellen</span><span class="sxs-lookup"><span data-stu-id="7fdbd-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="7fdbd-202">Start Microsoft Windows PowerShell als beheerder op de AOS-computer en voer de volgende opdrachten uit om de integratie tussen Finance and Operations en Financial Reporting opnieuw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="7fdbd-203">Hier volgt een uitleg van de parameters in de opdracht **Reset-DatamartIntegration**:</span><span class="sxs-lookup"><span data-stu-id="7fdbd-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="7fdbd-204">De geldige waarden voor **-Reason** zijn **SERVICING**, **BADDATA** en **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="7fdbd-205">Bij de parameter **-ReasonDetail** kunt u vrije tekst invoeren.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="7fdbd-206">De reden en redengegevens worden vastgelegd in telemetrie/omgevingsbewaking.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="7fdbd-207">Nadat u de opdrachten hebt uitgevoerd, wordt u gevraagd om **Y** in te voeren om te bevestigen dat u de database opnieuw wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="7fdbd-208">Services opnieuw starten</span><span class="sxs-lookup"><span data-stu-id="7fdbd-208">Restart services</span></span>

<span data-ttu-id="7fdbd-209">Start de services die u eerder hebt afgestopt opnieuw op door middel van services.msc:</span><span class="sxs-lookup"><span data-stu-id="7fdbd-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="7fdbd-210">World Wide Web Publishing-service (op alle AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="7fdbd-211">Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="7fdbd-212">Management Reporter 2012 Process Service (alleen op BI-computers)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="7fdbd-213">Rapportdefinities importeren</span><span class="sxs-lookup"><span data-stu-id="7fdbd-213">Import report definitions</span></span>

<span data-ttu-id="7fdbd-214">Importeert uw rapportontwerpen vanuit Rapportontwerper met behulp van het bestand dat tijdens het exporteren is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="7fdbd-215">Selecteer in Rapportontwerper de optie **Bedrijf** &gt; **Bouwsteengroepen**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="7fdbd-216">Selecteer de bouwsteengroep die u wilt exporteren en selecteer **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fdbd-217">Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="7fdbd-218">Selecteer de bouwsteen **Standaard** en selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="7fdbd-219">Selecteer het bestand met de geëxporteerde rapportdefinities en selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="7fdbd-220">Selecteer in het dialoogvenster **Importeren** de rapportdefinities die u wilt importeren:</span><span class="sxs-lookup"><span data-stu-id="7fdbd-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="7fdbd-221">Als u alle rapportdefinities en de bijbehorende bouwstenen wilt importeren, selecteert u **Alles selecteren**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="7fdbd-222">Als u specifieke rapporten, rijen, kolommen, structuren of dimensiegroepen wilt importeren, selecteert u de rapporten, rijen, kolommen, structuren of dimensiegroepen die u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="7fdbd-223">Selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="7fdbd-224">De datamart voor financiële rapportage opnieuw instellen voor Finance and Operations (on-premises)</span><span class="sxs-lookup"><span data-stu-id="7fdbd-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="7fdbd-225">Instrueer alle gebruikers om Rapportontwerper en het gedeelte Financiële rapportage van Finance and Operations af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="7fdbd-226">Voer het volgende script uit op de database voor financiële rapportage (MRDB).</span><span class="sxs-lookup"><span data-stu-id="7fdbd-226">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="7fdbd-227">U moet alle records uit de tabel FINANCIALREPORTS in de Finance and Operations-database (AXDB) afkappen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="7fdbd-228">Als deze tabel aanwezig is, moet u alle records uit de tabel FINANCIALREPORTVERSION in de Finance and Operations-database (AXDB) afkappen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="7fdbd-229">Als de tabel niet bestaat in de Finance and Operations-database, slaat u deze stap over.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="7fdbd-230">Voer het script **ResetDatamart.sql** uit op de database voor financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="7fdbd-231">Met dit script wordt de datamartintegratie uitgeschakeld, worden alle datamartgegevens verwijderd en wordt de datamartintegratie opnieuw ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="7fdbd-232">Na het opnieuw instellen kunt u handmatig controleren of de gegevens opnieuw zijn geladen door de volgende query uit te voeren op de database voor financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="7fdbd-233">Controleer of alle rijen een waarde voor **LastRunTime** bevatten en of **StateType** is ingesteld op **5**.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="7fdbd-234">Wanneer voor **StateType** de waarde **5** wordt weergegeven, zijn de gegevens opnieuw geladen.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="7fdbd-235">Een waarde van **7** geeft een foutstatus aan.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="7fdbd-236">Soms heeft de toewijzing Organisatiehiërarchie deze status wanneer deze voor het eerst wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="7fdbd-237">Als het goed is, wordt de foutstatus automatisch opgelost.</span><span class="sxs-lookup"><span data-stu-id="7fdbd-237">However, the faulted state but should be automatically resolved.</span></span>

