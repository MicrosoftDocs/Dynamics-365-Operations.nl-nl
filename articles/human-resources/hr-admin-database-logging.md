---
title: Databaselogboeken configureren en beheren
description: U kunt wijzigingen in tabellen en velden in Dynamics 365 Human Resources bijhouden met databaselogboeken.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801330"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="5a2cd-103">Databaselogboeken configureren en beheren</span><span class="sxs-lookup"><span data-stu-id="5a2cd-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5a2cd-104">U kunt wijzigingen in tabellen en velden in Dynamics 365 Human Resources bijhouden met databaselogboeken.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="5a2cd-105">In dit onderwerp komt het volgende aan de orde:</span><span class="sxs-lookup"><span data-stu-id="5a2cd-105">This topic describes how to:</span></span>

- <span data-ttu-id="5a2cd-106">Beveiliging en prestaties voor databaselogboeken beheren</span><span class="sxs-lookup"><span data-stu-id="5a2cd-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="5a2cd-107">Databaselogboek instellen</span><span class="sxs-lookup"><span data-stu-id="5a2cd-107">Set up database logging</span></span>
- <span data-ttu-id="5a2cd-108">Databaselogboeken opschonen</span><span class="sxs-lookup"><span data-stu-id="5a2cd-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="5a2cd-109">Overzicht van databaselogboeken</span><span class="sxs-lookup"><span data-stu-id="5a2cd-109">Overview of database logging</span></span>

<span data-ttu-id="5a2cd-110">U kunt specifieke wijzigingen in Microsoft Dynamics 365 Human Resources bijhouden met databaselogboeken.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="5a2cd-111">Deze wijzigingen betreffen onder andere invoegen, bijwerken of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="5a2cd-112">Met databaselogboeken wordt een record met wijzigingen in tabellen of velden in de databaselogboektabel opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="5a2cd-113">Zakelijke toepassingen van databaselogboeken zijn onder andere:</span><span class="sxs-lookup"><span data-stu-id="5a2cd-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="5a2cd-114">Een controlerecord maken van wijzigingen in specifieke tabellen die gevoelige informatie bevatten.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="5a2cd-115">Het bijhouden van afzonderlijke transacties.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-115">Tracking single transactions.</span></span> <span data-ttu-id="5a2cd-116">Databaselogboeken zijn niet bedoeld voor het bijhouden van geautomatiseerde transacties die in batchtaken worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="5a2cd-117">Beveiliging voor databaselogboeken</span><span class="sxs-lookup"><span data-stu-id="5a2cd-117">Security for database logging</span></span>

<span data-ttu-id="5a2cd-118">Databaselogboeken kunnen vertrouwelijke gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="5a2cd-119">Beperk de toegang tot beveiligingsrollen die toegang moeten hebben tot de logboekgegevens.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="5a2cd-120">Databaselogboeken en prestaties</span><span class="sxs-lookup"><span data-stu-id="5a2cd-120">Database logging and performance</span></span>

<span data-ttu-id="5a2cd-121">Het bijhouden van databaselogboeken kan waardevol zijn vanuit een zakelijk perspectief, maar ook kostbaar in termen van resourcegebruik en beheer.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="5a2cd-122">De implicaties van de prestaties van databaselogboeken zijn onder andere:</span><span class="sxs-lookup"><span data-stu-id="5a2cd-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="5a2cd-123">De databaselogboektabel kan snel groter worden en veroorzaakt een toename van de omvang van de database.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="5a2cd-124">De groei is afhankelijk van de hoeveelheid vastgelegde gegevens die u wilt behouden.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="5a2cd-125">Standaard worden in de databaselogboektabel slechts 30 dagen aan logboekgegevens bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="5a2cd-126">Databaselogboeken kunnen een negatieve invloed hebben op langdurige geautomatiseerde processen, zoals langlopende gegevensimportprocessen.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="5a2cd-127">Best practices</span><span class="sxs-lookup"><span data-stu-id="5a2cd-127">Best practices</span></span>

<span data-ttu-id="5a2cd-128">Selecteer specifieke velden die u in het logboek wilt opnemen in plaats van gehele tabellen, zodat de prestaties worden verbeterd.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="5a2cd-129">Om de prestaties op peil te houden zijn de databaselogboeken beperkt tot 20 tabellen.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="5a2cd-130">Voor afzonderlijke velden kunnen alleen updates worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="5a2cd-131">Databaselogboek instellen</span><span class="sxs-lookup"><span data-stu-id="5a2cd-131">Set up database logging</span></span>

