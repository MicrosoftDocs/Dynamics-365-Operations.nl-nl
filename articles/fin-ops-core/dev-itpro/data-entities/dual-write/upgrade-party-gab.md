---
title: Bijwerken naar het model voor partij en globaal adresboek
description: In dit onderwerp wordt beschreven hoe u gegevens voor twee keer wegschrijven kunt upgraden naar het partij- en globale adresboekmodel.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112668"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="0ddba-103">Bijwerken naar het model voor partij en globaal adresboek</span><span class="sxs-lookup"><span data-stu-id="0ddba-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0ddba-104">Met de [Microsoft Azure Data Factory-sjabloon](https://aka.ms/dual-write-gab-adf) kunt u bestaande tabelgegevens voor **Account**, **Contactpersoon** en **Leverancier** met twee keer wegschrijven upgraden naar het partij- en globale adresboekmodel.</span><span class="sxs-lookup"><span data-stu-id="0ddba-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="0ddba-105">Met de sjabloon worden de gegevens van zowel Finance and Operations-apps als Customer Engagement-applicaties afgestemd.</span><span class="sxs-lookup"><span data-stu-id="0ddba-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="0ddba-106">Aan het einde van het proces worden de velden **Partij** en **Contactpersoon** gemaakt voor **partijrecords** en gekoppeld aan **account-**, **contactpersoon-** en **leveranciers** records in klantbetrokkenheidstoepassingen.</span><span class="sxs-lookup"><span data-stu-id="0ddba-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="0ddba-107">Er wordt een .csv-bestand (`FONewParty.csv`) gegenereerd om nieuwe **Partij**-records te maken in de Finance and Operations-app .</span><span class="sxs-lookup"><span data-stu-id="0ddba-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="0ddba-108">Dit onderwerp bevat instructies voor het gebruik van de Data Factory-sjabloon en het upgraden van uw gegevens.</span><span class="sxs-lookup"><span data-stu-id="0ddba-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="0ddba-109">Als u geen aanpassingen hebt, kunt u de sjabloon ongewijzigd gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0ddba-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="0ddba-110">Als u aanpassingen hebt voor **Account**, **Contactpersoon** en **Leverancier**, moet u de sjabloon wijzigen met behulp van de volgende instructies.</span><span class="sxs-lookup"><span data-stu-id="0ddba-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="0ddba-111">Met de sjabloon wordt alleen een upgrade uitgevoerd op de **Partij**-gegevens .</span><span class="sxs-lookup"><span data-stu-id="0ddba-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="0ddba-112">In een toekomstige release zullen post- en elektronische adressen worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0ddba-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ddba-113">Vereisten</span><span class="sxs-lookup"><span data-stu-id="0ddba-113">Prerequisites</span></span>

<span data-ttu-id="0ddba-114">De volgende vereisten zijn vereist om een upgrade naar het partij- en globale adresboekmodel uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="0ddba-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="0ddba-115">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="0ddba-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="0ddba-116">Toegang tot de sjabloon</span><span class="sxs-lookup"><span data-stu-id="0ddba-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="0ddba-117">U moet een bestaande klant voor twee keer wegschrijven zijn.</span><span class="sxs-lookup"><span data-stu-id="0ddba-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="0ddba-118">Upgrade voorbereiden</span><span class="sxs-lookup"><span data-stu-id="0ddba-118">Prepare for the upgrade</span></span>
<span data-ttu-id="0ddba-119">Ter voorbereiding op de upgrade zijn de volgende activiteiten nodig:</span><span class="sxs-lookup"><span data-stu-id="0ddba-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="0ddba-120">**Volledig gesynchroniseerd**: beide omgevingen zijn volledig gesynchroniseerd voor **Account (klant)**, **Contactpersoon** en **Leverancier**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="0ddba-121">**Integratiesleutels:** de tabellen **Account (klant)**, **Contactpersoon** en **Leverancier** in apps voor klantbetrokkenheid gebruiken de integratiesleutels die met het product worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="0ddba-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="0ddba-122">Als u de integratiesleutels hebt aangepast, moet u de sjabloon aanpassen.</span><span class="sxs-lookup"><span data-stu-id="0ddba-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="0ddba-123">**Partijnummer**: alle records van **Account (klant)**, **Contactpersoon** en **Leverancier** die worden bijgewerkt, hebben een **partijnummer**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="0ddba-124">Records zonder **partijnummer** worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="0ddba-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="0ddba-125">Als u deze records wilt upgraden, voegt u er een **partijnummer** aan toe voordat u het upgradeproces start.</span><span class="sxs-lookup"><span data-stu-id="0ddba-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="0ddba-126">**Systeemstoring**: tijdens het upgradeproces moet u de omgevingen van Finance and Operations en Customer Engagement offline halen.</span><span class="sxs-lookup"><span data-stu-id="0ddba-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="0ddba-127">**Momentopname**: maak momentopnames van zowel Finance and Operations- als Customer Engagement-apps.</span><span class="sxs-lookup"><span data-stu-id="0ddba-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="0ddba-128">Gebruik de momentopnamen om de vorige status te herstellen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="0ddba-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="0ddba-129">Implementatie</span><span class="sxs-lookup"><span data-stu-id="0ddba-129">Deployment</span></span>

