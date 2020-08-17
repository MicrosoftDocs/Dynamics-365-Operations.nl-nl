---
title: Common Data Service-integratie configureren
description: U kunt de integratie tussen Common Data Service en Dynamics 365 Human Resources in- of uitschakelen. U kunt ook synchronisatiegegevens weergeven, traceringsgegevens wissen en een entiteit opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 8cbead2961c4576a5394080aae2fec109bce3f10
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621299"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="fb44c-104">Common Data Service-integratie configureren</span><span class="sxs-lookup"><span data-stu-id="fb44c-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="fb44c-105">U kunt de integratie tussen Common Data Service en Dynamics 365 Human Resources in- of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="fb44c-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="fb44c-106">U kunt ook de synchronisatiegegevens weergeven, traceringsgegevens wissen en een entiteit opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.</span><span class="sxs-lookup"><span data-stu-id="fb44c-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="fb44c-107">Wanneer u integratie uitschakelt, kunnen gebruikers wijzigingen aanbrengen in Human Resources of Common Data Service, maar deze wijzigingen worden niet gesynchroniseerd tussen de twee omgevingen.</span><span class="sxs-lookup"><span data-stu-id="fb44c-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="fb44c-108">Integratie tussen Human Resources en Common Data Service is standaard uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="fb44c-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="fb44c-109">Mogelijk wilt u integratie in de volgende situaties uitschakelen:</span><span class="sxs-lookup"><span data-stu-id="fb44c-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="fb44c-110">U vult gegevens in via het Data Management Framework en u moet de gegevens meerdere keren importeren om de juiste status te krijgen.</span><span class="sxs-lookup"><span data-stu-id="fb44c-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="fb44c-111">Er zijn problemen met gegevens in Human Resources of Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fb44c-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="fb44c-112">Als u integratie uitschakelt, kunt u een record in de ene omgeving verwijderen zonder deze in de andere omgeving te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="fb44c-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="fb44c-113">Wanneer u de integratie weer inschakelt, wordt de record in de omgeving waarin deze niet is verwijderd, gesynchroniseerd naar de omgeving waarin deze was verwijderd.</span><span class="sxs-lookup"><span data-stu-id="fb44c-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="fb44c-114">De synchronisatie begint de volgende keer dat de batchtaak **Gemiste aanvragen Common Data Service-integratie synchroniseren** wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fb44c-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="fb44c-115">Wanneer u gegevensintegratie uitschakelt, moet u niet dezelfde record in beide omgevingen bewerken.</span><span class="sxs-lookup"><span data-stu-id="fb44c-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="fb44c-116">Wanneer u de integratie weer inschakelt, wordt de record die u als laatste hebt bewerkt, gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="fb44c-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="fb44c-117">Als u in beide omgevingen niet dezelfde wijzigingen in de record hebt aangebracht, kan er gegevensverlies optreden.</span><span class="sxs-lookup"><span data-stu-id="fb44c-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="fb44c-118">Toegang tot de pagina Common Data Service-integratie</span><span class="sxs-lookup"><span data-stu-id="fb44c-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="fb44c-119">Selecteer in het Human Resources-exemplaar waarin u de instellingen voor de integratie met Common Data Service wilt weergeven of configureren, de tegel **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="fb44c-120">[![Tegel Systeembeheer](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="fb44c-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="fb44c-121">Selecteer het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="fb44c-122">[![Tabblad Koppelingen](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="fb44c-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="fb44c-123">Selecteer onder **Integraties** de optie **Common Data Service-configuratie**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="fb44c-124">[![Koppeling Common Data Service-configuratie](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="fb44c-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="fb44c-125">Gegevensintegratie tussen Human Resources en Common Data Service in- of uitschakelen</span><span class="sxs-lookup"><span data-stu-id="fb44c-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="fb44c-126">Als u de integratie wilt inschakelen, stelt u de optie **De integratie met Common Data Service inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb44c-127">Wanneer u de integratie inschakelt, worden de gegevens gesynchroniseerd wanneer de batchtaak **Gemiste aanvragen Common Data Service-integratie synchroniseren** de volgende keer wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fb44c-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="fb44c-128">Alle gegevens zijn als het goed is beschikbaar nadat de batchtaak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="fb44c-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="fb44c-129">Als u de integratie wilt uitschakelen, stelt u de optie in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="fb44c-130">[![De Common Data Service-integratie in- of uitschakelen](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="fb44c-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="fb44c-131">Het wordt nadrukkelijk aanbevolen om Common Data Service-integratie uit te schakelen tijdens het uitvoeren van gegevensmigratietaken.</span><span class="sxs-lookup"><span data-stu-id="fb44c-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="fb44c-132">Grote gegevensuploads kunnen de prestaties aanzienlijk beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="fb44c-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="fb44c-133">Het uploaden van 2000 werknemers kan bijvoorbeeld enkele uren duren wanneer integratie is ingeschakeld, en minder dan een uur wanneer het is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="fb44c-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="fb44c-134">De getallen die in dit voorbeeld worden gegeven, zijn alleen voor demonstratiedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="fb44c-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="fb44c-135">De exacte hoeveelheid tijd die nodig is voor het importeren van records kan sterk variëren op basis van een groot aantal factoren.</span><span class="sxs-lookup"><span data-stu-id="fb44c-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="fb44c-136">Details van de gegevensintegratie weergeven</span><span class="sxs-lookup"><span data-stu-id="fb44c-136">View data integration details</span></span>

<span data-ttu-id="fb44c-137">Op het sneltabblad **Beheer** van de pagina **Common Data Service-integratie** kunt u zien hoe de records in Human Resources en Common Data Service aan elkaar zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="fb44c-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="fb44c-138">Als u de records voor een entiteit wilt weergeven, selecteert u de entiteit in het veld**CDS-entiteitsnaam**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="fb44c-139">In het raster worden alle records weergegeven die zijn gekoppeld aan de geselecteerde entiteit.</span><span class="sxs-lookup"><span data-stu-id="fb44c-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="fb44c-140">[![De records voor een entiteit weergeven](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="fb44c-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="fb44c-141">Niet alle Common Data Service-entiteiten worden op dit moment in het raster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fb44c-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="fb44c-142">Alleen entiteiten die het gebruik van aangepaste velden ondersteunen, worden weergegeven in het raster.</span><span class="sxs-lookup"><span data-stu-id="fb44c-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="fb44c-143">Nieuwe entiteiten worden beschikbaar via doorlopende releases van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fb44c-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="fb44c-144">Het raster bevat de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="fb44c-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="fb44c-145">**CDS-entiteitsnaam** – De naam van de entiteit in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fb44c-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="fb44c-146">**CDS-entiteitsverwijzing** – De id die in Common Data Service wordt gebruikt om een record aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="fb44c-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="fb44c-147">Deze waarde is gelijk aan de **RecId**-waarde van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fb44c-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="fb44c-148">U kunt de id vinden wanneer u de Common Data Service-entiteit opent in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fb44c-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="fb44c-149">**Human Resources-entiteitsnaam** – De entiteit die als laatste gegevens heeft gesynchroniseerd naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fb44c-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="fb44c-150">De entiteit kan het voorvoegsel Common Data Service of een ander voorvoegsel hebben.</span><span class="sxs-lookup"><span data-stu-id="fb44c-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="fb44c-151">**Human Resources-verwijzing** – De **RecId**-waarde die is gekoppeld aan de record in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fb44c-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="fb44c-152">**Is verwijderd uit CDS** – Een waarde die aangeeft of de record is verwijderd uit Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fb44c-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="fb44c-153">De koppeling van een record in Human Resources verwijderen uit Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fb44c-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="fb44c-154">Als u problemen ondervindt tijdens de gegevenssynchronisatie tussen Human Resources en Common Data Service, kunt u deze mogelijk oplossen door de traceringsgegevens te wissen en de traceringstabel opnieuw te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="fb44c-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="fb44c-155">Als u de koppeling verwijdert en vervolgens een record wijzigt of verwijdert in Common Data Service, worden de wijzigingen niet gesynchroniseerd naar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fb44c-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="fb44c-156">Als u wijzigingen aanbrengt in Human Resources, wordt er een nieuwe traceringsrecord gemaakt en wordt de record bijgewerkt in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fb44c-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="fb44c-157">Als u de koppeling van een record tussen Human Resources en Common Data Service wilt verwijderen, selecteert u de entiteit in het veld **CDS-entiteitsnaam** en selecteert u vervolgens de optie **Traceringsgegevens wissen**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="fb44c-158">[![Traceringsgegevens wissen](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="fb44c-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="fb44c-159">Zie de volgende procedure als u een volledige synchronisatie wilt uitvoeren op de entiteit nadat u de traceringsgegevens hebt gewist.</span><span class="sxs-lookup"><span data-stu-id="fb44c-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="fb44c-160">Een entiteit synchroniseren tussen Human Resources en Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fb44c-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="fb44c-161">Gebruik deze procedure als:</span><span class="sxs-lookup"><span data-stu-id="fb44c-161">Use this procedure when:</span></span>

- <span data-ttu-id="fb44c-162">De wijzigingen van Common Data Service te lang duren om te worden weergegeven in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fb44c-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="fb44c-163">U moet de traceringstabel vernieuwen nadat u de tracering hebt gewist.</span><span class="sxs-lookup"><span data-stu-id="fb44c-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="fb44c-164">Een volledige synchronisatie uitvoeren voor een entiteit tussen Human Resources en Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="fb44c-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="fb44c-165">Selecteer de entiteit in het veld **CDS-entiteitsnaam**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="fb44c-166">Selecteer **Nu synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="fb44c-166">Select **Sync now**.</span></span>

<span data-ttu-id="fb44c-167">[![Een volledige synchronisatie uitvoeren](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="fb44c-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


