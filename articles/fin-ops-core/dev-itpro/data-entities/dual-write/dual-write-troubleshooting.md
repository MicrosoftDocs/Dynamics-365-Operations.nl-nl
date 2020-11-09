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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c3352afd93dfc7c37a8af9dabaf85b7a1debad30
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997249"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="5a713-103">Algemene problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="5a713-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="5a713-104">Dit onderwerp bevat informatie voor het oplossen van algemene problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="5a713-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a713-105">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="5a713-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="5a713-106">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="5a713-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="5a713-107">Wanneer u het pakket voor twee keer wegschrijven probeert te installeren met het hulpprogramma Package Deployer, worden er geen beschikbare oplossingen weergegeven</span><span class="sxs-lookup"><span data-stu-id="5a713-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="5a713-108">Sommige versies van het hulpprogramma Package Deployer zijn niet compatibel met het oplossingspakket voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="5a713-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="5a713-109">Als u het pakket wilt installeren, moet u [versie 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) of hoger van het hulpprogramma Package Deployer gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5a713-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="5a713-110">Nadat u het hulpprogramma Package Deployer hebt geïnstalleerd, installeert u het oplossingspakket door de volgende stappen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="5a713-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="5a713-111">Download het meest recente bestand met het oplossingspakket van Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="5a713-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="5a713-112">Nadat het zipbestand met het pakket is gedownload, klikt u erop met de rechtermuisknop en selecteert u **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="5a713-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="5a713-113">Schakel het selectievakje **Deblokkeren** in en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="5a713-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="5a713-114">Als het selectievakje **Deblokkeren** niet wordt weergeven, is het zipbestand al gedeblokkeerd en kunt u deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="5a713-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialoogvenster Eigenschappen](media/unblock_option.png)

2. <span data-ttu-id="5a713-116">Pak het zipbestand uit en kopieer alle bestanden in de map **Dynamics365FinanceAndOperationsCommon. PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="5a713-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Inhoud van de map Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="5a713-118">Plak alle gekopieerde bestanden in de map **Tools** van het hulpprogramma Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="5a713-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="5a713-119">Voer **PackageDeployer.exe** uit om de Common Data Service-omgeving te selecteren en de oplossingen te installeren.</span><span class="sxs-lookup"><span data-stu-id="5a713-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Inhoud van de map Tools](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="5a713-121">Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Common Data Service om foutdetails weer te geven</span><span class="sxs-lookup"><span data-stu-id="5a713-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="5a713-122">**Vereiste rol om het traceerlogboek in te schakelen en fouten weer te geven:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="5a713-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="5a713-123">Voer de volgende stappen uit om het traceerlogboek in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="5a713-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="5a713-124">Meld u aan bij de modelgestuurde-app in Dynamics 365, open de pagina **Instellingen** en selecteer vervolgens onder **Systeem** de optie **Beheer**.</span><span class="sxs-lookup"><span data-stu-id="5a713-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System** , select **Administration**.</span></span>
2. <span data-ttu-id="5a713-125">Selecteer op de pagina **Beheer** de optie **Systeeminstellingen**.</span><span class="sxs-lookup"><span data-stu-id="5a713-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="5a713-126">Ga naar het tabblad **Aanpassen** en selecteer in het veld **Traceren van invoegtoepassing en aangepaste werkstroomactiviteit** **Alle** om het traceerlogboek voor invoegtoepassingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="5a713-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="5a713-127">Als u traceerlogboeken alleen wilt vastleggen wanneer er uitzonderingen optreden, kunt u in plaats daarvan **Uitzondering** selecteren.</span><span class="sxs-lookup"><span data-stu-id="5a713-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="5a713-128">Voer de volgende stappen uit om het traceerlogboek weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5a713-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="5a713-129">Meld u aan bij de modelgestuurde-app in Dynamics 365, open de pagina **Instellingen** en selecteer vervolgens onder **Systeem** de optie **Traceerlogboek invoegtoepassing**.</span><span class="sxs-lookup"><span data-stu-id="5a713-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization** , select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="5a713-130">Zoek de traceerlogboeken waarvoor het veld **Type naam** is ingesteld op **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="5a713-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="5a713-131">Dubbelklik op een item om het volledige logboek weer te geven en controleer vervolgens op het sneltabblad **Uitvoering** de tekst **Bericht blokkeren**.</span><span class="sxs-lookup"><span data-stu-id="5a713-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="5a713-132">De modus Foutopsporing inschakelen om live synchronisatieproblemen in Finance and Operations-apps op te lossen</span><span class="sxs-lookup"><span data-stu-id="5a713-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="5a713-133">**Vereiste rol om de fouten weer te geven** : fouten van systeembeheerder met Twee keer wegschrijven die zijn ontstaan in Common Data Service, kunnen worden weergegeven in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="5a713-133">**Required role to view the errors:** System admin Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="5a713-134">In sommige gevallen is de volledige tekst van het foutbericht niet beschikbaar omdat het bericht te lang is of persoonlijke identificatie gegevens (PII) bevat.</span><span class="sxs-lookup"><span data-stu-id="5a713-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="5a713-135">U kunt uitgebreide logboekregistratie voor fouten inschakelen door de volgende stappen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="5a713-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="5a713-136">Alle projectconfiguraties in Finance and Operations-apps hebben een eigenschap **IsDebugMode** in de entiteit **DualWriteprojectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5a713-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="5a713-137">Open de entiteit **DualWriteProjectConfiguration** met de Excel-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="5a713-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="5a713-138">Een eenvoudige manier om de entiteit te openen is om de **ontwerp** modus in de Excel-invoegtoepassing in te schakelen en vervolgens **DualWriteprojectConfigurationEntity** toe te voegen aan het werkblad.</span><span class="sxs-lookup"><span data-stu-id="5a713-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="5a713-139">zie [Entiteitsgegevens in Excel openen en bijwerken via de Excel-invoegtoepassing](../../office-integration/use-excel-add-in.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5a713-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="5a713-140">Stel de eigenschap **IsDebugMode** in op **Ja** voor het project.</span><span class="sxs-lookup"><span data-stu-id="5a713-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="5a713-141">Voer het scenario uit dat fouten genereert.</span><span class="sxs-lookup"><span data-stu-id="5a713-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="5a713-142">De uitgebreide logboeken zijn beschikbaar in de tabel DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="5a713-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="5a713-143">Als u gegevens wilt opzoeken in de tabelbrowser, gebruikt u de volgende URL (vervang **XXX** waar van toepassing):</span><span class="sxs-lookup"><span data-stu-id="5a713-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="5a713-144">Synchronisatiefouten controleren op de virtuele machine voor de Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="5a713-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="5a713-145">**Vereiste rol om de fouten weer te geven:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="5a713-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="5a713-146">Meld u aan bij Microsoft Dynamics LCS (LifeCycle Services).</span><span class="sxs-lookup"><span data-stu-id="5a713-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="5a713-147">Open het LCS-project dat u hebt gekozen voor tests met twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="5a713-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="5a713-148">Selecteer de tegel **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="5a713-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="5a713-149">Gebruik extern bureaublad om u aan te melden bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="5a713-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="5a713-150">Gebruik het lokale account dat wordt weergegeven in LCS.</span><span class="sxs-lookup"><span data-stu-id="5a713-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="5a713-151">Open Logboeken.</span><span class="sxs-lookup"><span data-stu-id="5a713-151">Open Event viewer.</span></span>
6. <span data-ttu-id="5a713-152">Selecteer **Logboeken Toepassingen en Services \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationeel**.</span><span class="sxs-lookup"><span data-stu-id="5a713-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="5a713-153">Bekijk de lijst met recente fouten.</span><span class="sxs-lookup"><span data-stu-id="5a713-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="5a713-154">Een Common Data Service-omgeving ontkoppelen en een andere omgeving uit een Finance and Operations-app koppelen</span><span class="sxs-lookup"><span data-stu-id="5a713-154">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="5a713-155">**De vereiste rol om de omgeving te ontkoppelen:** systeembeheerder voor de Finance and Operations-app of Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="5a713-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Common Data Service.</span></span>

