---
title: Een exemplaar kopiëren
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008572"
---
# <a name="copy-an-instance"></a><span data-ttu-id="05dc1-102">Een exemplaar kopiëren</span><span class="sxs-lookup"><span data-stu-id="05dc1-102">Copy an instance</span></span>

<span data-ttu-id="05dc1-103">U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="05dc1-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="05dc1-104">Als u nog een sandbox-omgeving hebt, kunt u de database ook vanuit die omgeving kopiëren naar een specifieke sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="05dc1-105">Voor het kopiëren van een exemplaar moet u het volgende controleren:</span><span class="sxs-lookup"><span data-stu-id="05dc1-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="05dc1-106">Het Human Resources-exemplaar dat u wilt overschrijven, moet een sandbox-omgeving zijn.</span><span class="sxs-lookup"><span data-stu-id="05dc1-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="05dc1-107">De omgevingen die u kopieert, moeten zich in dezelfde regio bevinden.</span><span class="sxs-lookup"><span data-stu-id="05dc1-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="05dc1-108">U kunt niet kopiëren van de ene naar de andere omgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-108">You can't copy across regions.</span></span>

- <span data-ttu-id="05dc1-109">U moet een beheerder zijn in de doelomgeving, zodat u zich kunt aanmelden nadat u het exemplaar hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="05dc1-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="05dc1-110">Wanneer u de Human Resources-database kopieert, kopieert u niet de elementen (apps of gegevens) die zijn opgenomen in een Microsoft PowerApps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="05dc1-111">Zie [Een omgeving kopiëren](https://docs.microsoft.com/power-platform/admin/copy-environment) voor informatie over het kopiëren van elementen in een PowerApps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="05dc1-112">De PowerApps-omgeving die u wilt overschrijven, moet een sandbox-omgeving zijn.</span><span class="sxs-lookup"><span data-stu-id="05dc1-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="05dc1-113">U moet een globale tenantbeheerder zijn om een PowerApps-productieomgeving te wijzigen in een sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="05dc1-114">Zie [Schakelen tussen exemplaren](https://docs.microsoft.com/dynamics365/admin/switch-instance) voor meer informatie over het wijzigen van een PowerApps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="05dc1-115">De gevolgen van het kopiëren van een Human Resources-database</span><span class="sxs-lookup"><span data-stu-id="05dc1-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="05dc1-116">De volgende gebeurtenissen treden op wanneer u een Human Resources-database kopieert:</span><span class="sxs-lookup"><span data-stu-id="05dc1-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="05dc1-117">Tijdens het kopiëren wordt de bestaande database in de doelomgeving gewist.</span><span class="sxs-lookup"><span data-stu-id="05dc1-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="05dc1-118">Nadat het kopieerproces is voltooid, kunt u de bestaande database niet herstellen.</span><span class="sxs-lookup"><span data-stu-id="05dc1-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="05dc1-119">De doelomgeving is pas weer beschikbaar als de kopieerbewerking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="05dc1-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="05dc1-120">Documenten in de Microsoft Azure Blob-opslag worden niet van de ene omgeving naar de andere gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="05dc1-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="05dc1-121">Daarom worden documenten en sjablonen die zijn gekoppeld, niet gekopieerd en blijven deze in de bronomgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="05dc1-122">Alle gebruikers behalve de gebruiker met beheerdersrechten en andere interne servicegebruikersaccounts worden uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="05dc1-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="05dc1-123">De gebruiker met beheerdersrechten kan de gegevens dus verwijderen of onleesbaar maken voordat andere gebruikers weer toegang hebben tot het systeem.</span><span class="sxs-lookup"><span data-stu-id="05dc1-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="05dc1-124">De gebruiker met beheerdersrechten moet de vereiste configuratiewijzigingen aanbrengen, zoals het opnieuw verbinden van integratie-eindpunten met specifieke services of URL's.</span><span class="sxs-lookup"><span data-stu-id="05dc1-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="05dc1-125">De Human Resources-database kopiëren</span><span class="sxs-lookup"><span data-stu-id="05dc1-125">Copy the Human Resources database</span></span>

<span data-ttu-id="05dc1-126">Als u deze taak wilt voltooien, kopieert u eerst een exemplaar en meldt u zich vervolgens aan bij het Microsoft Power Platform-beheercentrum om uw PowerApps-omgeving te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="05dc1-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="05dc1-127">Wanneer u een exemplaar kopieert, wordt de database gewist in het doelexemplaar.</span><span class="sxs-lookup"><span data-stu-id="05dc1-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="05dc1-128">Het doelexemplaar is niet beschikbaar tijdens dit proces.</span><span class="sxs-lookup"><span data-stu-id="05dc1-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="05dc1-129">Meld u aan bij LCS en selecteer het LCS-project met het exemplaar dat u wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="05dc1-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="05dc1-130">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="05dc1-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="05dc1-131">Selecteer het exemplaar dat u wilt kopiëren en selecteer **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="05dc1-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="05dc1-132">Selecteer in het taak venster **Een exemplaar kopiëren** het exemplaar dat u wilt overschrijven en selecteer vervolgens **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="05dc1-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="05dc1-133">Wacht totdat de waarde in het veld **Kopieerstatus** is bijgewerkt naar **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="05dc1-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="05dc1-134">Selecteer het exemplaar dat u wilt overschrijven</span><span class="sxs-lookup"><span data-stu-id="05dc1-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="05dc1-135">Selecteer **Power Platform** en meld u aan bij het Microsoft Power Platform-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="05dc1-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="05dc1-136">Selecteer Power Platform</span><span class="sxs-lookup"><span data-stu-id="05dc1-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="05dc1-137">Selecteer de PowerApps-omgeving die u wilt kopiëren en selecteer vervolgens **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="05dc1-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="05dc1-138">Wanneer het kopieerproces is voltooid, meldt u zich aan bij het doelexemplaar en schakelt u Common Data Service-integratie in.</span><span class="sxs-lookup"><span data-stu-id="05dc1-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="05dc1-139">Zie voor meer informatie en instructies [Common Data Service-integratie configureren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="05dc1-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="05dc1-140">Gegevenselementen en statussen</span><span class="sxs-lookup"><span data-stu-id="05dc1-140">Data elements and statuses</span></span>

<span data-ttu-id="05dc1-141">De volgende gegevenselementen worden niet gekopieerd wanneer u een Human Resources-exemplaar kopieert:</span><span class="sxs-lookup"><span data-stu-id="05dc1-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="05dc1-142">E-mailadressen in de tabel **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="05dc1-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="05dc1-143">De batchtaakhistorie in de tabellen **BatchJobHistory**, **BatchHistory** en **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="05dc1-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="05dc1-144">Het SMTP-wachtwoord (Simple Mail Transfer Protocol) in de tabel **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="05dc1-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="05dc1-145">De SMTP-relayserver in de tabel **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="05dc1-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="05dc1-146">Afdrukbeheerinstellingen in de tabellen **PrintMgmtSettings** en **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="05dc1-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="05dc1-147">Omgevingsspecifieke records in de tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** en **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="05dc1-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="05dc1-148">Documentbijlagen in de tabel DocuValue.</span><span class="sxs-lookup"><span data-stu-id="05dc1-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="05dc1-149">Deze bijlagen bevatten Microsoft Office-sjablonen die in de bronomgeving zijn overschreven.</span><span class="sxs-lookup"><span data-stu-id="05dc1-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="05dc1-150">De verbindingsreeks in de tabel **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="05dc1-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="05dc1-151">Sommige van deze elementen worden niet gekopieerd omdat ze omgevingsspecifiek zijn.</span><span class="sxs-lookup"><span data-stu-id="05dc1-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="05dc1-152">Voorbeelden zijn de **BatchServerConfig**- en **SysCorpNetPrinters**-records.</span><span class="sxs-lookup"><span data-stu-id="05dc1-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="05dc1-153">Andere elementen worden niet gekopieerd vanwege het volume van de ondersteuningstickets.</span><span class="sxs-lookup"><span data-stu-id="05dc1-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="05dc1-154">Er kunnen bijvoorbeeld dubbele e-mailberichten worden verzonden omdat SMTP nog steeds is ingeschakeld in de omgeving voor acceptatietests voor gebruikers (sandbox-omgeving), er kunnen ongeldige integratieberichten worden verzonden omdat batchtaken nog steeds zijn ingeschakeld en er kunnen gebruikers worden ingeschakeld voordat beheerders opruimacties na vernieuwing kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="05dc1-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="05dc1-155">Bovendien worden de volgende statuswaarden gewijzigd wanneer u een exemplaar kopieert:</span><span class="sxs-lookup"><span data-stu-id="05dc1-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="05dc1-156">Alle gebruikers behalve de beheerder worden ingesteld op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="05dc1-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="05dc1-157">Alle batchtaken, met uitzondering van bepaalde systeemtaken, worden ingesteld op **Inhouden**.</span><span class="sxs-lookup"><span data-stu-id="05dc1-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="05dc1-158">Omgevingsbeheerder</span><span class="sxs-lookup"><span data-stu-id="05dc1-158">Environment admin</span></span>

<span data-ttu-id="05dc1-159">Alle gebruikers in de sandbox-doelomgeving, inclusief beheerders, worden vervangen door de gebruikers van de bronomgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="05dc1-160">Voordat u een exemplaar kopieert, moet u controleren of u een beheerder bent in de doelomgeving.</span><span class="sxs-lookup"><span data-stu-id="05dc1-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="05dc1-161">Als u dat niet bent, kunt u zich niet aanmelden bij de sandbox-doelomgeving nadat de kopie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="05dc1-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="05dc1-162">Alle gebruikers die geen beheerder zijn in de sandbox-doelomgeving, zijn uitgeschakeld om ongewenste aanmeldingen in de sandbox-omgeving te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="05dc1-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="05dc1-163">Beheerders kunnen gebruikers zo nodig opnieuw inschakelen.</span><span class="sxs-lookup"><span data-stu-id="05dc1-163">Administrators can reenable users if needed.</span></span>
