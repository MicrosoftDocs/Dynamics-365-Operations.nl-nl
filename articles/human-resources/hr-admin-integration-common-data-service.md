---
title: Common Data Service-integratie configureren
description: U kunt de integratie tussen Common Data Service en een exemplaar van Microsoft Dynamics 365 Human Resources in- of uitschakelen. U kunt ook de synchronisatiegegevens weergeven, traceringsgegevens wissen en een entiteit opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.
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
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008592"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="e271d-104">Common Data Service-integratie configureren</span><span class="sxs-lookup"><span data-stu-id="e271d-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="e271d-105">U kunt de integratie tussen Common Data Service en een exemplaar van Microsoft Dynamics 365 Human Resources in- of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="e271d-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="e271d-106">U kunt ook de synchronisatiegegevens weergeven, traceringsgegevens wissen en een entiteit opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.</span><span class="sxs-lookup"><span data-stu-id="e271d-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="e271d-107">Wanneer u integratie uitschakelt, kunnen gebruikers wijzigingen aanbrengen in Human Resources of Common Data Service, maar deze wijzigingen worden niet gesynchroniseerd tussen de twee omgevingen.</span><span class="sxs-lookup"><span data-stu-id="e271d-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="e271d-108">De integratie tussen Human Resources en Common Data Service is standaard uitgeschakeld of ingeschakeld, afhankelijk van de aanwezigheid van demogegevens in de omgevingen:</span><span class="sxs-lookup"><span data-stu-id="e271d-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="e271d-109">**Uit** voor nieuwe omgevingen waarin geen demogegevens zijn opgenomen</span><span class="sxs-lookup"><span data-stu-id="e271d-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="e271d-110">**Aan** voor nieuwe omgevingen waarin demogegevens zijn opgenomen</span><span class="sxs-lookup"><span data-stu-id="e271d-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="e271d-111">Nieuwe omgevingen die demogegevens bevatten, beginnen met het synchroniseren van gegevens wanneer ze worden ingericht.</span><span class="sxs-lookup"><span data-stu-id="e271d-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="e271d-112">Mogelijk wilt u integratie in de volgende situaties uitschakelen:</span><span class="sxs-lookup"><span data-stu-id="e271d-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="e271d-113">U vult gegevens in via het Data Management Framework en u moet de gegevens meerdere keren importeren om de juiste status te krijgen.</span><span class="sxs-lookup"><span data-stu-id="e271d-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="e271d-114">Er zijn problemen met gegevens in Human Resources of Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e271d-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="e271d-115">Als u integratie uitschakelt, kunt u een record in de ene omgeving verwijderen zonder deze in de andere omgeving te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="e271d-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="e271d-116">Wanneer u de integratie weer inschakelt, wordt de record in de omgeving waarin deze niet is verwijderd, opnieuw gesynchroniseerd naar de omgeving waarin deze was verwijderd.</span><span class="sxs-lookup"><span data-stu-id="e271d-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="e271d-117">De synchronisatie begint de volgende keer dat de batchtaak **Gemiste aanvragen Common Data Service-integratie synchroniseren** wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e271d-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="e271d-118">Wanneer u gegevensintegratie uitschakelt, moet u niet dezelfde record in beide omgevingen bewerken.</span><span class="sxs-lookup"><span data-stu-id="e271d-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="e271d-119">Wanneer u de integratie weer inschakelt, wordt de record die u als laatste hebt bewerkt, gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="e271d-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="e271d-120">Als u in beide omgevingen niet dezelfde wijzigingen in de record hebt aangebracht, kan er gegevensverlies optreden.</span><span class="sxs-lookup"><span data-stu-id="e271d-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="e271d-121">Toegang tot de pagina Common Data Service-integratie</span><span class="sxs-lookup"><span data-stu-id="e271d-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="e271d-122">Selecteer in het Human Resources-exemplaar waarin u de instellingen voor de integratie met Common Data Service wilt weergeven of configureren, de tegel **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="e271d-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="e271d-123">[![Tegel Systeembeheer](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="e271d-124">Selecteer het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="e271d-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="e271d-125">[![Tabblad Koppelingen](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="e271d-126">Selecteer onder **Integraties** de optie **Common Data Service-configuratie**.</span><span class="sxs-lookup"><span data-stu-id="e271d-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="e271d-127">[![Koppeling Common Data Service-configuratie](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="e271d-128">Gegevensintegratie tussen Human Resources en Common Data Service in- of uitschakelen</span><span class="sxs-lookup"><span data-stu-id="e271d-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="e271d-129">Als u de integratie wilt inschakelen, stelt u de optie **De integratie met Common Data Service inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e271d-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e271d-130">Wanneer u de integratie inschakelt, worden de gegevens gesynchroniseerd wanneer de batchtaak **Gemiste aanvragen Common Data Service-integratie synchroniseren** de volgende keer wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e271d-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="e271d-131">Alle gegevens zijn als het goed is beschikbaar nadat de batchtaak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="e271d-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="e271d-132">Als u de integratie wilt uitschakelen, stelt u de optie in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="e271d-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="e271d-133">[![De Common Data Service-integratie in- of uitschakelen](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="e271d-134">Details van de gegevensintegratie weergeven</span><span class="sxs-lookup"><span data-stu-id="e271d-134">View data integration details</span></span>

<span data-ttu-id="e271d-135">Op het sneltabblad **Beheer** van de pagina **Common Data Service-integratie** kunt u zien hoe de records in Human Resources en Common Data Service aan elkaar zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e271d-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="e271d-136">Als u de records voor een entiteit wilt weergeven, selecteert u de entiteit in het veld**CDS-entiteitsnaam**.</span><span class="sxs-lookup"><span data-stu-id="e271d-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="e271d-137">In het raster worden alle records weergegeven die zijn gekoppeld aan de geselecteerde entiteit.</span><span class="sxs-lookup"><span data-stu-id="e271d-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="e271d-138">[![De records voor een entiteit weergeven](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e271d-139">Niet alle Common Data Service-entiteiten worden op dit moment in het raster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e271d-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="e271d-140">Alleen entiteiten die het gebruik van aangepaste velden ondersteunen, worden weergegeven in het raster.</span><span class="sxs-lookup"><span data-stu-id="e271d-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="e271d-141">Nieuwe entiteiten worden beschikbaar via doorlopende releases van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e271d-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="e271d-142">Het raster bevat de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="e271d-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="e271d-143">**CDS-entiteitsnaam** – De naam van de entiteit in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e271d-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="e271d-144">**CDS-entiteitsverwijzing** – De id die in Common Data Service wordt gebruikt om een record aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="e271d-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="e271d-145">Deze waarde is gelijk aan de **RecId**-waarde van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e271d-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="e271d-146">U kunt de id vinden wanneer u de Common Data Service-entiteit opent in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e271d-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="e271d-147">**Human Resources-entiteitsnaam** – De entiteit die als laatste gegevens heeft gesynchroniseerd naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e271d-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="e271d-148">De entiteit kan het voorvoegsel Common Data Service of een ander voorvoegsel hebben.</span><span class="sxs-lookup"><span data-stu-id="e271d-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="e271d-149">**Human Resources-verwijzing** – De **RecId**-waarde die is gekoppeld aan de record in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e271d-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="e271d-150">**Is verwijderd uit CDS** – Een waarde die aangeeft of de record is verwijderd uit Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e271d-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="e271d-151">De koppeling van een record in Human Resources verwijderen uit Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e271d-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="e271d-152">Als u problemen ondervindt tijdens de gegevenssynchronisatie tussen Human Resources en Common Data Service, kunt u deze mogelijk oplossen door de traceringsgegevens te wissen en de traceringstabel opnieuw te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="e271d-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="e271d-153">Als u de koppeling verwijdert en vervolgens een record wijzigt of verwijdert in Common Data Service, worden de wijzigingen niet gesynchroniseerd naar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e271d-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="e271d-154">Als u wijzigingen aanbrengt in Human Resources, wordt er een nieuwe traceringsrecord gemaakt en wordt de record bijgewerkt in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e271d-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="e271d-155">Als u de koppeling van een record tussen Human Resources en Common Data Service wilt verwijderen, selecteert u de entiteit in het veld **CDS-entiteitsnaam** en selecteert u vervolgens de optie **Traceringsgegevens wissen**.</span><span class="sxs-lookup"><span data-stu-id="e271d-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="e271d-156">[![Traceringsgegevens wissen](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="e271d-157">Zie de volgende procedure als u een volledige synchronisatie wilt uitvoeren op de entiteit nadat u de traceringsgegevens hebt gewist.</span><span class="sxs-lookup"><span data-stu-id="e271d-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="e271d-158">Een entiteit synchroniseren tussen Human Resources en Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e271d-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="e271d-159">Gebruik deze procedure als het te lang duurt voor wijzigingen in Common Data Service in Human Resources verschijnen, of als u de traceringstabel moet vernieuwen nadat u de traceringsgegevens hebt gewist.</span><span class="sxs-lookup"><span data-stu-id="e271d-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="e271d-160">Als u een volledige synchronisatie wilt uitvoeren voor een entiteit tussen Human Resources en Common Data Service, selecteert u de entiteit in het veld **CDS- entiteitsnaam** en selecteert u **Nu synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="e271d-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="e271d-161">[![Een volledige synchronisatie uitvoeren](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