1. <span data-ttu-id="5a713-156">Meld u aan bij de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="5a713-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="5a713-157">Ga naar **Werkruimten \> Gegevensbeheer** en selecteer de tegel **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="5a713-157">Go to **Workspaces \> Data management** , and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="5a713-158">Selecteer alle actieve toewijzingen en vervolgens **Stoppen**.</span><span class="sxs-lookup"><span data-stu-id="5a713-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="5a713-159">Selecteer **Koppeling met omgeving verbreken**.</span><span class="sxs-lookup"><span data-stu-id="5a713-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="5a713-160">Selecteer **Ja** om de bewerking te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="5a713-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="5a713-161">U kunt nu een nieuwe omgeving koppelen.</span><span class="sxs-lookup"><span data-stu-id="5a713-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="5a713-162">Informatieformulier met verkooporderregel kan niet worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="5a713-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="5a713-163">Wanneer u een verkooporder maakt in Dynamics 365 Sales, kunt u door te klikken op **+ Producten toevoegen** worden omgeleid naar het formulier Dynamics 365 Project Operations-orderregel.</span><span class="sxs-lookup"><span data-stu-id="5a713-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="5a713-164">U kunt vanuit dat formulier niet het **informatieformulier** over de verkooporderregel weergeven.</span><span class="sxs-lookup"><span data-stu-id="5a713-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="5a713-165">De optie voor **informatie** wordt niet weergegeven in de vervolgkeuzelijst onder **Nieuwe orderregel**.</span><span class="sxs-lookup"><span data-stu-id="5a713-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="5a713-166">Dit gebeurt omdat Project Operations in uw omgeving is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="5a713-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="5a713-167">Ga als volgt te werk om de optie voor het formulier **Informatie** opnieuw in te schakelen:</span><span class="sxs-lookup"><span data-stu-id="5a713-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="5a713-168">Ga naar de entiteit **Orderregel**.</span><span class="sxs-lookup"><span data-stu-id="5a713-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="5a713-169">Zoek het formulier **Informatie** onder het knooppunt met formulieren.</span><span class="sxs-lookup"><span data-stu-id="5a713-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="5a713-170">Selecteer het formulier **Informatie** en klik op **Beveiligingsrollen inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="5a713-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="5a713-171">Wijzig de beveiligingsinstelling in **Weergeven aan iedereen**.</span><span class="sxs-lookup"><span data-stu-id="5a713-171">Change the security setting to **Display to everyone**.</span></span>
