---
title: Algemene problemen oplossen
description: Dit onderwerp bevat informatie voor het oplossen van algemene problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172686"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="cb031-103">Algemene problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="cb031-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cb031-104">Dit onderwerp bevat informatie voor het oplossen van algemene problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cb031-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb031-105">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="cb031-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="cb031-106">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="cb031-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="cb031-107">Wanneer u het pakket voor twee keer wegschrijven probeert te installeren met het hulpprogramma Package Deployer, worden er geen beschikbare oplossingen weergegeven</span><span class="sxs-lookup"><span data-stu-id="cb031-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="cb031-108">Sommige versies van het hulpprogramma Package Deployer zijn niet compatibel met het oplossingspakket voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="cb031-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="cb031-109">Als u het pakket wilt installeren, moet u [versie 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) of hoger van het hulpprogramma Package Deployer gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cb031-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="cb031-110">Nadat u het hulpprogramma Package Deployer hebt geïnstalleerd, installeert u het oplossingspakket door de volgende stappen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="cb031-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="cb031-111">Download het meest recente bestand met het oplossingspakket van Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="cb031-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="cb031-112">Nadat het zipbestand met het pakket is gedownload, klikt u erop met de rechtermuisknop en selecteert u **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="cb031-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="cb031-113">Schakel het selectievakje **Deblokkeren** in en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="cb031-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="cb031-114">Als het selectievakje **Deblokkeren** niet wordt weergeven, is het zipbestand al gedeblokkeerd en kunt u deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="cb031-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialoogvenster Eigenschappen](media/unblock_option.png)

