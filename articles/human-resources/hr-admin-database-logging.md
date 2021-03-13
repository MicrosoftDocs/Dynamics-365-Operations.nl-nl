---
title: Databaselogboeken configureren en beheren
description: U kunt wijzigingen in tabellen en velden in Dynamics 365 Human Resources bijhouden met databaselogboeken.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50346cc495fe08f49137dba59dbcbb3f7f838c7b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129274"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="503bd-103">Databaselogboeken configureren en beheren</span><span class="sxs-lookup"><span data-stu-id="503bd-103">Configure and manage database logging</span></span>

<span data-ttu-id="503bd-104">U kunt wijzigingen in tabellen en velden in Dynamics 365 Human Resources bijhouden met databaselogboeken.</span><span class="sxs-lookup"><span data-stu-id="503bd-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="503bd-105">In dit onderwerp komt het volgende aan de orde:</span><span class="sxs-lookup"><span data-stu-id="503bd-105">This topic describes how to:</span></span>

- <span data-ttu-id="503bd-106">Beveiliging en prestaties voor databaselogboeken beheren</span><span class="sxs-lookup"><span data-stu-id="503bd-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="503bd-107">Databaselogboek instellen</span><span class="sxs-lookup"><span data-stu-id="503bd-107">Set up database logging</span></span>
- <span data-ttu-id="503bd-108">Databaselogboeken opschonen</span><span class="sxs-lookup"><span data-stu-id="503bd-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="503bd-109">Overzicht van databaselogboeken</span><span class="sxs-lookup"><span data-stu-id="503bd-109">Overview of database logging</span></span>

<span data-ttu-id="503bd-110">U kunt specifieke wijzigingen in Microsoft Dynamics 365 Human Resources bijhouden met databaselogboeken.</span><span class="sxs-lookup"><span data-stu-id="503bd-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="503bd-111">Deze wijzigingen betreffen onder andere invoegen, bijwerken of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="503bd-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="503bd-112">Met databaselogboeken wordt een record met wijzigingen in tabellen of velden in de databaselogboektabel opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="503bd-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="503bd-113">Zakelijke toepassingen van databaselogboeken zijn onder andere:</span><span class="sxs-lookup"><span data-stu-id="503bd-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="503bd-114">Een controlerecord maken van wijzigingen in specifieke tabellen die gevoelige informatie bevatten.</span><span class="sxs-lookup"><span data-stu-id="503bd-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="503bd-115">Het bijhouden van afzonderlijke transacties.</span><span class="sxs-lookup"><span data-stu-id="503bd-115">Tracking single transactions.</span></span> <span data-ttu-id="503bd-116">Databaselogboeken zijn niet bedoeld voor het bijhouden van geautomatiseerde transacties die in batchtaken worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="503bd-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="503bd-117">Beveiliging voor databaselogboeken</span><span class="sxs-lookup"><span data-stu-id="503bd-117">Security for database logging</span></span>

<span data-ttu-id="503bd-118">Databaselogboeken kunnen vertrouwelijke gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="503bd-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="503bd-119">Beperk de toegang tot beveiligingsrollen die toegang moeten hebben tot de logboekgegevens.</span><span class="sxs-lookup"><span data-stu-id="503bd-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="503bd-120">Databaselogboeken en prestaties</span><span class="sxs-lookup"><span data-stu-id="503bd-120">Database logging and performance</span></span>

<span data-ttu-id="503bd-121">Het bijhouden van databaselogboeken kan waardevol zijn vanuit een zakelijk perspectief, maar ook kostbaar in termen van resourcegebruik en beheer.</span><span class="sxs-lookup"><span data-stu-id="503bd-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="503bd-122">De implicaties van de prestaties van databaselogboeken zijn onder andere:</span><span class="sxs-lookup"><span data-stu-id="503bd-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="503bd-123">De databaselogboektabel kan snel groter worden en veroorzaakt een toename van de omvang van de database.</span><span class="sxs-lookup"><span data-stu-id="503bd-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="503bd-124">De groei is afhankelijk van de hoeveelheid vastgelegde gegevens die u wilt behouden.</span><span class="sxs-lookup"><span data-stu-id="503bd-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="503bd-125">Standaard worden in de databaselogboektabel slechts 30 dagen aan logboekgegevens bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="503bd-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="503bd-126">Databaselogboeken kunnen een negatieve invloed hebben op langdurige geautomatiseerde processen, zoals langlopende gegevensimportprocessen.</span><span class="sxs-lookup"><span data-stu-id="503bd-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="503bd-127">Best practices</span><span class="sxs-lookup"><span data-stu-id="503bd-127">Best practices</span></span>