<span data-ttu-id="5a2cd-132">Met de wizard **Logboek van wijzigingen in database maken** kunt u databaselogboeken instellen.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="5a2cd-133">De wizard biedt een flexibele manier om logboeken voor tabellen of velden in te stellen.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="5a2cd-134">Ga naar **Systeembeheer > Koppelingen > Database > Databaselogboek instellen**.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="5a2cd-135">Selecteer **Nieuw** om de wizard **Logboek van wijzigingen in database maken** te starten.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="5a2cd-136">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-136">Select **Next**.</span></span> 
3. <span data-ttu-id="5a2cd-137">Selecteer op de pagina **Tabellen en velden** van de wizard de tabellen en velden waarvoor u databaseregistratie wilt inschakelen en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="5a2cd-138">Databaseregistratie is niet beschikbaar voor alle tabellen in de Human Resources-database.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="5a2cd-139">Als u **Alle tabellen weergeven** selecteert onder de lijst, wordt de lijst met tabellen en velden uitgebreid om alle databasetabellen weer te geven waarvoor databaseregistratie beschikbaar is, maar dit is een subset van de volledige lijst met databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="5a2cd-140">Selecteer op de pagina **Typen wijzigingen** van de wizard de gegevensbewerkingen waarvoor u wijzigingen voor elk van de tabellen en velden wilt bijhouden en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="5a2cd-141">Zie de onderstaande tabel voor een beschrijving van de gegevensbewerkingen die beschikbaar zijn voor logboekregistratie.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="5a2cd-142">Bekijk op de pagina **Voltooien** de wijzigingen die worden aangebracht en selecteer **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="5a2cd-143">Bewerking</span><span class="sxs-lookup"><span data-stu-id="5a2cd-143">Operation</span></span> | <span data-ttu-id="5a2cd-144">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5a2cd-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="5a2cd-145">Nieuwe transacties traceren</span><span class="sxs-lookup"><span data-stu-id="5a2cd-145">Track new transactions</span></span> | <span data-ttu-id="5a2cd-146">Maak een logboek voor nieuwe records die in de tabel worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="5a2cd-147">Update</span><span class="sxs-lookup"><span data-stu-id="5a2cd-147">Update</span></span> | <span data-ttu-id="5a2cd-148">Maak een logboek voor updates van tabelrecords of updates voor afzonderlijk geselecteerde velden in de tabel.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="5a2cd-149">Als u ervoor kiest om updates voor de tabel te registreren, wordt er elke keer een logboekrecord gemaakt als een update wordt uitgevoerd voor een veld van een record in de tabel.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="5a2cd-150">Als u ervoor kiest om updates voor specifieke velden te registreren, wordt alleen een logboekrecord gemaakt bij updates van die velden van tabelrecords.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="5a2cd-151">Delete</span><span class="sxs-lookup"><span data-stu-id="5a2cd-151">Delete</span></span> | <span data-ttu-id="5a2cd-152">Maak een logboek voor records die uit de tabel worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="5a2cd-153">Sleutel hernoemen</span><span class="sxs-lookup"><span data-stu-id="5a2cd-153">Rename key</span></span> | <span data-ttu-id="5a2cd-154">Maak een logboekrecord wanneer de naam van een tabelsleutel wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="5a2cd-155">Databaselogboeken opschonen</span><span class="sxs-lookup"><span data-stu-id="5a2cd-155">Clean up database logs</span></span>

<span data-ttu-id="5a2cd-156">U kunt de databaselogboeken geheel of gedeeltelijk verwijderen met behulp van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="5a2cd-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="5a2cd-157">Alle logboeken voor een bepaalde tabel selecteren.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="5a2cd-158">Specifieke typen databaselogboeken selecteren.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-158">Select specific types of database log.</span></span>
- <span data-ttu-id="5a2cd-159">Een datum en tijd selecteren waarop een logboek is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="5a2cd-160">Volg deze stappen om databaselogboeken op te schonen:</span><span class="sxs-lookup"><span data-stu-id="5a2cd-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="5a2cd-161">Ga naar **Systeembeheer > Koppelingen > Database > Databaselogboek**.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="5a2cd-162">Selecteer **Logboek opschonen**.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="5a2cd-163">Kies een van de volgende opties voor het selecteren van logboeken die u wilt verwijderen:</span><span class="sxs-lookup"><span data-stu-id="5a2cd-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="5a2cd-164">Tabel-ID</span><span class="sxs-lookup"><span data-stu-id="5a2cd-164">Table ID</span></span>
   - <span data-ttu-id="5a2cd-165">Type logboek</span><span class="sxs-lookup"><span data-stu-id="5a2cd-165">Type of log</span></span>
   - <span data-ttu-id="5a2cd-166">Aanmaakdatum en -tijd</span><span class="sxs-lookup"><span data-stu-id="5a2cd-166">Created date and time</span></span>

3. <span data-ttu-id="5a2cd-167">Gebruik het tabblad **Databaselogboek opschonen** om te bepalen wanneer u de taak voor het opschonen van het logboek wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="5a2cd-168">Databaselogboeken zijn standaard 30 dagen beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="5a2cd-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
