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
ms.openlocfilehash: 95472a00d34ba939ac89b4e2484f34d50bee3088
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018307"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="20a88-103">Bijwerken naar het model voor partij en globaal adresboek</span><span class="sxs-lookup"><span data-stu-id="20a88-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="20a88-104">Met de [Azure Data Factory-sjabloon](https://aka.ms/dual-write-gab-adf) kunt u bestaande tabelgegevens voor **Account**, **Contactpersoon** en **Leverancier** met twee keer wegschrijven upgraden naar het partij- en globale adresboekmodel.</span><span class="sxs-lookup"><span data-stu-id="20a88-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="20a88-105">De sjabloon stemt de gegevens van zowel Finance and Operations-apps als applicaties voor klantbetrokkenheid met elkaar af.</span><span class="sxs-lookup"><span data-stu-id="20a88-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="20a88-106">Aan het einde van het proces worden de velden **Partij** en **Contactpersoon** gemaakt voor **partijrecords** en gekoppeld aan **account-**, **contactpersoon-** en **leveranciers** records in klantbetrokkenheidstoepassingen.</span><span class="sxs-lookup"><span data-stu-id="20a88-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="20a88-107">Er wordt een .csv bestand (`FONewParty.csv`) gegenereerd om nieuwe **partijrecords** te maken in de app Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="20a88-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="20a88-108">Dit onderwerp bevat de instructies voor het gebruik van de Data Factory-sjabloon en het upgraden van uw gegevens.</span><span class="sxs-lookup"><span data-stu-id="20a88-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="20a88-109">Als u geen aanpassingen hebt, kunt u de sjabloon gebruiken zoals deze is.</span><span class="sxs-lookup"><span data-stu-id="20a88-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="20a88-110">Als u aanpassingen hebt voor **Account**, **Contactpersoon** en **Leverancier**, moet u de sjabloon wijzigen met behulp van de volgende instructies.</span><span class="sxs-lookup"><span data-stu-id="20a88-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="20a88-111">De sjabloon helpt om alleen bij het upgraden van de **partijgegevens**.</span><span class="sxs-lookup"><span data-stu-id="20a88-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="20a88-112">In een toekomstige release zullen post- en elektronische adressen worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="20a88-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="20a88-113">Vereisten</span><span class="sxs-lookup"><span data-stu-id="20a88-113">Prerequisites</span></span>

<span data-ttu-id="20a88-114">Deze vereisten zijn van toepassing:</span><span class="sxs-lookup"><span data-stu-id="20a88-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="20a88-115">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="20a88-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="20a88-116">Toegang tot de sjabloon</span><span class="sxs-lookup"><span data-stu-id="20a88-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="20a88-117">U bent een bestaande klant voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="20a88-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="20a88-118">Upgrade voorbereiden</span><span class="sxs-lookup"><span data-stu-id="20a88-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="20a88-119">**Volledig gesynchroniseerd**: beide omgevingen zijn volledig gesynchroniseerd voor **Account (klant)**, **Contactpersoon** en **Leverancier**.</span><span class="sxs-lookup"><span data-stu-id="20a88-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="20a88-120">**Integratiesleutels:** de tabellen **Account (klant)**, **Contactpersoon** en **Leverancier** in apps voor klantbetrokkenheid gebruiken de integratiesleutels die met het product worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="20a88-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="20a88-121">Als u de integratiesleutels hebt aangepast, moet u de sjabloon aanpassen.</span><span class="sxs-lookup"><span data-stu-id="20a88-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="20a88-122">**Partijnummer**: alle records van **Account (klant)**, **Contactpersoon** en **Leverancier** die worden bijgewerkt, hebben een **partijnummer**.</span><span class="sxs-lookup"><span data-stu-id="20a88-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="20a88-123">Records zonder **partijnummer** worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="20a88-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="20a88-124">Als u deze records wilt upgraden, voegt u er een **partijnummer** aan toe voordat u het upgradeproces start.</span><span class="sxs-lookup"><span data-stu-id="20a88-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="20a88-125">**Systeemstoring:** tijdens het upgradeproces moet u de omgevingen voor Finance and Operations en klantbetrokkenheid offline halen.</span><span class="sxs-lookup"><span data-stu-id="20a88-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="20a88-126">**Momentopname:** maak momentopnames van apps voor Finance and Operations en klantbetrokkenheid.</span><span class="sxs-lookup"><span data-stu-id="20a88-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="20a88-127">Gebruik de momentopnamen om de vorige status te herstellen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="20a88-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="20a88-128">Implementatie</span><span class="sxs-lookup"><span data-stu-id="20a88-128">Deployment</span></span>

1. <span data-ttu-id="20a88-129">Download de sjabloon van [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="20a88-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="20a88-130">Meld u aan bij [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="20a88-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="20a88-131">Maak een [resourcegroep](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="20a88-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="20a88-132">Maak een [opslagaccount](/azure/storage/common/storage-account-create?tabs=azure-portal) in de resourcegroep die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="20a88-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="20a88-133">Maak een [data factory](/azure/data-factory/quickstart-create-data-factory-portal) boven de resourcegroep die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="20a88-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="20a88-134">Open de data factory en selecteer de tegel **Author & Monitor**.</span><span class="sxs-lookup"><span data-stu-id="20a88-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="20a88-135">Selecteer op het tabblad **Beheren** **ARM-sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="20a88-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="20a88-136">Selecteer **ARM-sjabloon importeren** om de **partijsjabloon** te importeren.</span><span class="sxs-lookup"><span data-stu-id="20a88-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="20a88-137">Importeer de sjabloon in de data factory.</span><span class="sxs-lookup"><span data-stu-id="20a88-137">Import the template into the data factory.</span></span> <span data-ttu-id="20a88-138">Voer de volgende waarden in voor **Projectdetails** en **Exemplaardetails**.</span><span class="sxs-lookup"><span data-stu-id="20a88-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="20a88-139">Veld</span><span class="sxs-lookup"><span data-stu-id="20a88-139">Field</span></span> | <span data-ttu-id="20a88-140">Waarde</span><span class="sxs-lookup"><span data-stu-id="20a88-140">Value</span></span>
    ---|---
    <span data-ttu-id="20a88-141">Abonnement</span><span class="sxs-lookup"><span data-stu-id="20a88-141">Subscription</span></span> | <span data-ttu-id="20a88-142">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="20a88-142">Azure subscription</span></span>
    <span data-ttu-id="20a88-143">Resourcegroep</span><span class="sxs-lookup"><span data-stu-id="20a88-143">Resource group</span></span> | <span data-ttu-id="20a88-144">Geef dezelfde resource op waaronder een opslagaccount wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="20a88-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="20a88-145">Regio</span><span class="sxs-lookup"><span data-stu-id="20a88-145">Region</span></span> | <span data-ttu-id="20a88-146">Geef regio op.</span><span class="sxs-lookup"><span data-stu-id="20a88-146">Specify region.</span></span>
    <span data-ttu-id="20a88-147">Fabrieksnaam</span><span class="sxs-lookup"><span data-stu-id="20a88-147">Factory Name</span></span> | <span data-ttu-id="20a88-148">Geef de fabrieksnaam op.</span><span class="sxs-lookup"><span data-stu-id="20a88-148">Specify factory name.</span></span>
    <span data-ttu-id="20a88-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="20a88-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="20a88-150">Geef de sleutel van de toepassing op.</span><span class="sxs-lookup"><span data-stu-id="20a88-150">Specify the application's key.</span></span>
    <span data-ttu-id="20a88-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="20a88-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="20a88-152">Azure Blob storage connection string.</span><span class="sxs-lookup"><span data-stu-id="20a88-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="20a88-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="20a88-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="20a88-154">Het wachtwoord voor het gebruikersaccount dat u hebt opgegeven als gebruikersnaam.</span><span class="sxs-lookup"><span data-stu-id="20a88-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="20a88-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="20a88-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="20a88-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="20a88-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="20a88-157">Geef de tenant (domeinnaam of tenant-id) op waaronder de toepassing zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="20a88-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="20a88-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="20a88-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="20a88-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="20a88-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="20a88-160">Geef de client-id van de toepassing op.</span><span class="sxs-lookup"><span data-stu-id="20a88-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="20a88-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="20a88-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="20a88-162">De gebruikersnaam voor de verbinding met Dynamics.</span><span class="sxs-lookup"><span data-stu-id="20a88-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="20a88-163">Meer informatie vindt u in [Een Resource Manager-sjabloon handmatig een niveau verhogen voor elke omgeving](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Eigenschappen van gekoppelde service](/azure/data-factory/connector-dynamics-ax#linked-service-properties) en [Gegevens kopiëren met Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="20a88-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="20a88-164">Valideer na de implementatie de gegevenssets, gegevensstroom en gekoppelde service van de data factory.</span><span class="sxs-lookup"><span data-stu-id="20a88-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Gegevenssets, gegevensstroom en gekoppelde service](media/data-factory-validate.png)

11. <span data-ttu-id="20a88-166">Navigeer naar **Beheren**.</span><span class="sxs-lookup"><span data-stu-id="20a88-166">Navigate to **Manage**.</span></span> <span data-ttu-id="20a88-167">Selecteer **Gekoppelde service** onder **Verbindingen**.</span><span class="sxs-lookup"><span data-stu-id="20a88-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="20a88-168">Selecteer **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="20a88-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="20a88-169">Voer in het formulier **Gekoppelde service bewerken (Dynamics CRM)** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="20a88-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="20a88-170">Veld</span><span class="sxs-lookup"><span data-stu-id="20a88-170">Field</span></span> | <span data-ttu-id="20a88-171">Waarde</span><span class="sxs-lookup"><span data-stu-id="20a88-171">Value</span></span>
    ---|---
    <span data-ttu-id="20a88-172">Naam</span><span class="sxs-lookup"><span data-stu-id="20a88-172">Name</span></span> | <span data-ttu-id="20a88-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="20a88-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="20a88-174">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="20a88-174">Description</span></span> | <span data-ttu-id="20a88-175">Gekoppelde services om verbinding te maken met CRM-exemplaar om entiteitengegevens op te halen</span><span class="sxs-lookup"><span data-stu-id="20a88-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="20a88-176">Verbinding maken via integratieruntime</span><span class="sxs-lookup"><span data-stu-id="20a88-176">Connect via integration runtime</span></span> | <span data-ttu-id="20a88-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="20a88-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="20a88-178">Implementatietype</span><span class="sxs-lookup"><span data-stu-id="20a88-178">Deployment type</span></span> | <span data-ttu-id="20a88-179">Online</span><span class="sxs-lookup"><span data-stu-id="20a88-179">Online</span></span>
    <span data-ttu-id="20a88-180">Service-URI</span><span class="sxs-lookup"><span data-stu-id="20a88-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="20a88-181">Verificatietype</span><span class="sxs-lookup"><span data-stu-id="20a88-181">Authentication type</span></span> | <span data-ttu-id="20a88-182">Office365</span><span class="sxs-lookup"><span data-stu-id="20a88-182">Office365</span></span>
    <span data-ttu-id="20a88-183">Gebruikersnaam</span><span class="sxs-lookup"><span data-stu-id="20a88-183">User name</span></span> |
    <span data-ttu-id="20a88-184">Wachtwoord of Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="20a88-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="20a88-185">Wachtwoord</span><span class="sxs-lookup"><span data-stu-id="20a88-185">Password</span></span>
    <span data-ttu-id="20a88-186">Wachtwoord</span><span class="sxs-lookup"><span data-stu-id="20a88-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="20a88-187">De sjabloon uitvoeren</span><span class="sxs-lookup"><span data-stu-id="20a88-187">Run the template</span></span>

1. <span data-ttu-id="20a88-188">Stop twee keer wegschrijven voor de volgende **Account**, **Contactpersoon** en **Leverancier** met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="20a88-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="20a88-189">Klanten V3 (rekeningen)</span><span class="sxs-lookup"><span data-stu-id="20a88-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="20a88-190">Klanten V3(contacts)</span><span class="sxs-lookup"><span data-stu-id="20a88-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="20a88-191">CDS-contactpersonen V2(contacts)</span><span class="sxs-lookup"><span data-stu-id="20a88-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="20a88-192">CDS-contactpersonen V2(contacts)</span><span class="sxs-lookup"><span data-stu-id="20a88-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="20a88-193">Leverancier V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="20a88-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="20a88-194">Zorg ervoor dat de kaarten worden verwijderd uit de tabel `msdy_dualwriteruntimeconfig` in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="20a88-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="20a88-195">Installeer [de oplossingen voor twee keer wegschrijven naar Partij en Globaal adresboek](https://aka.ms/dual-write-gab) uit AppSource.</span><span class="sxs-lookup"><span data-stu-id="20a88-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="20a88-196">Als de volgende tabellen gegevens bevatten in de Finance and Operations-app, moet u **Initiële synchronisatie** uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="20a88-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="20a88-197">Aanhef</span><span class="sxs-lookup"><span data-stu-id="20a88-197">Salutations</span></span>
    + <span data-ttu-id="20a88-198">Persoonlijke karaktertypen</span><span class="sxs-lookup"><span data-stu-id="20a88-198">Personal character types</span></span>
    + <span data-ttu-id="20a88-199">Afsluiting</span><span class="sxs-lookup"><span data-stu-id="20a88-199">Complimentary closing</span></span>
    + <span data-ttu-id="20a88-200">Titels contactpersoon</span><span class="sxs-lookup"><span data-stu-id="20a88-200">Contact person titles</span></span>
    + <span data-ttu-id="20a88-201">Besluitvormingsrollen</span><span class="sxs-lookup"><span data-stu-id="20a88-201">Decision making roles</span></span>
    + <span data-ttu-id="20a88-202">Loyaliteitsniveaus</span><span class="sxs-lookup"><span data-stu-id="20a88-202">Loyalty levels</span></span>

5. <span data-ttu-id="20a88-203">Schakel in de app voor klantbetrokkenheid de volgende stappen voor de invoegvoeging uit.</span><span class="sxs-lookup"><span data-stu-id="20a88-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="20a88-204">Account bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-204">Account Update</span></span>
         + <span data-ttu-id="20a88-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update van account</span><span class="sxs-lookup"><span data-stu-id="20a88-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="20a88-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update van account</span><span class="sxs-lookup"><span data-stu-id="20a88-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="20a88-207">Contactpersoon bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-207">Contact Update</span></span>
         + <span data-ttu-id="20a88-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="20a88-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="20a88-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="20a88-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="20a88-210">msdyn_party bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-210">msdyn_party Update</span></span>
         + <span data-ttu-id="20a88-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update van msdyn_party</span><span class="sxs-lookup"><span data-stu-id="20a88-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="20a88-212">msdyn_vendor bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="20a88-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update van msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="20a88-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="20a88-214">Schakel in de app voor klantbetrokkenheid de volgende werkstromen uit:</span><span class="sxs-lookup"><span data-stu-id="20a88-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="20a88-215">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="20a88-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20a88-216">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="20a88-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20a88-217">Leveranciers van het type Persoon maken in de tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="20a88-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="20a88-218">Leveranciers van het type Persoon maken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="20a88-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="20a88-219">Leveranciers bijwerken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="20a88-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20a88-220">Leveranciers bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="20a88-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="20a88-221">Leveranciers van het type Persoon bijwerken in tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="20a88-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="20a88-222">Leveranciers van het type Persoon bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="20a88-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="20a88-223">Voer in de data factory de sjabloon uit door **Trigger nu** te selecteren zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="20a88-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="20a88-224">Dit proces kan enkele uren duren op basis van het gegevensvolume.</span><span class="sxs-lookup"><span data-stu-id="20a88-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Triggeruitvoering](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="20a88-226">Als u aanpassingen hebt voor **Account**, **Contactpersoon** en **Leverancier**, moet u de sjabloon wijzigen.</span><span class="sxs-lookup"><span data-stu-id="20a88-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="20a88-227">Importeer de **nieuwe records voor Partij** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="20a88-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="20a88-228">Download het bestand `FONewParty.csv` vanuit Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="20a88-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="20a88-229">Het pad is `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="20a88-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="20a88-230">Converteer het bestand `FONewParty.csv` naar een Excel-bestand en importeer het Excel-bestand in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="20a88-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="20a88-231">Als de CSV-import voor u werkt, kunt u het CSV-bestand direct importeren.</span><span class="sxs-lookup"><span data-stu-id="20a88-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="20a88-232">Afhankelijk van het gegevensvolume kan het importeren enkele uren duren.</span><span class="sxs-lookup"><span data-stu-id="20a88-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="20a88-233">Meer informatie vindt u in [Overzicht van gegevensimport- en exporttaken](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="20a88-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![De partijrecords van Dataverse importeren](media/data-factory-import-party.png)

9. <span data-ttu-id="20a88-235">Schakel in de apps voor klantbetrokkenheid de volgende stappen voor de invoegvoeging in:</span><span class="sxs-lookup"><span data-stu-id="20a88-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="20a88-236">Account bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-236">Account Update</span></span>
         + <span data-ttu-id="20a88-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update van account</span><span class="sxs-lookup"><span data-stu-id="20a88-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="20a88-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update van account</span><span class="sxs-lookup"><span data-stu-id="20a88-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="20a88-239">Contactpersoon bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-239">Contact Update</span></span>
         + <span data-ttu-id="20a88-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="20a88-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="20a88-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update van contactpersoon</span><span class="sxs-lookup"><span data-stu-id="20a88-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="20a88-242">msdyn_party bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-242">msdyn_party Update</span></span>
         + <span data-ttu-id="20a88-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update van msdyn_party</span><span class="sxs-lookup"><span data-stu-id="20a88-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="20a88-244">msdyn_vendor bijwerken</span><span class="sxs-lookup"><span data-stu-id="20a88-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="20a88-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update van msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="20a88-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="20a88-246">Activeer in de apps voor klantbetrokkenheid de volgende werkstromen als u ze in vorige stappen hebt uitgeschakeld:</span><span class="sxs-lookup"><span data-stu-id="20a88-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="20a88-247">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="20a88-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20a88-248">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="20a88-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20a88-249">Leveranciers van het type Persoon maken in de tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="20a88-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="20a88-250">Leveranciers van het type Persoon maken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="20a88-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="20a88-251">Leveranciers bijwerken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="20a88-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20a88-252">Leveranciers bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="20a88-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="20a88-253">Leveranciers van het type Persoon bijwerken in tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="20a88-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="20a88-254">Leveranciers van het type Persoon bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="20a88-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="20a88-255">Voer de **partij**-gerelateerde kaarten uit, zoals wordt aangegeven in [Partij en globaal adresboek](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="20a88-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="20a88-256">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="20a88-256">Troubleshooting</span></span>

1. <span data-ttu-id="20a88-257">Als het proces mislukt, moet u de data factory opnieuw starten vanaf de mislukte activiteit.</span><span class="sxs-lookup"><span data-stu-id="20a88-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="20a88-258">Sommige bestanden worden gegenereerd door de data factory. U kunt deze gebruiken om gegevens te valideren.</span><span class="sxs-lookup"><span data-stu-id="20a88-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="20a88-259">De data factory wordt uitgevoerd op basis van csv-bestanden met door komma's gescheiden waarden.</span><span class="sxs-lookup"><span data-stu-id="20a88-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="20a88-260">Als er een veldwaarde is met komma's, kan dit invloed hebben op de resultaten.</span><span class="sxs-lookup"><span data-stu-id="20a88-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="20a88-261">U moet de komma's verwijderen.</span><span class="sxs-lookup"><span data-stu-id="20a88-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="20a88-262">Het tabblad **Controle** bevat informatie over alle stappen en verwerkte gegevens.</span><span class="sxs-lookup"><span data-stu-id="20a88-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="20a88-263">Hier kunt u een specifieke stap selecteren voor foutopsporing.</span><span class="sxs-lookup"><span data-stu-id="20a88-263">Select a specific step to debug it.</span></span>

    ![Tabblad Controle](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="20a88-265">Meer informatie over de sjabloon</span><span class="sxs-lookup"><span data-stu-id="20a88-265">Learn more about the template</span></span>

<span data-ttu-id="20a88-266">U kunt opmerkingen voor de sjabloon vinden in het [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)-bestand.</span><span class="sxs-lookup"><span data-stu-id="20a88-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>