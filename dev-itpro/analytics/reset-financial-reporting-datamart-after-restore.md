---
title: "De datamart voor financiële rapportage opnieuw instellen na het herstellen van een database"
description: "In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt na het terugzetten van een Microsoft Dynamics 365 for Finance and Operations-database."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: nl-nl
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="15486-103">De datamart voor financiële rapportage opnieuw instellen na het herstellen van een database</span><span class="sxs-lookup"><span data-stu-id="15486-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="15486-104">In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt na het terugzetten van een Microsoft Dynamics 365 for Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="15486-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="15486-105">Als u uw Finance and Operations-database vanaf een back-up moet terugzetten of de database uit een andere omgeving kopieert, moet u de stappen in dit onderwerp volgen om te zorgen dat de datamart voor financiële rapportage correct gebruikmaakt van de teruggezette Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="15486-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="15486-106">De stappen in dit proces worden ondersteund voor de release van mei 2016 van Dynamics 365 for Operations (App-build 7.0.1265.23014 en financiële rapportage-build 7.0.10000.4) en nieuwere versies.</span><span class="sxs-lookup"><span data-stu-id="15486-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="15486-107">Als u een eerdere versie van Finance and Operations hebt, neem dan contact op met ons ondersteuningsteam voor hulp.</span><span class="sxs-lookup"><span data-stu-id="15486-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="15486-108">Rapportdefinities exporteren</span><span class="sxs-lookup"><span data-stu-id="15486-108">Export report definitions</span></span>
<span data-ttu-id="15486-109">Exporteer eerst de rapportontwerpen die zich in de Report Designer bevinden volgens de onderstaande procedure:</span><span class="sxs-lookup"><span data-stu-id="15486-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="15486-110">Ga in Report Designer naar **Bedrijf** &gt; **Bouwsteengroepen**.</span><span class="sxs-lookup"><span data-stu-id="15486-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="15486-111">Selecteer de bouwsteengroep die u wilt exporteren en klik op **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="15486-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="15486-112">Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="15486-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="15486-113">Selecteer de rapportdefinities die u wilt exporteren:</span><span class="sxs-lookup"><span data-stu-id="15486-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="15486-114">Om al uw rapportdefinities en de gekoppelde bouwstenen te exporteren klikt u op **Alles selecteren**.</span><span class="sxs-lookup"><span data-stu-id="15486-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="15486-115">U kunt specifieke rapporten, rijen, kolommen, structuren of dimensiesets exporteren door op het gewenste tabblad te klikken en vervolgens de te exporteren items selecteren.</span><span class="sxs-lookup"><span data-stu-id="15486-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="15486-116">Druk op Ctrl en houd deze toets ingedrukt om meerdere artikelen in een tabblad te selecteren.</span><span class="sxs-lookup"><span data-stu-id="15486-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="15486-117">Als u te exporteren rapporten selecteert, worden de gekoppelde rijen, kolommen, structuren en dimensiesets geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="15486-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="15486-118">Klik op **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="15486-118">Click **Export**.</span></span>
5.  <span data-ttu-id="15486-119">Voer een bestandsnaam in en selecteer de beveiligde locatie waar u de geëxporteerde rapportdefinities wilt opslaan.</span><span class="sxs-lookup"><span data-stu-id="15486-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="15486-120">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="15486-120">Click **Save**.</span></span>

