---
title: Een exemplaar kopiëren
description: U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: b14baf49517f5d606038af20366944788b22eba2
ms.sourcegitcommit: 1ec931f8fe86bde27f6def36ea214a2a05fb22f6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2020
ms.locfileid: "3554320"
---
# <a name="copy-an-instance"></a><span data-ttu-id="ed196-103">Een exemplaar kopiëren</span><span class="sxs-lookup"><span data-stu-id="ed196-103">Copy an instance</span></span>

<span data-ttu-id="ed196-104">U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="ed196-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="ed196-105">Als u nog een sandbox-omgeving hebt, kunt u de database ook vanuit die omgeving kopiëren naar een specifieke sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="ed196-106">Voor het kopiëren van een exemplaar moet u het volgende controleren:</span><span class="sxs-lookup"><span data-stu-id="ed196-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="ed196-107">Het Human Resources-exemplaar dat u wilt overschrijven, moet een sandbox-omgeving zijn.</span><span class="sxs-lookup"><span data-stu-id="ed196-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="ed196-108">De omgevingen die u kopieert, moeten zich in dezelfde regio bevinden.</span><span class="sxs-lookup"><span data-stu-id="ed196-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="ed196-109">U kunt niet kopiëren van de ene naar de andere omgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-109">You can't copy across regions.</span></span>

