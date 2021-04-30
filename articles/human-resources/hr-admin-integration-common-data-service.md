---
title: Dataverse-integratie configureren
description: U kunt de integratie tussen Microsoft Dataverse en Dynamics 365 Human Resources in- of uitschakelen. U kunt ook synchronisatiegegevens weergeven, traceringsgegevens wissen en een tabel opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890023"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="30e25-104">Dataverse-integratie configureren</span><span class="sxs-lookup"><span data-stu-id="30e25-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="30e25-105">U kunt de integratie tussen Microsoft Dataverse en Dynamics 365 Human Resources in- of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="30e25-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="30e25-106">U kunt ook de synchronisatiegegevens weergeven, traceringsgegevens wissen en een tabel opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.</span><span class="sxs-lookup"><span data-stu-id="30e25-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="30e25-107">Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="30e25-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="30e25-108">Wanneer u integratie uitschakelt, kunnen gebruikers wijzigingen aanbrengen in Human Resources of Dataverse, maar deze wijzigingen worden niet gesynchroniseerd tussen de twee omgevingen.</span><span class="sxs-lookup"><span data-stu-id="30e25-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="30e25-109">Integratie tussen Human Resources en Dataverse is standaard uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="30e25-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="30e25-110">Mogelijk wilt u integratie in de volgende situaties uitschakelen:</span><span class="sxs-lookup"><span data-stu-id="30e25-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="30e25-111">U vult gegevens in via het Data Management Framework en u moet de gegevens meerdere keren importeren om de juiste status te krijgen.</span><span class="sxs-lookup"><span data-stu-id="30e25-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="30e25-112">Er zijn problemen met gegevens in Human Resources of Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30e25-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="30e25-113">Als u integratie uitschakelt, kunt u een record in de ene omgeving verwijderen zonder deze in de andere omgeving te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="30e25-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="30e25-114">Wanneer u de integratie weer inschakelt, wordt de record in de omgeving waarin deze niet is verwijderd, gesynchroniseerd naar de omgeving waarin deze was verwijderd.</span><span class="sxs-lookup"><span data-stu-id="30e25-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="30e25-115">De synchronisatie begint de volgende keer dat de batchtaak **Gemiste aanvragen Dataverse-integratie synchroniseren** wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="30e25-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="30e25-116">Wanneer u gegevensintegratie uitschakelt, moet u niet dezelfde record in beide omgevingen bewerken.</span><span class="sxs-lookup"><span data-stu-id="30e25-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="30e25-117">Wanneer u de integratie weer inschakelt, wordt de record die u als laatste hebt bewerkt, gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="30e25-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="30e25-118">Als u in beide omgevingen niet dezelfde wijzigingen in de record hebt aangebracht, kan er gegevensverlies optreden.</span><span class="sxs-lookup"><span data-stu-id="30e25-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="30e25-119">Toegang tot de pagina Dataverse-integratie</span><span class="sxs-lookup"><span data-stu-id="30e25-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="30e25-120">Selecteer in het Human Resources-exemplaar waarin u de instellingen voor de integratie met Dataverse wilt weergeven of configureren, de tegel **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="30e25-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="30e25-121">[![Tegel Systeembeheer](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="30e25-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="30e25-122">Selecteer het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="30e25-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="30e25-123">[![Tabblad Koppelingen](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="30e25-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="30e25-124">Selecteer onder **Integraties** de optie **Dataverse-configuratie**.</span><span class="sxs-lookup"><span data-stu-id="30e25-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="30e25-125">[![Koppeling Dataverse-configuratie](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="30e25-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="30e25-126">Gegevensintegratie tussen Human Resources en Dataverse in- of uitschakelen</span><span class="sxs-lookup"><span data-stu-id="30e25-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="30e25-127">Als u de integratie wilt inschakelen, stelt u de optie **Dataverse-integratie inschakelen** in op **Ja** op de pagina **Microsoft Dataverse-integratie**.</span><span class="sxs-lookup"><span data-stu-id="30e25-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30e25-128">Wanneer u de integratie inschakelt, worden de gegevens gesynchroniseerd wanneer de batchtaak **Gemiste aanvragen Dataverse-integratie synchroniseren** de volgende keer wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="30e25-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="30e25-129">Alle gegevens zijn als het goed is beschikbaar nadat de batchtaak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="30e25-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="30e25-130">Als u de integratie wilt uitschakelen, stelt u de optie in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="30e25-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="30e25-131">[![De Dataverse-integratie in- of uitschakelen](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="30e25-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="30e25-132">Het wordt nadrukkelijk aanbevolen om Dataverse-integratie uit te schakelen tijdens het uitvoeren van gegevensmigratietaken.</span><span class="sxs-lookup"><span data-stu-id="30e25-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="30e25-133">Grote gegevensuploads kunnen de prestaties aanzienlijk beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="30e25-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="30e25-134">Het uploaden van 2000 werknemers kan bijvoorbeeld enkele uren duren wanneer integratie is ingeschakeld, en minder dan een uur wanneer het is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="30e25-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="30e25-135">De getallen die in dit voorbeeld worden gegeven, zijn alleen voor demonstratiedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="30e25-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="30e25-136">De exacte hoeveelheid tijd die nodig is voor het importeren van records kan sterk variëren op basis van een groot aantal factoren.</span><span class="sxs-lookup"><span data-stu-id="30e25-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="30e25-137">Details van de gegevensintegratie weergeven</span><span class="sxs-lookup"><span data-stu-id="30e25-137">View data integration details</span></span>

<span data-ttu-id="30e25-138">Op het sneltabblad **Beheer** van de pagina **Microsoft Dataverse-integratie** kunt u zien hoe de rijen in Human Resources en Dataverse aan elkaar zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="30e25-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="30e25-139">Als u de rijen voor een tabel wilt weergeven, selecteert u de tabel in het veld **Dataverse-tabel**.</span><span class="sxs-lookup"><span data-stu-id="30e25-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="30e25-140">In het raster worden alle rijen weergegeven die zijn gekoppeld aan de geselecteerde tabel.</span><span class="sxs-lookup"><span data-stu-id="30e25-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="30e25-141">Niet alle Dataverse-tabellen worden op dit moment weergegeven.</span><span class="sxs-lookup"><span data-stu-id="30e25-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="30e25-142">Alleen tabellen die het gebruik van aangepaste velden ondersteunen, worden weergegeven in het raster.</span><span class="sxs-lookup"><span data-stu-id="30e25-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="30e25-143">Nieuwe tabellen worden beschikbaar via doorlopende releases van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="30e25-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="30e25-144">Het raster bevat de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="30e25-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="30e25-145">**Dataverse-tabel**: de naam van de tabel in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30e25-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="30e25-146">**Dataverse-tabelverwijzing**: de id die in Dataverse wordt gebruikt om een record aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="30e25-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="30e25-147">Deze waarde is gelijk aan de **RecId**-waarde van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="30e25-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="30e25-148">U kunt de id vinden wanneer u de Dataverse-tabel opent in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="30e25-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="30e25-149">**Human Resources-entiteitsnaam**: de Human Resources-entiteit die als laatste gegevens heeft gesynchroniseerd naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30e25-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="30e25-150">De entiteit kan het voorvoegsel Dataverse of een ander voorvoegsel hebben.</span><span class="sxs-lookup"><span data-stu-id="30e25-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="30e25-151">**Human Resources-verwijzing** – De **RecId**-waarde die is gekoppeld aan de record in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="30e25-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="30e25-152">**Verwijderd uit Dataverse**: een waarde die aangeeft of de rij is verwijderd uit Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30e25-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="30e25-153">Records in Human Resources komen overeen met rijen in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30e25-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="30e25-154">De koppeling van een record in Human Resources verwijderen uit een Dataverse-rij</span><span class="sxs-lookup"><span data-stu-id="30e25-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="30e25-155">Als u problemen ondervindt tijdens de gegevenssynchronisatie tussen Human Resources en Dataverse, kunt u deze mogelijk oplossen door de traceringsgegevens te wissen en de traceringstabel opnieuw te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="30e25-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="30e25-156">Als u de koppeling verwijdert en vervolgens een rij wijzigt of verwijdert in Dataverse, worden de wijzigingen niet gesynchroniseerd naar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="30e25-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="30e25-157">Als u wijzigingen aanbrengt in Human Resources, wordt er een nieuwe traceringsrecord gemaakt en wordt de rij bijgewerkt in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30e25-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="30e25-158">Als u de koppeling van een Human Resources-record en een Dataverse-rij wilt verwijderen, selecteert u de tabel in het veld **Dataverse-tabel** en selecteert u de optie **Traceringsgegevens wissen**.</span><span class="sxs-lookup"><span data-stu-id="30e25-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="30e25-159">[![Traceringsgegevens wissen](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="30e25-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="30e25-160">Zie de volgende procedure als u een volledige synchronisatie wilt uitvoeren op de tabel nadat u de traceringsgegevens hebt gewist.</span><span class="sxs-lookup"><span data-stu-id="30e25-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="30e25-161">Een tabel synchroniseren tussen Human Resources en Dataverse</span><span class="sxs-lookup"><span data-stu-id="30e25-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="30e25-162">Gebruik deze procedure als:</span><span class="sxs-lookup"><span data-stu-id="30e25-162">Use this procedure when:</span></span>

- <span data-ttu-id="30e25-163">De wijzigingen van Dataverse te lang duren om te worden weergegeven in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="30e25-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="30e25-164">U moet de traceringstabel vernieuwen nadat u de tracering hebt gewist.</span><span class="sxs-lookup"><span data-stu-id="30e25-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="30e25-165">Een volledige synchronisatie uitvoeren voor een tabel tussen Human Resources en Dataverse:</span><span class="sxs-lookup"><span data-stu-id="30e25-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="30e25-166">Selecteer de tabel in het veld **Dataverse-tabel**.</span><span class="sxs-lookup"><span data-stu-id="30e25-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="30e25-167">Selecteer **Nu synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="30e25-167">Select **Sync now**.</span></span>

<span data-ttu-id="30e25-168">[![Een volledige synchronisatie uitvoeren](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="30e25-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="30e25-169">Zie ook</span><span class="sxs-lookup"><span data-stu-id="30e25-169">See also</span></span>

[<span data-ttu-id="30e25-170">Dataverse-tabellen</span><span class="sxs-lookup"><span data-stu-id="30e25-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="30e25-171">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="30e25-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="30e25-172">Veelgestelde vragen over virtuele tabellen voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="30e25-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="30e25-173">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="30e25-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="30e25-174">Terminologiewijzigingen</span><span class="sxs-lookup"><span data-stu-id="30e25-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]