<span data-ttu-id="15486-121">U kunt het bestand kopiëren of uploaden naar een beveiligde locatie, zodat u het later kunt importeren in een andere omgeving.</span><span class="sxs-lookup"><span data-stu-id="15486-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="15486-122">Informatie over het gebruik van een Microsoft Azure-opslagaccount vindt u in het onderwerp [Gegevensoverdracht met het opdrachtregelprogramma AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="15486-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="15486-123">Microsoft biedt bij uw abonnement voor Finance and Operations geen opslagaccount aan.</span><span class="sxs-lookup"><span data-stu-id="15486-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="15486-124">U moet een opslagaccount aanschaffen of een opslagaccount uit een separaat Azure-abonnement gebruiken.</span><span class="sxs-lookup"><span data-stu-id="15486-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="15486-125">Houd rekening met het gedrag van het station D in virtuele Azure-machines.</span><span class="sxs-lookup"><span data-stu-id="15486-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="15486-126">Bewaar uw geëxporteerde bouwsteengroepen hier niet permanent.</span><span class="sxs-lookup"><span data-stu-id="15486-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="15486-127">Zie voor meer informatie over tijdelijke schijven het onderwerp [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="15486-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="15486-128">Services afstoppen</span><span class="sxs-lookup"><span data-stu-id="15486-128">Stop services</span></span>
<span data-ttu-id="15486-129">Maak via Extern bureaublad verbinding met alle computers in de omgeving en stop de volgende Windows-services af door middel van services.msc:</span><span class="sxs-lookup"><span data-stu-id="15486-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="15486-130">World Wide Web Publishing-service (op alle AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="15486-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="15486-131">Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="15486-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="15486-132">Management Reporter 2012 Process Service (alleen op BI-computers)</span><span class="sxs-lookup"><span data-stu-id="15486-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="15486-133">Deze services hebben openstaande verbindingen met de Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="15486-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="15486-134">Opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="15486-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="15486-135">Zoek het meest recente pakket met MinorVersionDataUpgrade.zip en download het</span><span class="sxs-lookup"><span data-stu-id="15486-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="15486-136">Zoek het meest recente pakket MinorVersionDataUpgrade.zip met de aanwijzingen in het onderwerp [Downloaden van het meest recente bruikbare pakket met gegevensupgrade](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="15486-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="15486-137">De instructies geven aan hoe u de juiste versie van het gegevensupgradepakket voor uw omgeving vindt en downloadt.</span><span class="sxs-lookup"><span data-stu-id="15486-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="15486-138">Een upgrade is niet vereist voor het downloaden van het pakket MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="15486-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="15486-139">U hoeft alleen de stappen in de sectie 'Downloaden van het meest recente bruikbare pakket met gegevensupgrade' uit te voeren zonder de overige stappen in het artikel voor het ophalen van een kopie van het pakket MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="15486-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="15486-140">Scripts uitvoeren op de Finance and Operations-database</span><span class="sxs-lookup"><span data-stu-id="15486-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="15486-141">Voer de volgende scripts uit op de Finance and Operations-database (niet op de database voor financiële rapportage).</span><span class="sxs-lookup"><span data-stu-id="15486-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="15486-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="15486-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="15486-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="15486-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="15486-144">Deze scripts zorgen ervoor dat de gebruikers, rollen en instellingen voor het bijhouden van wijzigingen juist zijn.</span><span class="sxs-lookup"><span data-stu-id="15486-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="15486-145">PowerShell-opdracht uitvoeren om de database opnieuw in te stellen</span><span class="sxs-lookup"><span data-stu-id="15486-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="15486-146">Voer de volgende opdracht direct op de AOS-computer uit, om de integratie tussen Finance and Operations en de financiële rapportage opnieuw in te stellen:</span><span class="sxs-lookup"><span data-stu-id="15486-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="15486-147">Open Windows PowerShell als beheerder.</span><span class="sxs-lookup"><span data-stu-id="15486-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="15486-148">Voer uit: F:</span><span class="sxs-lookup"><span data-stu-id="15486-148">Execute: F:</span></span>
3.  <span data-ttu-id="15486-149">Voer uit: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="15486-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="15486-150">Voer uit: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="15486-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="15486-151">Voer uit: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;mijn_reden_voor_opnieuw_instellen&gt;”</span><span class="sxs-lookup"><span data-stu-id="15486-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="15486-152">U wordt gevraagd om 'Y' in te voeren om te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="15486-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="15486-153">Uitleg van parameters:</span><span class="sxs-lookup"><span data-stu-id="15486-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="15486-154">De geldige waarden voor -Reason zijn: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="15486-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="15486-155">Bij de parameter -ReasonDetail kunt u vrije tekst invoeren.</span><span class="sxs-lookup"><span data-stu-id="15486-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="15486-156">De waarden voor Reason en ReasonDetail worden vastgelegd in telemetrie/omgevingsbewaking.</span><span class="sxs-lookup"><span data-stu-id="15486-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="15486-157">Services opstarten</span><span class="sxs-lookup"><span data-stu-id="15486-157">Start services</span></span>
<span data-ttu-id="15486-158">Start de services die u eerder hebt afgestopt opnieuw op door middel van services.msc:</span><span class="sxs-lookup"><span data-stu-id="15486-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="15486-159">World Wide Web Publishing-service (op alle AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="15486-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="15486-160">Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)</span><span class="sxs-lookup"><span data-stu-id="15486-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="15486-161">Management Reporter 2012 Process Service (alleen op BI-computers)</span><span class="sxs-lookup"><span data-stu-id="15486-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="15486-162">Rapportdefinities importeren</span><span class="sxs-lookup"><span data-stu-id="15486-162">Import report definitions</span></span>
<span data-ttu-id="15486-163">Importeert uw rapportontwerpen vanuit de Report Designer, met behulp van het bestand dat bij het exporteren werd aangemaakt:</span><span class="sxs-lookup"><span data-stu-id="15486-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="15486-164">Ga in Report Designer naar **Bedrijf** &gt; **Bouwsteengroepen**.</span><span class="sxs-lookup"><span data-stu-id="15486-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="15486-165">Selecteer de bouwsteengroep die u wilt exporteren en klik op **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="15486-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="15486-166">Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="15486-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="15486-167">Selecteer de bouwsteen **Standaard** en klik op **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="15486-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="15486-168">Selecteer het bestand met de geëxporteerde rapportdefinities en klik op **Openen**.</span><span class="sxs-lookup"><span data-stu-id="15486-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="15486-169">Selecteer in het dialoogvenster Importeren de te importeren rapportdefinities:</span><span class="sxs-lookup"><span data-stu-id="15486-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="15486-170">Als u alle rapportdefinities en de ondersteunende bouwstenen wilt importeren, klikt u op **Alles selecteren**.</span><span class="sxs-lookup"><span data-stu-id="15486-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="15486-171">Om specifieke rapporten, rijen, kolommen, structuren of dimensiesets te importeren, selecteert u de te importeren rapporten, rijen, kolommen, structuren of dimensiesets.</span><span class="sxs-lookup"><span data-stu-id="15486-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="15486-172">Klik op **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="15486-172">Click **Import**.</span></span>





