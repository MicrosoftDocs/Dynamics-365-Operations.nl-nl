---
title: Een exemplaar kopiëren
description: U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren.
author: andreabichsel
manager: tfehr
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e38abf3537d88bb147fbf0030999953025e5820f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466899"
---
# <a name="copy-an-instance"></a><span data-ttu-id="091e8-103">Een exemplaar kopiëren</span><span class="sxs-lookup"><span data-stu-id="091e8-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="091e8-104">U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="091e8-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="091e8-105">Als u nog een sandbox-omgeving hebt, kunt u de database ook vanuit die omgeving kopiëren naar een specifieke sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="091e8-106">Houd rekening met de volgende tips als u een exemplaar wilt kopiëren:</span><span class="sxs-lookup"><span data-stu-id="091e8-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="091e8-107">Het Human Resources-exemplaar dat u wilt overschrijven, moet een sandbox-omgeving zijn.</span><span class="sxs-lookup"><span data-stu-id="091e8-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="091e8-108">De omgevingen die u kopieert, moeten zich in dezelfde regio bevinden.</span><span class="sxs-lookup"><span data-stu-id="091e8-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="091e8-109">U kunt niet kopiëren van de ene naar de andere omgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-109">You can't copy across regions.</span></span>

- <span data-ttu-id="091e8-110">U moet een beheerder zijn in de doelomgeving, zodat u zich kunt aanmelden nadat u het exemplaar hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="091e8-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="091e8-111">Wanneer u de Human Resources-database kopieert, kopieert u niet de elementen (apps of gegevens) die zijn opgenomen in een Microsoft Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="091e8-112">Zie [Een omgeving kopiëren](https://docs.microsoft.com/power-platform/admin/copy-environment) voor informatie over het kopiëren van elementen in een Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="091e8-113">De Power Apps-omgeving die u wilt overschrijven, moet een sandbox-omgeving zijn.</span><span class="sxs-lookup"><span data-stu-id="091e8-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="091e8-114">U moet een globale tenantbeheerder zijn om een Power Apps-productieomgeving te wijzigen in een sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="091e8-115">Zie [Schakelen tussen exemplaren](https://docs.microsoft.com/dynamics365/admin/switch-instance) voor meer informatie over het wijzigen van een Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="091e8-116">Als u een exemplaar in uw sandbox-omgeving kopieert en u de sandbox-omgeving wilt integreren met Dataverse, moet u aangepaste velden opnieuw toepassen op Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="091e8-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="091e8-117">Zie [Aangepaste velden toepassen op Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="091e8-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="091e8-118">De gevolgen van het kopiëren van een Human Resources-database</span><span class="sxs-lookup"><span data-stu-id="091e8-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="091e8-119">De volgende gebeurtenissen treden op wanneer u een Human Resources-database kopieert:</span><span class="sxs-lookup"><span data-stu-id="091e8-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="091e8-120">Tijdens het kopiëren wordt de bestaande database in de doelomgeving gewist.</span><span class="sxs-lookup"><span data-stu-id="091e8-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="091e8-121">Nadat het kopieerproces is voltooid, kunt u de bestaande database niet herstellen.</span><span class="sxs-lookup"><span data-stu-id="091e8-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="091e8-122">De doelomgeving is pas weer beschikbaar als de kopieerbewerking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="091e8-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="091e8-123">Documenten in de Microsoft Azure Blob-opslag worden niet van de ene omgeving naar de andere gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="091e8-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="091e8-124">Het resultaat is dat documenten en sjablonen die zijn gekoppeld, niet worden gekopieerd en in de bronomgeving blijven staan.</span><span class="sxs-lookup"><span data-stu-id="091e8-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="091e8-125">Alle gebruikers behalve de gebruiker met beheerdersrechten en andere interne servicegebruikersaccounts worden uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="091e8-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="091e8-126">De gebruiker met beheerdersrechten kan de gegevens verwijderen of onleesbaar maken voordat andere gebruikers weer toegang hebben tot het systeem.</span><span class="sxs-lookup"><span data-stu-id="091e8-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="091e8-127">De gebruiker met beheerdersrechten moet de vereiste configuratiewijzigingen aanbrengen, zoals het opnieuw verbinden van integratie-eindpunten met specifieke services of URL's.</span><span class="sxs-lookup"><span data-stu-id="091e8-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="091e8-128">De Human Resources-database kopiëren</span><span class="sxs-lookup"><span data-stu-id="091e8-128">Copy the Human Resources database</span></span>

<span data-ttu-id="091e8-129">Als u deze taak wilt voltooien, kopieert u eerst een exemplaar en meldt u zich vervolgens aan bij het Microsoft Power Platform-beheercentrum om uw Power Apps-omgeving te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="091e8-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="091e8-130">Wanneer u een exemplaar kopieert, wordt de database gewist in het doelexemplaar.</span><span class="sxs-lookup"><span data-stu-id="091e8-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="091e8-131">Het doelexemplaar is niet beschikbaar tijdens dit proces.</span><span class="sxs-lookup"><span data-stu-id="091e8-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="091e8-132">Meld u aan bij LCS en selecteer het LCS-project met het exemplaar dat u wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="091e8-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="091e8-133">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="091e8-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="091e8-134">Selecteer het exemplaar dat u wilt kopiëren en selecteer **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="091e8-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="091e8-135">Selecteer in het taak venster **Een exemplaar kopiëren** het exemplaar dat u wilt overschrijven en selecteer vervolgens **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="091e8-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="091e8-136">Wacht totdat de waarde in het veld **Kopieerstatus** is bijgewerkt naar **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="091e8-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="091e8-137">Selecteer het exemplaar dat u wilt overschrijven</span><span class="sxs-lookup"><span data-stu-id="091e8-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="091e8-138">Selecteer **Power Platform** en meld u aan bij het Microsoft Power Platform-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="091e8-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="091e8-139">Selecteer Power Platform</span><span class="sxs-lookup"><span data-stu-id="091e8-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="091e8-140">Selecteer de Power Apps-omgeving die u wilt kopiëren en selecteer vervolgens **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="091e8-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="091e8-141">Wanneer het kopieerproces is voltooid, meldt u zich aan bij het doelexemplaar en schakelt u Dataverse-integratie in.</span><span class="sxs-lookup"><span data-stu-id="091e8-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="091e8-142">Zie voor meer informatie en instructies [Dataverse-integratie configureren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="091e8-142">For more information and instructions, see [Configure Dataverse integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="091e8-143">Gegevenselementen en statussen</span><span class="sxs-lookup"><span data-stu-id="091e8-143">Data elements and statuses</span></span>

<span data-ttu-id="091e8-144">De volgende gegevenselementen worden niet gekopieerd wanneer u een Human Resources-exemplaar kopieert:</span><span class="sxs-lookup"><span data-stu-id="091e8-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="091e8-145">E-mailadressen in de tabel **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="091e8-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="091e8-146">De batchtaakhistorie in de tabellen **BatchJobHistory**, **BatchHistory** en **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="091e8-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="091e8-147">Het SMTP-wachtwoord (Simple Mail Transfer Protocol) in de tabel **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="091e8-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="091e8-148">De SMTP-relayserver in de tabel **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="091e8-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="091e8-149">Afdrukbeheerinstellingen in de tabellen **PrintMgmtSettings** en **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="091e8-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="091e8-150">Omgevingsspecifieke records in de tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** en **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="091e8-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="091e8-151">Documentbijlagen in de tabel DocuValue.</span><span class="sxs-lookup"><span data-stu-id="091e8-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="091e8-152">Deze bijlagen bevatten Microsoft Office-sjablonen die in de bronomgeving zijn overschreven.</span><span class="sxs-lookup"><span data-stu-id="091e8-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="091e8-153">De verbindingsreeks in de tabel **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="091e8-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="091e8-154">Sommige van deze elementen worden niet gekopieerd omdat ze specifiek zijn voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="091e8-155">Voorbeelden zijn de **BatchServerConfig**- en **SysCorpNetPrinters**-records.</span><span class="sxs-lookup"><span data-stu-id="091e8-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="091e8-156">Andere elementen worden niet gekopieerd vanwege het volume van de ondersteuningstickets.</span><span class="sxs-lookup"><span data-stu-id="091e8-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="091e8-157">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="091e8-157">For example:</span></span>

- <span data-ttu-id="091e8-158">Er kunnen dubbele e-mails worden verzonden omdat SMTP nog steeds is ingeschakeld in de omgeving voor acceptatietests voor gebruikers (sandbox).</span><span class="sxs-lookup"><span data-stu-id="091e8-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="091e8-159">Er worden mogelijk berichten over een ongeldige integratie verzonden omdat batchtaken nog steeds zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="091e8-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="091e8-160">Gebruikers kunnen zijn ingeschakeld voordat beheerders de opruimacties na vernieuwen kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="091e8-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="091e8-161">Bovendien worden de volgende statuswaarden gewijzigd wanneer u een exemplaar kopieert:</span><span class="sxs-lookup"><span data-stu-id="091e8-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="091e8-162">Alle gebruikers behalve de beheerder worden ingesteld op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="091e8-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="091e8-163">Alle batchtaken, met uitzondering van bepaalde systeemtaken, worden ingesteld op **Inhouden**.</span><span class="sxs-lookup"><span data-stu-id="091e8-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="091e8-164">Omgevingsbeheerder</span><span class="sxs-lookup"><span data-stu-id="091e8-164">Environment admin</span></span>

<span data-ttu-id="091e8-165">Alle gebruikers in de sandbox-doelomgeving, inclusief beheerders, worden vervangen door de gebruikers van de bronomgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="091e8-166">Voordat u een exemplaar kopieert, moet u controleren of u een beheerder bent in de bronomgeving.</span><span class="sxs-lookup"><span data-stu-id="091e8-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="091e8-167">Als u nog niet bij de sandbox-doelomgeving bent aangemeld, kunt u dat doen nadat de kopie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="091e8-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="091e8-168">Alle gebruikers die geen beheerder zijn in de sandbox-doelomgeving, zijn uitgeschakeld om ongewenste aanmeldingen in de sandbox-omgeving te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="091e8-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="091e8-169">Beheerders kunnen gebruikers zo nodig opnieuw inschakelen.</span><span class="sxs-lookup"><span data-stu-id="091e8-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="091e8-170">Aangepaste velden toepassen op Dataverse</span><span class="sxs-lookup"><span data-stu-id="091e8-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="091e8-171">Als u een exemplaar in uw sandbox-omgeving kopieert en u de sandbox-omgeving wilt integreren met Dataverse, moet u aangepaste velden opnieuw toepassen op Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="091e8-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="091e8-172">Voer de volgende stappen uit voor elk aangepast veld dat wordt weergegeven in Dataverse-tabellen:</span><span class="sxs-lookup"><span data-stu-id="091e8-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="091e8-173">Ga naar het aangepaste veld en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="091e8-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="091e8-174">Schakel het selectievakje **Ingeschakeld** uit voor elke cdm_\*-entiteit waarvoor het aangepaste veld is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="091e8-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="091e8-175">Selecteer **Wijzigingen toepassen**.</span><span class="sxs-lookup"><span data-stu-id="091e8-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="091e8-176">Selecteer opnieuw **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="091e8-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="091e8-177">Schakel het selectievakje **Ingeschakeld** in voor elke cdm_\*-entiteit waarvoor het aangepaste veld is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="091e8-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="091e8-178">Selecteer opnieuw **Wijzigingen toepassen**.</span><span class="sxs-lookup"><span data-stu-id="091e8-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="091e8-179">Door het proces van uitschakelen, wijzigingen toepassen, opnieuw inschakelen en wijzigingen weer toepassen, wordt het schema in Dataverse bijgewerkt met de aangepaste velden.</span><span class="sxs-lookup"><span data-stu-id="091e8-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="091e8-180">Meer informatie over aangepaste velden vindt u in [Aangepaste velden maken en gebruiken](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="091e8-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="091e8-181">Zie ook</span><span class="sxs-lookup"><span data-stu-id="091e8-181">See also</span></span>

[<span data-ttu-id="091e8-182">Human resources inrichten</span><span class="sxs-lookup"><span data-stu-id="091e8-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="091e8-183">Een exemplaar verwijderen</span><span class="sxs-lookup"><span data-stu-id="091e8-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="091e8-184">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="091e8-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]