1. <span data-ttu-id="0ddba-130">Download de sjabloon van [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="0ddba-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="0ddba-131">Meld u aan bij [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="0ddba-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="0ddba-132">Maak een [resourcegroep](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="0ddba-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="0ddba-133">Maak een [opslagaccount](/azure/storage/common/storage-account-create?tabs=azure-portal) in de resourcegroep die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0ddba-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="0ddba-134">Maak een [data factory](/azure/data-factory/quickstart-create-data-factory-portal) boven de resourcegroep die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0ddba-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="0ddba-135">Open de data factory en selecteer de tegel **Author & Monitor**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="0ddba-136">Selecteer op het tabblad **Beheren** **ARM-sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="0ddba-137">Selecteer **ARM-sjabloon importeren** om de **partijsjabloon** te importeren.</span><span class="sxs-lookup"><span data-stu-id="0ddba-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="0ddba-138">Importeer de sjabloon in de data factory.</span><span class="sxs-lookup"><span data-stu-id="0ddba-138">Import the template into the data factory.</span></span> <span data-ttu-id="0ddba-139">Voer de volgende waarden in voor **Projectdetails** en **Exemplaardetails**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="0ddba-140">Veld</span><span class="sxs-lookup"><span data-stu-id="0ddba-140">Field</span></span> | <span data-ttu-id="0ddba-141">Waarde</span><span class="sxs-lookup"><span data-stu-id="0ddba-141">Value</span></span>
    ---|---
    <span data-ttu-id="0ddba-142">Abonnement</span><span class="sxs-lookup"><span data-stu-id="0ddba-142">Subscription</span></span> | <span data-ttu-id="0ddba-143">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="0ddba-143">Azure subscription</span></span>
    <span data-ttu-id="0ddba-144">Resourcegroep</span><span class="sxs-lookup"><span data-stu-id="0ddba-144">Resource group</span></span> | <span data-ttu-id="0ddba-145">Geef dezelfde resource op waaronder een opslagaccount wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0ddba-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="0ddba-146">Regio</span><span class="sxs-lookup"><span data-stu-id="0ddba-146">Region</span></span> | <span data-ttu-id="0ddba-147">Geef regio op.</span><span class="sxs-lookup"><span data-stu-id="0ddba-147">Specify region.</span></span>
    <span data-ttu-id="0ddba-148">Fabrieksnaam</span><span class="sxs-lookup"><span data-stu-id="0ddba-148">Factory Name</span></span> | <span data-ttu-id="0ddba-149">Geef de fabrieksnaam op.</span><span class="sxs-lookup"><span data-stu-id="0ddba-149">Specify factory name.</span></span>
    <span data-ttu-id="0ddba-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="0ddba-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="0ddba-151">Geef de sleutel van de toepassing op.</span><span class="sxs-lookup"><span data-stu-id="0ddba-151">Specify the application's key.</span></span>
    <span data-ttu-id="0ddba-152">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="0ddba-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="0ddba-153">Azure Blob storage connection string.</span><span class="sxs-lookup"><span data-stu-id="0ddba-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="0ddba-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="0ddba-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="0ddba-155">Het wachtwoord voor het gebruikersaccount dat u hebt opgegeven als gebruikersnaam.</span><span class="sxs-lookup"><span data-stu-id="0ddba-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="0ddba-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="0ddba-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="0ddba-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="0ddba-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="0ddba-158">Geef de tenant (domeinnaam of tenant-id) op waaronder de toepassing zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="0ddba-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="0ddba-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="0ddba-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="0ddba-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="0ddba-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="0ddba-161">Geef de client-id van de toepassing op.</span><span class="sxs-lookup"><span data-stu-id="0ddba-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="0ddba-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="0ddba-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="0ddba-163">De gebruikersnaam om verbinding te maken met Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0ddba-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="0ddba-164">Raadpleeg de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="0ddba-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="0ddba-165">Een Resource Manager-sjabloon handmatig een niveau verhogen voor elke omgeving</span><span class="sxs-lookup"><span data-stu-id="0ddba-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="0ddba-166">Eigenschappen van gekoppelde service</span><span class="sxs-lookup"><span data-stu-id="0ddba-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="0ddba-167">Gegevens kopiëren met Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="0ddba-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="0ddba-168">Valideer na de implementatie de gegevenssets, gegevensstroom en gekoppelde service van de data factory.</span><span class="sxs-lookup"><span data-stu-id="0ddba-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Gegevenssets, gegevensstroom en gekoppelde service](media/data-factory-validate.png)

11. <span data-ttu-id="0ddba-170">Navigeer naar **Beheren**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-170">Navigate to **Manage**.</span></span> <span data-ttu-id="0ddba-171">Selecteer **Gekoppelde service** onder **Verbindingen**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="0ddba-172">Selecteer **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="0ddba-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="0ddba-173">Voer in het formulier **Gekoppelde service bewerken (Dynamics CRM)** de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="0ddba-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="0ddba-174">Veld</span><span class="sxs-lookup"><span data-stu-id="0ddba-174">Field</span></span> | <span data-ttu-id="0ddba-175">Waarde</span><span class="sxs-lookup"><span data-stu-id="0ddba-175">Value</span></span>
    ---|---
    <span data-ttu-id="0ddba-176">Naam</span><span class="sxs-lookup"><span data-stu-id="0ddba-176">Name</span></span> | <span data-ttu-id="0ddba-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="0ddba-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="0ddba-178">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0ddba-178">Description</span></span> | <span data-ttu-id="0ddba-179">Gekoppelde services om verbinding te maken met CRM-exemplaar om entiteitengegevens op te halen</span><span class="sxs-lookup"><span data-stu-id="0ddba-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="0ddba-180">Verbinding maken via integratieruntime</span><span class="sxs-lookup"><span data-stu-id="0ddba-180">Connect via integration runtime</span></span> | <span data-ttu-id="0ddba-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0ddba-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="0ddba-182">Implementatietype</span><span class="sxs-lookup"><span data-stu-id="0ddba-182">Deployment type</span></span> | <span data-ttu-id="0ddba-183">Online</span><span class="sxs-lookup"><span data-stu-id="0ddba-183">Online</span></span>
    <span data-ttu-id="0ddba-184">Service-URI</span><span class="sxs-lookup"><span data-stu-id="0ddba-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="0ddba-185">Verificatietype</span><span class="sxs-lookup"><span data-stu-id="0ddba-185">Authentication type</span></span> | <span data-ttu-id="0ddba-186">Office365</span><span class="sxs-lookup"><span data-stu-id="0ddba-186">Office365</span></span>
    <span data-ttu-id="0ddba-187">Gebruikersnaam</span><span class="sxs-lookup"><span data-stu-id="0ddba-187">User name</span></span> |
    <span data-ttu-id="0ddba-188">Wachtwoord of Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="0ddba-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="0ddba-189">Wachtwoord</span><span class="sxs-lookup"><span data-stu-id="0ddba-189">Password</span></span>
    <span data-ttu-id="0ddba-190">Wachtwoord</span><span class="sxs-lookup"><span data-stu-id="0ddba-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="0ddba-191">De sjabloon uitvoeren</span><span class="sxs-lookup"><span data-stu-id="0ddba-191">Run the template</span></span>

1. <span data-ttu-id="0ddba-192">Stop de volgende toewijzingen voor twee keer wegschrijven voor **Account**, **Contactpersoon** en **Leverancier** met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="0ddba-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="0ddba-193">Klanten V3 (rekeningen)</span><span class="sxs-lookup"><span data-stu-id="0ddba-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="0ddba-194">Klanten V3(contacts)</span><span class="sxs-lookup"><span data-stu-id="0ddba-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="0ddba-195">CDS-contactpersonen V2(contacts)</span><span class="sxs-lookup"><span data-stu-id="0ddba-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="0ddba-196">CDS-contactpersonen V2(contacts)</span><span class="sxs-lookup"><span data-stu-id="0ddba-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="0ddba-197">Leverancier V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="0ddba-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="0ddba-198">Zorg ervoor dat de kaarten worden verwijderd uit de tabel `msdy_dualwriteruntimeconfig` in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ddba-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="0ddba-199">Installeer [de oplossingen voor twee keer wegschrijven naar Partij en Globaal adresboek](https://aka.ms/dual-write-gab) uit AppSource.</span><span class="sxs-lookup"><span data-stu-id="0ddba-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="0ddba-200">Als de volgende tabellen gegevens bevatten in de Finance and Operations-app, moet u **Initiële synchronisatie** uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="0ddba-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="0ddba-201">Aanhef</span><span class="sxs-lookup"><span data-stu-id="0ddba-201">Salutations</span></span>
    + <span data-ttu-id="0ddba-202">Persoonlijke karaktertypen</span><span class="sxs-lookup"><span data-stu-id="0ddba-202">Personal character types</span></span>
    + <span data-ttu-id="0ddba-203">Afsluiting</span><span class="sxs-lookup"><span data-stu-id="0ddba-203">Complimentary closing</span></span>
    + <span data-ttu-id="0ddba-204">Titels contactpersoon</span><span class="sxs-lookup"><span data-stu-id="0ddba-204">Contact person titles</span></span>
    + <span data-ttu-id="0ddba-205">Besluitvormingsrollen</span><span class="sxs-lookup"><span data-stu-id="0ddba-205">Decision making roles</span></span>
    + <span data-ttu-id="0ddba-206">Loyaliteitsniveaus</span><span class="sxs-lookup"><span data-stu-id="0ddba-206">Loyalty levels</span></span>

5. <span data-ttu-id="0ddba-207">Schakel in de Customer Engagement-app de volgende invoegtoepassingsstappen uit.</span><span class="sxs-lookup"><span data-stu-id="0ddba-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="0ddba-208">Account bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-208">Account Update</span></span>
         + <span data-ttu-id="0ddba-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update van account</span><span class="sxs-lookup"><span data-stu-id="0ddba-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="0ddba-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update van account</span><span class="sxs-lookup"><span data-stu-id="0ddba-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="0ddba-211">Contactpersoon bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-211">Contact Update</span></span>
         + <span data-ttu-id="0ddba-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="0ddba-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="0ddba-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="0ddba-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="0ddba-214">msdyn_party bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-214">msdyn_party Update</span></span>
         + <span data-ttu-id="0ddba-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update van msdyn_party</span><span class="sxs-lookup"><span data-stu-id="0ddba-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="0ddba-216">msdyn_vendor bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="0ddba-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update van msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="0ddba-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="0ddba-218">Schakel in de app voor klantbetrokkenheid de volgende werkstromen uit:</span><span class="sxs-lookup"><span data-stu-id="0ddba-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="0ddba-219">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="0ddba-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="0ddba-220">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="0ddba-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="0ddba-221">Leveranciers van het type Persoon maken in de tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="0ddba-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="0ddba-222">Leveranciers van het type Persoon maken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="0ddba-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="0ddba-223">Leveranciers bijwerken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="0ddba-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="0ddba-224">Leveranciers bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="0ddba-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="0ddba-225">Leveranciers van het type Persoon bijwerken in tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="0ddba-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="0ddba-226">Leveranciers van het type Persoon bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="0ddba-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="0ddba-227">Voer in de data factory de sjabloon uit door **Trigger nu** te selecteren zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="0ddba-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="0ddba-228">Dit proces kan enkele uren duren op basis van het gegevensvolume.</span><span class="sxs-lookup"><span data-stu-id="0ddba-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Triggeruitvoering](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="0ddba-230">Als u aanpassingen hebt voor **Account**, **Contactpersoon** en **Leverancier**, moet u de sjabloon wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0ddba-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="0ddba-231">Importeer de **nieuwe records voor Partij** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="0ddba-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="0ddba-232">Download het bestand `FONewParty.csv` vanuit Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="0ddba-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="0ddba-233">Het pad is `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="0ddba-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="0ddba-234">Converteer het bestand `FONewParty.csv` naar een Excel-bestand en importeer het Excel-bestand in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="0ddba-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="0ddba-235">Als de CSV-import voor u werkt, kunt u het CSV-bestand direct importeren.</span><span class="sxs-lookup"><span data-stu-id="0ddba-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="0ddba-236">Afhankelijk van het gegevensvolume kan het importeren enkele uren duren.</span><span class="sxs-lookup"><span data-stu-id="0ddba-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="0ddba-237">Meer informatie vindt u in [Overzicht van gegevensimport- en exporttaken](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="0ddba-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![De partijrecords van Dataverse importeren](media/data-factory-import-party.png)

9. <span data-ttu-id="0ddba-239">Schakel in de Customer Engagement-apps de volgende invoegtoepassingsstappen in:</span><span class="sxs-lookup"><span data-stu-id="0ddba-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="0ddba-240">Account bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-240">Account Update</span></span>
         + <span data-ttu-id="0ddba-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update van account</span><span class="sxs-lookup"><span data-stu-id="0ddba-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="0ddba-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update van account</span><span class="sxs-lookup"><span data-stu-id="0ddba-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="0ddba-243">Contactpersoon bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-243">Contact Update</span></span>
         + <span data-ttu-id="0ddba-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="0ddba-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="0ddba-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="0ddba-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="0ddba-246">msdyn_party bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-246">msdyn_party Update</span></span>
         + <span data-ttu-id="0ddba-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update van msdyn_party</span><span class="sxs-lookup"><span data-stu-id="0ddba-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="0ddba-248">msdyn_vendor bijwerken</span><span class="sxs-lookup"><span data-stu-id="0ddba-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="0ddba-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update van msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="0ddba-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="0ddba-250">Activeer in de apps voor klantbetrokkenheid de volgende werkstromen als u ze in vorige stappen hebt uitgeschakeld:</span><span class="sxs-lookup"><span data-stu-id="0ddba-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="0ddba-251">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="0ddba-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="0ddba-252">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="0ddba-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="0ddba-253">Leveranciers van het type Persoon maken in de tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="0ddba-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="0ddba-254">Leveranciers van het type Persoon maken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="0ddba-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="0ddba-255">Leveranciers bijwerken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="0ddba-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="0ddba-256">Leveranciers bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="0ddba-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="0ddba-257">Leveranciers van het type Persoon bijwerken in tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="0ddba-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="0ddba-258">Leveranciers van het type Persoon bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="0ddba-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="0ddba-259">Voer de **partij**-gerelateerde kaarten uit, zoals wordt aangegeven in [Partij en globaal adresboek](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="0ddba-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="0ddba-260">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="0ddba-260">Troubleshooting</span></span>

1. <span data-ttu-id="0ddba-261">Als het proces mislukt, moet u de data factory opnieuw starten vanaf de mislukte activiteit.</span><span class="sxs-lookup"><span data-stu-id="0ddba-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="0ddba-262">Sommige bestanden worden gegenereerd door de data factory. U kunt deze gebruiken om gegevens te valideren.</span><span class="sxs-lookup"><span data-stu-id="0ddba-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="0ddba-263">De data factory wordt uitgevoerd op basis van csv-bestanden met door komma's gescheiden waarden.</span><span class="sxs-lookup"><span data-stu-id="0ddba-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="0ddba-264">Als er een veldwaarde is met komma's, kan dit invloed hebben op de resultaten.</span><span class="sxs-lookup"><span data-stu-id="0ddba-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="0ddba-265">U moet de komma's verwijderen.</span><span class="sxs-lookup"><span data-stu-id="0ddba-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="0ddba-266">Het tabblad **Controle** bevat informatie over alle stappen en verwerkte gegevens.</span><span class="sxs-lookup"><span data-stu-id="0ddba-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="0ddba-267">Hier kunt u een specifieke stap selecteren voor foutopsporing.</span><span class="sxs-lookup"><span data-stu-id="0ddba-267">Select a specific step to debug it.</span></span>

    ![Tabblad Controle](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="0ddba-269">Meer informatie over de sjabloon</span><span class="sxs-lookup"><span data-stu-id="0ddba-269">Learn more about the template</span></span>

<span data-ttu-id="0ddba-270">U kunt extra informatie over de sjabloon vinden in het [leesmij-bestand Opmerkingen voor Azure Data Factory-sjabloon ](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="0ddba-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
