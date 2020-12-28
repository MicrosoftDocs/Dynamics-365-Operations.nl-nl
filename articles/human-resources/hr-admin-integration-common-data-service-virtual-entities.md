---
title: Virtuele Common Data Service-entiteiten configureren
description: In dit onderwerp wordt beschreven hoe u virtuele entiteiten configureert voor Dynamics 365 Human Resources. Genereer bestaande virtuele entiteiten, werk ze bij en analyseer gegenereerde en beschikbare entiteiten.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645596"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="52507-104">Virtuele Common Data Service-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="52507-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="52507-105">Dynamics 365 Human Resources is een virtuele gegevensbron in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="52507-106">De gegevensbron biedt volledige bewerkingen voor maken, lezen, bijwerken en verwijderen vanuit Common Data Service en Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="52507-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="52507-107">De gegevens voor virtuele entiteiten worden niet opgeslagen in Common Data Service, maar in de toepassingsdatabase.</span><span class="sxs-lookup"><span data-stu-id="52507-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="52507-108">Als u bewerkingen voor maken, lezen, bijwerken en verwijderen voor entiteiten van Human Resources wilt inschakelen vanuit Common Data Service, moet u de entiteiten beschikbaar maken als virtuele entiteiten in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="52507-109">Op deze manier kunt u bewerkingen voor maken, lezen, bijwerken en verwijderen uitvoeren vanuit Common Data Service en Microsoft Power Platform op gegevens in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="52507-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="52507-110">De bewerkingen ondersteunen ook de validaties van de volledige bedrijfslogica van Human Resources om de gegevensintegriteit te waarborgen bij het schrijven van gegevens naar de entiteiten.</span><span class="sxs-lookup"><span data-stu-id="52507-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="52507-111">Beschikbare virtuele entiteiten voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="52507-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="52507-112">Alle OData-entiteiten (Open Data Protocol) in Human Resources zijn beschikbaar als virtuele entiteiten in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="52507-113">Ze zijn ook beschikbaar in Power Platform.</span><span class="sxs-lookup"><span data-stu-id="52507-113">They're also available in Power Platform.</span></span> <span data-ttu-id="52507-114">U kunt nu apps en ervaringen met gegevens rechtstreeks vanuit Human Resources maken met alle mogelijkheden voor maken, lezen, bijwerken en verwijderen, zonder dat u gegevens hoeft te kopiëren of synchroniseren naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="52507-115">U kunt Power Apps-portals gebruiken om extern gerichte websites te maken die samenwerkingsscenario's mogelijk maken voor bedrijfsprocessen in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="52507-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="52507-116">U kunt de lijst met virtuele entiteiten die in de omgeving zijn ingeschakeld, weergeven en in [Power Apps](https://make.powerapps.com) met de entiteiten gaan werken in de oplossing **Dynamics 365 HR Virtual Entities**.</span><span class="sxs-lookup"><span data-stu-id="52507-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR Virtual Entities in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="52507-118">Virtuele entiteiten versus natuurlijke entiteiten</span><span class="sxs-lookup"><span data-stu-id="52507-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="52507-119">Virtuele entiteiten voor Human Resources zijn niet hetzelfde als de natuurlijke Common Data Service-entiteiten die voor Human Resources zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="52507-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="52507-120">De natuurlijke entiteiten voor Human Resources worden afzonderlijk gegenereerd en onderhouden in de HCM Common-oplossing in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="52507-121">Met natuurlijke entiteiten worden de gegevens opgeslagen in Common Data Service en is synchronisatie met de Human Resources-toepassingdatabase vereist.</span><span class="sxs-lookup"><span data-stu-id="52507-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="52507-122">Zie [Common Data Service-entiteiten](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities) voor een lijst met de natuurlijke Common Data Service-entiteiten voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="52507-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="52507-123">Instelling</span><span class="sxs-lookup"><span data-stu-id="52507-123">Setup</span></span>

<span data-ttu-id="52507-124">Volg deze instellingsstappen om virtuele entiteiten in uw omgeving in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="52507-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="52507-125">Virtuele entiteiten in Human Resources inschakelen</span><span class="sxs-lookup"><span data-stu-id="52507-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="52507-126">Eerst moet u virtuele entiteiten inschakelen in de werkruimte **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="52507-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="52507-127">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="52507-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="52507-128">Selecteer de tegel **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="52507-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="52507-129">Selecteer **Ondersteuning van virtuele entiteit in HR/CDS** en selecteer **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="52507-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="52507-130">Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van previewfuncties.</span><span class="sxs-lookup"><span data-stu-id="52507-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="52507-131">De app registreren in Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="52507-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="52507-132">U moet uw Human Resources-exemplaar registreren in de Azure-portal, zodat het Microsoft-identiteitsplatform verificatie- en machtigingsservices kan bieden voor de app en de gebruikers.</span><span class="sxs-lookup"><span data-stu-id="52507-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="52507-133">Ga voor meer informatie over het registreren van apps in Azure naar [Snelstart: Een toepassing registreren bij het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="52507-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="52507-134">Open de [Microsoft Azure-portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="52507-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="52507-135">Selecteer in de lijst Azure-services de optie **App-registraties**.</span><span class="sxs-lookup"><span data-stu-id="52507-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="52507-136">Selecteer **Nieuwe registratie**.</span><span class="sxs-lookup"><span data-stu-id="52507-136">Select **New registration**.</span></span>

4. <span data-ttu-id="52507-137">Voer in het veld **Naam** een beschrijvende naam voor de app in.</span><span class="sxs-lookup"><span data-stu-id="52507-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="52507-138">Bijvoorbeeld, **Dynamics 365 Human Resources Virtuele entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="52507-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="52507-139">Voer in het veld **URI omleiden** de naamruimte-URL in van uw instantie van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="52507-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="52507-140">Selecteer **Registreren**.</span><span class="sxs-lookup"><span data-stu-id="52507-140">Select **Register**.</span></span>

7. <span data-ttu-id="52507-141">Wanneer de registratie is voltooid, wordt in de Azure-portal het deelvenster **Overzicht** van de app-registratie weergegeven met de bijbehorende **Id van toepassing (client)**.</span><span class="sxs-lookup"><span data-stu-id="52507-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="52507-142">Maak nu een notitie van de **Id van toepassing (client)**.</span><span class="sxs-lookup"><span data-stu-id="52507-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="52507-143">U voert deze gegevens in wanneer u [de gegevensbron van de virtuele entiteit configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="52507-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="52507-144">Selecteer in het linkernavigatievenster de optie **Certificaten en geheimen**.</span><span class="sxs-lookup"><span data-stu-id="52507-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="52507-145">Selecteer in het gedeelte **Clientgeheimen** van de pagina de optie **Nieuw clientgeheim**.</span><span class="sxs-lookup"><span data-stu-id="52507-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="52507-146">Geef een omschrijving op, selecteer een duur en selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="52507-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="52507-147">Leg de waarde van het geheim vast.</span><span class="sxs-lookup"><span data-stu-id="52507-147">Record the secret's value.</span></span> <span data-ttu-id="52507-148">U voert deze gegevens in wanneer u [de gegevensbron van de virtuele entiteit configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="52507-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="52507-149">Maak nu een notitie van de waarde van het geheim.</span><span class="sxs-lookup"><span data-stu-id="52507-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="52507-150">Het geheim wordt nooit meer weergegeven nadat u deze pagina hebt verlaten.</span><span class="sxs-lookup"><span data-stu-id="52507-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="52507-151">De Dynamics 365 HR Virtual Entity-app installeren</span><span class="sxs-lookup"><span data-stu-id="52507-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="52507-152">Installeer de Dynamics 365 HR Virtual Entity-app in uw Power Apps-omgeving om het pakket van de virtuele entiteit te implementeren naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="52507-153">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="52507-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="52507-154">Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="52507-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="52507-155">Selecteer in het gedeelte **Resources** van de pagina de optie **Dynamics 365-apps**.</span><span class="sxs-lookup"><span data-stu-id="52507-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="52507-156">Selecteer de actie **App installeren**.</span><span class="sxs-lookup"><span data-stu-id="52507-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="52507-157">Selecteer **Dynamics 365 HR Virtual Entity** en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="52507-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="52507-158">Controleer en markeer om de servicevoorwaarden te accepteren.</span><span class="sxs-lookup"><span data-stu-id="52507-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="52507-159">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="52507-159">Select **Install**.</span></span>

<span data-ttu-id="52507-160">De installatie duurt een paar minuten.</span><span class="sxs-lookup"><span data-stu-id="52507-160">The install takes a few minutes.</span></span> <span data-ttu-id="52507-161">Wanneer de installatie is voltooid, gaat u door naar de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="52507-161">When it completes, continue to the next steps.</span></span>

![De Dynamics 365 HR Virtual Entity-app installeren vanuit het Power Platform-beheercentrum](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="52507-163">De gegevensbron van de virtuele entiteit configureren</span><span class="sxs-lookup"><span data-stu-id="52507-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="52507-164">In de volgende stap configureert u de gegevensbron van de virtuele entiteit in de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="52507-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="52507-165">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="52507-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="52507-166">Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="52507-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="52507-167">Selecteer de **Omgevings-URL** in het gedeelte **Details** van de pagina.</span><span class="sxs-lookup"><span data-stu-id="52507-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="52507-168">Selecteer op de **Oplossingsstatushub** het pictogram **Geavanceerd zoeken** in de rechtsbovenhoek van de toepassingspagina.</span><span class="sxs-lookup"><span data-stu-id="52507-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="52507-169">Selecteer op de pagina **Geavanceerd zoeken** in de vervolgkeuzelijst **Zoeken naar** de optie **Finance and Operations Virtual Data Source Configurations**.</span><span class="sxs-lookup"><span data-stu-id="52507-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="52507-170">Selecteer **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="52507-170">Select **Results**.</span></span>

7. <span data-ttu-id="52507-171">Selecteer de record **Microsoft HR-gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="52507-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="52507-172">Voer de vereiste informatie in voor de gegevensbronconfiguratie:</span><span class="sxs-lookup"><span data-stu-id="52507-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="52507-173">**Doel-URL** : de URL van uw Human Resources-naamruimte.</span><span class="sxs-lookup"><span data-stu-id="52507-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="52507-174">De doel-URL heeft het volgende formaat:</span><span class="sxs-lookup"><span data-stu-id="52507-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="52507-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="52507-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="52507-176">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="52507-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="52507-177">Vergeet niet het "**/**"-teken aan het einde van de URL toe te voegen om te voorkomen dat er een fout optreedt.</span><span class="sxs-lookup"><span data-stu-id="52507-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="52507-178">**Tenant-id**: de tenant-id van Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="52507-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="52507-179">**AAD-toepassings-id** : de toepassings-id (client) die is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="52507-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="52507-180">U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="52507-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="52507-181">**AAD-toepassingsgeheim**: het clientgeheim dat is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="52507-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="52507-182">U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="52507-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-gegevensbron](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="52507-184">Selecteer **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="52507-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="52507-185">App-machtigingen verlenen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="52507-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="52507-186">Verleen als volgt machtigingen voor de twee Azure AD-toepassingen in Human Resources:</span><span class="sxs-lookup"><span data-stu-id="52507-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="52507-187">De app die is gemaakt voor uw tenant in de Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="52507-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="52507-188">De Dynamics 365 HR Virtual Entity-app die is geïnstalleerd in de Power Apps-omgeving</span><span class="sxs-lookup"><span data-stu-id="52507-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="52507-189">Open in Human Resources de pagina **Azure Active Directory-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="52507-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="52507-190">Selecteer **Nieuw** om een nieuwe toepassingsrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="52507-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="52507-191">Voer in het veld **Client-id** de client-id in van de app die u in de Microsoft Azure-portal hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="52507-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="52507-192">Voer in het veld **Naam** de naam in van de app die u in de Microsoft Azure-portal hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="52507-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="52507-193">Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="52507-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="52507-194">Selecteer **Nieuw** om een tweede toepassingsrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="52507-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="52507-195">**Client-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="52507-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="52507-196">**Naam**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="52507-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="52507-197">Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="52507-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="52507-198">Virtuele entiteiten genereren</span><span class="sxs-lookup"><span data-stu-id="52507-198">Generate virtual entities</span></span>

<span data-ttu-id="52507-199">Wanneer het instellen is voltooid, kunt u de virtuele entiteiten selecteren die u in uw Common Data Service-exemplaar wilt genereren en inschakelen.</span><span class="sxs-lookup"><span data-stu-id="52507-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="52507-200">Open in Human Resources de pagina **Integratie met Common Data Service (CDS)**.</span><span class="sxs-lookup"><span data-stu-id="52507-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="52507-201">Selecteer het tabblad **Virtuele entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="52507-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="52507-202">De wisselknop **De virtuele entiteit inschakelen** wordt automatisch ingesteld op **Ja** als alle vereiste instellingen zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="52507-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="52507-203">Als de wisselknop is ingesteld op **Nee**, controleert u de stappen in vorige secties van dit document om ervoor te zorgen dat alle vereiste instellingen worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="52507-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="52507-204">Selecteer de entiteit of entiteiten die u wilt genereren in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="52507-205">Selecteer **Genereren/vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="52507-205">Select **Generate/refresh**.</span></span>

![Integratie met Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="52507-207">Status van het genereren van entiteiten controleren</span><span class="sxs-lookup"><span data-stu-id="52507-207">Check entity generation status</span></span>

<span data-ttu-id="52507-208">Virtuele entiteiten worden gegenereerd in Common Data Service via een asynchroon achtergrondproces.</span><span class="sxs-lookup"><span data-stu-id="52507-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="52507-209">Updates in de procesweergave in het actiecentrum.</span><span class="sxs-lookup"><span data-stu-id="52507-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="52507-210">Details over het proces, waaronder foutlogboeken, worden weergegeven op de pagina **Procesautomatiseringen**.</span><span class="sxs-lookup"><span data-stu-id="52507-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="52507-211">Open in Human Resources de pagina **Procesautomatiseringen**.</span><span class="sxs-lookup"><span data-stu-id="52507-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="52507-212">Selecteer het tabblad **Achtergrondprocessen**.</span><span class="sxs-lookup"><span data-stu-id="52507-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="52507-213">Selecteer **Achtergrondproces voor asynchrone bewerking van controle van virtuele entiteit**.</span><span class="sxs-lookup"><span data-stu-id="52507-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="52507-214">Selecteer **Meest recente resultaten weergeven**.</span><span class="sxs-lookup"><span data-stu-id="52507-214">Select **View most recent results**.</span></span>

<span data-ttu-id="52507-215">In het uitschuifvenster worden de meest recente uitvoeringsresultaten voor het proces weergegeven.</span><span class="sxs-lookup"><span data-stu-id="52507-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="52507-216">U kunt het logboek voor het proces weergeven, inclusief eventuele fouten die worden geretourneerd van Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="52507-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="52507-217">Zie ook</span><span class="sxs-lookup"><span data-stu-id="52507-217">See also</span></span>

[<span data-ttu-id="52507-218">Wat is Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="52507-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="52507-219">Overzicht van entiteiten</span><span class="sxs-lookup"><span data-stu-id="52507-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="52507-220">Overzicht van entiteitsrelaties</span><span class="sxs-lookup"><span data-stu-id="52507-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="52507-221">Virtuele entiteiten maken en bewerken die gegevens uit een externe gegevensbron bevatten</span><span class="sxs-lookup"><span data-stu-id="52507-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="52507-222">Wat zijn Power Apps-portals?</span><span class="sxs-lookup"><span data-stu-id="52507-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="52507-223">Overzicht van het maken van apps in Power Apps</span><span class="sxs-lookup"><span data-stu-id="52507-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