<span data-ttu-id="503bd-128">Selecteer specifieke velden die u in het logboek wilt opnemen in plaats van gehele tabellen, zodat de prestaties worden verbeterd.</span><span class="sxs-lookup"><span data-stu-id="503bd-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="503bd-129">Om de prestaties op peil te houden zijn de databaselogboeken beperkt tot 20 tabellen.</span><span class="sxs-lookup"><span data-stu-id="503bd-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="503bd-130">Voor afzonderlijke velden kunnen alleen updates worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="503bd-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="503bd-131">Databaselogboek instellen</span><span class="sxs-lookup"><span data-stu-id="503bd-131">Set up database logging</span></span>

<span data-ttu-id="503bd-132">Met de wizard **Logboek van wijzigingen in database maken** kunt u databaselogboeken instellen.</span><span class="sxs-lookup"><span data-stu-id="503bd-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="503bd-133">De wizard biedt een flexibele manier om logboeken voor tabellen of velden in te stellen.</span><span class="sxs-lookup"><span data-stu-id="503bd-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="503bd-134">Ga naar **Systeembeheer > Koppelingen > Database > Databaselogboek instellen**.</span><span class="sxs-lookup"><span data-stu-id="503bd-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="503bd-135">Selecteer **Nieuw** om de wizard **Logboek van wijzigingen in database maken** te starten.</span><span class="sxs-lookup"><span data-stu-id="503bd-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="503bd-136">Voer de wizard uit.</span><span class="sxs-lookup"><span data-stu-id="503bd-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="503bd-137">Databaselogboeken opschonen</span><span class="sxs-lookup"><span data-stu-id="503bd-137">Clean up database logs</span></span>

<span data-ttu-id="503bd-138">U kunt de databaselogboeken geheel of gedeeltelijk verwijderen met behulp van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="503bd-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="503bd-139">Alle logboeken voor een bepaalde tabel selecteren.</span><span class="sxs-lookup"><span data-stu-id="503bd-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="503bd-140">Specifieke typen databaselogboeken selecteren.</span><span class="sxs-lookup"><span data-stu-id="503bd-140">Select specific types of database log.</span></span>
- <span data-ttu-id="503bd-141">Een datum en tijd selecteren waarop een logboek is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="503bd-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="503bd-142">Volg deze stappen om databaselogboeken op te schonen:</span><span class="sxs-lookup"><span data-stu-id="503bd-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="503bd-143">Ga naar **Systeembeheer > Koppelingen > Database > Databaselogboek**.</span><span class="sxs-lookup"><span data-stu-id="503bd-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="503bd-144">Selecteer **Logboek opschonen**.</span><span class="sxs-lookup"><span data-stu-id="503bd-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="503bd-145">Kies een van de volgende opties voor het selecteren van logboeken die u wilt verwijderen:</span><span class="sxs-lookup"><span data-stu-id="503bd-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="503bd-146">Tabel-ID</span><span class="sxs-lookup"><span data-stu-id="503bd-146">Table ID</span></span>
   - <span data-ttu-id="503bd-147">Type logboek</span><span class="sxs-lookup"><span data-stu-id="503bd-147">Type of log</span></span>
   - <span data-ttu-id="503bd-148">Aanmaakdatum en -tijd</span><span class="sxs-lookup"><span data-stu-id="503bd-148">Created date and time</span></span>

3. <span data-ttu-id="503bd-149">Gebruik het tabblad **Databaselogboek opschonen** om te bepalen wanneer u de taak voor het opschonen van het logboek wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="503bd-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="503bd-150">Databaselogboeken zijn standaard 30 dagen beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="503bd-150">By default, database logs are available for 30 days.</span></span>