- <span data-ttu-id="ed196-110">U moet een beheerder zijn in de doelomgeving, zodat u zich kunt aanmelden nadat u het exemplaar hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="ed196-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="ed196-111">Wanneer u de Human Resources-database kopieert, kopieert u niet de elementen (apps of gegevens) die zijn opgenomen in een Microsoft PowerApps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="ed196-112">Zie [Een omgeving kopiëren](https://docs.microsoft.com/power-platform/admin/copy-environment) voor informatie over het kopiëren van elementen in een PowerApps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="ed196-113">De PowerApps-omgeving die u wilt overschrijven, moet een sandbox-omgeving zijn.</span><span class="sxs-lookup"><span data-stu-id="ed196-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="ed196-114">U moet een globale tenantbeheerder zijn om een PowerApps-productieomgeving te wijzigen in een sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="ed196-115">Zie [Schakelen tussen exemplaren](https://docs.microsoft.com/dynamics365/admin/switch-instance) voor meer informatie over het wijzigen van een PowerApps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="ed196-116">De gevolgen van het kopiëren van een Human Resources-database</span><span class="sxs-lookup"><span data-stu-id="ed196-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="ed196-117">De volgende gebeurtenissen treden op wanneer u een Human Resources-database kopieert:</span><span class="sxs-lookup"><span data-stu-id="ed196-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="ed196-118">Tijdens het kopiëren wordt de bestaande database in de doelomgeving gewist.</span><span class="sxs-lookup"><span data-stu-id="ed196-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="ed196-119">Nadat het kopieerproces is voltooid, kunt u de bestaande database niet herstellen.</span><span class="sxs-lookup"><span data-stu-id="ed196-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="ed196-120">De doelomgeving is pas weer beschikbaar als de kopieerbewerking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ed196-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="ed196-121">Documenten in de Microsoft Azure Blob-opslag worden niet van de ene omgeving naar de andere gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="ed196-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="ed196-122">Daarom worden documenten en sjablonen die zijn gekoppeld, niet gekopieerd en blijven deze in de bronomgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="ed196-123">Alle gebruikers behalve de gebruiker met beheerdersrechten en andere interne servicegebruikersaccounts worden uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ed196-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="ed196-124">De gebruiker met beheerdersrechten kan de gegevens dus verwijderen of onleesbaar maken voordat andere gebruikers weer toegang hebben tot het systeem.</span><span class="sxs-lookup"><span data-stu-id="ed196-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="ed196-125">De gebruiker met beheerdersrechten moet de vereiste configuratiewijzigingen aanbrengen, zoals het opnieuw verbinden van integratie-eindpunten met specifieke services of URL's.</span><span class="sxs-lookup"><span data-stu-id="ed196-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="ed196-126">De Human Resources-database kopiëren</span><span class="sxs-lookup"><span data-stu-id="ed196-126">Copy the Human Resources database</span></span>

<span data-ttu-id="ed196-127">Als u deze taak wilt voltooien, kopieert u eerst een exemplaar en meldt u zich vervolgens aan bij het Microsoft Power Platform-beheercentrum om uw PowerApps-omgeving te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="ed196-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="ed196-128">Wanneer u een exemplaar kopieert, wordt de database gewist in het doelexemplaar.</span><span class="sxs-lookup"><span data-stu-id="ed196-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="ed196-129">Het doelexemplaar is niet beschikbaar tijdens dit proces.</span><span class="sxs-lookup"><span data-stu-id="ed196-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="ed196-130">Meld u aan bij LCS en selecteer het LCS-project met het exemplaar dat u wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="ed196-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="ed196-131">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="ed196-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="ed196-132">Selecteer het exemplaar dat u wilt kopiëren en selecteer **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="ed196-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="ed196-133">Selecteer in het taak venster **Een exemplaar kopiëren** het exemplaar dat u wilt overschrijven en selecteer vervolgens **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="ed196-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="ed196-134">Wacht totdat de waarde in het veld **Kopieerstatus** is bijgewerkt naar **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="ed196-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="ed196-135">Selecteer het exemplaar dat u wilt overschrijven</span><span class="sxs-lookup"><span data-stu-id="ed196-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="ed196-136">Selecteer **Power Platform** en meld u aan bij het Microsoft Power Platform-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="ed196-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="ed196-137">Selecteer Power Platform</span><span class="sxs-lookup"><span data-stu-id="ed196-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="ed196-138">Selecteer de PowerApps-omgeving die u wilt kopiëren en selecteer vervolgens **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="ed196-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="ed196-139">Wanneer het kopieerproces is voltooid, meldt u zich aan bij het doelexemplaar en schakelt u Common Data Service-integratie in.</span><span class="sxs-lookup"><span data-stu-id="ed196-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="ed196-140">Zie voor meer informatie en instructies [Common Data Service-integratie configureren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="ed196-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="ed196-141">Gegevenselementen en statussen</span><span class="sxs-lookup"><span data-stu-id="ed196-141">Data elements and statuses</span></span>

<span data-ttu-id="ed196-142">De volgende gegevenselementen worden niet gekopieerd wanneer u een Human Resources-exemplaar kopieert:</span><span class="sxs-lookup"><span data-stu-id="ed196-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="ed196-143">E-mailadressen in de tabel **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="ed196-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="ed196-144">De batchtaakhistorie in de tabellen **BatchJobHistory**, **BatchHistory** en **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="ed196-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="ed196-145">Het SMTP-wachtwoord (Simple Mail Transfer Protocol) in de tabel **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="ed196-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="ed196-146">De SMTP-relayserver in de tabel **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="ed196-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="ed196-147">Afdrukbeheerinstellingen in de tabellen **PrintMgmtSettings** en **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="ed196-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="ed196-148">Omgevingsspecifieke records in de tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** en **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="ed196-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="ed196-149">Documentbijlagen in de tabel DocuValue.</span><span class="sxs-lookup"><span data-stu-id="ed196-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="ed196-150">Deze bijlagen bevatten Microsoft Office-sjablonen die in de bronomgeving zijn overschreven.</span><span class="sxs-lookup"><span data-stu-id="ed196-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="ed196-151">De verbindingsreeks in de tabel **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="ed196-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="ed196-152">Sommige van deze elementen worden niet gekopieerd omdat ze omgevingsspecifiek zijn.</span><span class="sxs-lookup"><span data-stu-id="ed196-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="ed196-153">Voorbeelden zijn de **BatchServerConfig**- en **SysCorpNetPrinters**-records.</span><span class="sxs-lookup"><span data-stu-id="ed196-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="ed196-154">Andere elementen worden niet gekopieerd vanwege het volume van de ondersteuningstickets.</span><span class="sxs-lookup"><span data-stu-id="ed196-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="ed196-155">Er kunnen bijvoorbeeld dubbele e-mailberichten worden verzonden omdat SMTP nog steeds is ingeschakeld in de omgeving voor acceptatietests voor gebruikers (sandbox-omgeving), er kunnen ongeldige integratieberichten worden verzonden omdat batchtaken nog steeds zijn ingeschakeld en er kunnen gebruikers worden ingeschakeld voordat beheerders opruimacties na vernieuwing kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ed196-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="ed196-156">Bovendien worden de volgende statuswaarden gewijzigd wanneer u een exemplaar kopieert:</span><span class="sxs-lookup"><span data-stu-id="ed196-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="ed196-157">Alle gebruikers behalve de beheerder worden ingesteld op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="ed196-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="ed196-158">Alle batchtaken, met uitzondering van bepaalde systeemtaken, worden ingesteld op **Inhouden**.</span><span class="sxs-lookup"><span data-stu-id="ed196-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="ed196-159">Omgevingsbeheerder</span><span class="sxs-lookup"><span data-stu-id="ed196-159">Environment admin</span></span>

<span data-ttu-id="ed196-160">Alle gebruikers in de sandbox-doelomgeving, inclusief beheerders, worden vervangen door de gebruikers van de bronomgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="ed196-161">Voordat u een exemplaar kopieert, moet u controleren of u een beheerder bent in de bronomgeving.</span><span class="sxs-lookup"><span data-stu-id="ed196-161">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="ed196-162">Als u dat niet bent, kunt u zich niet aanmelden bij de sandbox-doelomgeving nadat de kopie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ed196-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="ed196-163">Alle gebruikers die geen beheerder zijn in de sandbox-doelomgeving, zijn uitgeschakeld om ongewenste aanmeldingen in de sandbox-omgeving te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="ed196-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="ed196-164">Beheerders kunnen gebruikers zo nodig opnieuw inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ed196-164">Administrators can reenable users if needed.</span></span>