2. <span data-ttu-id="cb031-116">Pak het zipbestand uit en kopieer alle bestanden in de map **Dynamics365FinanceAndOperationsCommon. PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="cb031-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Inhoud van de map Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="cb031-118">Plak alle gekopieerde bestanden in de map **Tools** van het hulpprogramma Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="cb031-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="cb031-119">Voer **PackageDeployer.exe** uit om de Common Data Service-omgeving te selecteren en de oplossingen te installeren.</span><span class="sxs-lookup"><span data-stu-id="cb031-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Inhoud van de map Tools](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="cb031-121">Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Common Data Service om foutdetails weer te geven</span><span class="sxs-lookup"><span data-stu-id="cb031-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="cb031-122">**Vereiste rol om het traceerlogboek in te schakelen en fouten weer te geven:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="cb031-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="cb031-123">Voer de volgende stappen uit om het traceerlogboek in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="cb031-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="cb031-124">Meld u aan bij de Finance and Operations-app, open de pagina **Instellingen** en selecteer vervolgens onder **Systeem** de optie **Beheer**.</span><span class="sxs-lookup"><span data-stu-id="cb031-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="cb031-125">Selecteer op de pagina **Beheer** de optie **Systeeminstellingen**.</span><span class="sxs-lookup"><span data-stu-id="cb031-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="cb031-126">Ga naar het tabblad **Aanpassen** en selecteer in het veld **Traceren van invoegtoepassing en aangepaste werkstroomactiviteit** **Alle** om het traceerlogboek voor invoegtoepassingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="cb031-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="cb031-127">Als u traceerlogboeken alleen wilt vastleggen wanneer er uitzonderingen optreden, kunt u in plaats daarvan **Uitzondering** selecteren.</span><span class="sxs-lookup"><span data-stu-id="cb031-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="cb031-128">Voer de volgende stappen uit om het traceerlogboek weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cb031-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="cb031-129">Meld u aan bij de Finance and Operations-app, open de pagina **Instellingen** en selecteer vervolgens onder **Aanpassen** de optie **Traceerlogboek invoegtoepassing**.</span><span class="sxs-lookup"><span data-stu-id="cb031-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="cb031-130">Zoek de traceerlogboeken waarvoor het veld **Type naam** is ingesteld op **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="cb031-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="cb031-131">Dubbelklik op een item om het volledige logboek weer te geven en controleer vervolgens op het sneltabblad **Uitvoering** de tekst **Bericht blokkeren**.</span><span class="sxs-lookup"><span data-stu-id="cb031-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="cb031-132">De modus Foutopsporing inschakelen om live synchronisatieproblemen in Finance and Operations-apps op te lossen</span><span class="sxs-lookup"><span data-stu-id="cb031-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="cb031-133">**Vereiste rol om de fouten weer te geven:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="cb031-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="cb031-134">Fouten met twee keer wegschrijven die afkomstig zijn uit Common Data Service, kunnen worden weergegeven in de  Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="cb031-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="cb031-135">In sommige gevallen is de volledige tekst van het foutbericht niet beschikbaar omdat het bericht te lang is of persoonlijke identificatie gegevens (PII) bevat.</span><span class="sxs-lookup"><span data-stu-id="cb031-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="cb031-136">U kunt uitgebreide logboekregistratie voor fouten inschakelen door de volgende stappen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="cb031-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="cb031-137">Alle projectconfiguraties in Finance and Operations-apps hebben een eigenschap **IsDebugMode** in de entiteit **DualWriteprojectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="cb031-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="cb031-138">Open de entiteit **DualWriteProjectConfiguration** met de Excel-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="cb031-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="cb031-139">Een eenvoudige manier om de entiteit te openen is om de **ontwerp**modus in de Excel-invoegtoepassing in te schakelen en vervolgens **DualWriteprojectConfigurationEntity** toe te voegen aan het werkblad.</span><span class="sxs-lookup"><span data-stu-id="cb031-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="cb031-140">zie [Entiteitsgegevens in Excel openen en bijwerken via de Excel-invoegtoepassing](../../office-integration/use-excel-add-in.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="cb031-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="cb031-141">Stel de eigenschap **IsDebugMode** in op **Ja** voor het project.</span><span class="sxs-lookup"><span data-stu-id="cb031-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="cb031-142">Voer het scenario uit dat fouten genereert.</span><span class="sxs-lookup"><span data-stu-id="cb031-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="cb031-143">De uitgebreide logboeken zijn beschikbaar in de tabel DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="cb031-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="cb031-144">Als u gegevens wilt opzoeken in de tabelbrowser, gebruikt u de volgende URL (vervang **XXX** waar van toepassing):</span><span class="sxs-lookup"><span data-stu-id="cb031-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="cb031-145">Synchronisatiefouten controleren op de virtuele machine voor de Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="cb031-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="cb031-146">**Vereiste rol om de fouten weer te geven:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="cb031-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="cb031-147">Meld u aan bij Microsoft Dynamics LCS (LifeCycle Services).</span><span class="sxs-lookup"><span data-stu-id="cb031-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="cb031-148">Open het LCS-project dat u hebt gekozen voor tests met twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="cb031-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="cb031-149">Selecteer de tegel **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="cb031-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="cb031-150">Gebruik extern bureaublad om u aan te melden bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="cb031-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="cb031-151">Gebruik het lokale account dat wordt weergegeven in LCS.</span><span class="sxs-lookup"><span data-stu-id="cb031-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="cb031-152">Open Logboeken.</span><span class="sxs-lookup"><span data-stu-id="cb031-152">Open Event viewer.</span></span>
6. <span data-ttu-id="cb031-153">Selecteer **Logboeken Toepassingen en Services \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationeel**.</span><span class="sxs-lookup"><span data-stu-id="cb031-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="cb031-154">Bekijk de lijst met recente fouten.</span><span class="sxs-lookup"><span data-stu-id="cb031-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="cb031-155">Een Common Data Service-omgeving ontkoppelen en een andere omgeving uit een Finance and Operations-app koppelen</span><span class="sxs-lookup"><span data-stu-id="cb031-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="cb031-156">**Vereiste referenties om de omgeving te ontkoppelen:** Azure AD-tenantbeheerder</span><span class="sxs-lookup"><span data-stu-id="cb031-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="cb031-157">Meld u aan bij de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="cb031-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="cb031-158">Ga naar **Werkruimten \> Gegevensbeheer** en selecteer de tegel **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="cb031-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="cb031-159">Selecteer alle actieve toewijzingen en vervolgens **Stoppen**.</span><span class="sxs-lookup"><span data-stu-id="cb031-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="cb031-160">Selecteer **Koppeling met omgeving verbreken**.</span><span class="sxs-lookup"><span data-stu-id="cb031-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="cb031-161">Selecteer **Ja** om de bewerking te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="cb031-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="cb031-162">U kunt nu een nieuwe omgeving koppelen.</span><span class="sxs-lookup"><span data-stu-id="cb031-162">You can now link a new environment.</span></span>
