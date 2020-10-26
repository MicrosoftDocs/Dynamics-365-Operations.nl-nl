---
title: Virtuele Common Data Service-entiteiten configureren
description: In dit onderwerp wordt beschreven hoe u virtuele entiteiten configureert voor Dynamics 365 Human Resources. Genereer bestaande virtuele entiteiten, werk ze bij en analyseer gegenereerde en beschikbare entiteiten.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959570"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="e1b5c-104">Virtuele Common Data Service-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="e1b5c-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e1b5c-105">Dynamics 365 Human Resources is een virtuele gegevensbron in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="e1b5c-106">De gegevensbron biedt volledige bewerkingen voor maken, lezen, bijwerken en verwijderen vanuit Common Data Service en Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="e1b5c-107">De gegevens voor virtuele entiteiten worden niet opgeslagen in Common Data Service, maar in de toepassingsdatabase.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="e1b5c-108">Als u bewerkingen voor maken, lezen, bijwerken en verwijderen voor entiteiten van Human Resources wilt inschakelen vanuit Common Data Service, moet u de entiteiten beschikbaar maken als virtuele entiteiten in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="e1b5c-109">Op deze manier kunt u bewerkingen voor maken, lezen, bijwerken en verwijderen uitvoeren vanuit Common Data Service en Microsoft Power Platform op gegevens in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="e1b5c-110">De bewerkingen ondersteunen ook de validaties van de volledige bedrijfslogica van Human Resources om de gegevensintegriteit te waarborgen bij het schrijven van gegevens naar de entiteiten.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="e1b5c-111">Beschikbare virtuele entiteiten voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="e1b5c-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="e1b5c-112">Alle OData-entiteiten (Open Data Protocol) in Human Resources zijn beschikbaar als virtuele entiteiten in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="e1b5c-113">Ze zijn ook beschikbaar in Power Platform.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-113">They're also available in Power Platform.</span></span> <span data-ttu-id="e1b5c-114">U kunt nu apps en ervaringen met gegevens rechtstreeks vanuit Human Resources maken met alle mogelijkheden voor maken, lezen, bijwerken en verwijderen, zonder dat u gegevens hoeft te kopiëren of synchroniseren naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="e1b5c-115">U kunt Power Apps-portals gebruiken om extern gerichte websites te maken die samenwerkingsscenario's mogelijk maken voor bedrijfsprocessen in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="e1b5c-116">U kunt de lijst met virtuele entiteiten die in de omgeving zijn ingeschakeld, weergeven en in [Power Apps](https://make.powerapps.com) met de entiteiten gaan werken in de oplossing **Dynamics 365 HR Virtual Entities**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR Virtual Entities in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="e1b5c-118">Virtuele entiteiten versus natuurlijke entiteiten</span><span class="sxs-lookup"><span data-stu-id="e1b5c-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="e1b5c-119">Virtuele entiteiten voor Human Resources zijn niet hetzelfde als de natuurlijke Common Data Service-entiteiten die voor Human Resources zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="e1b5c-120">De natuurlijke entiteiten voor Human Resources worden afzonderlijk gegenereerd en onderhouden in de HCM Common-oplossing in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="e1b5c-121">Met natuurlijke entiteiten worden de gegevens opgeslagen in Common Data Service en is synchronisatie met de Human Resources-toepassingdatabase vereist.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="e1b5c-122">Zie [Common Data Service-entiteiten](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities) voor een lijst met de natuurlijke Common Data Service-entiteiten voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="e1b5c-123">Instelling</span><span class="sxs-lookup"><span data-stu-id="e1b5c-123">Setup</span></span>

<span data-ttu-id="e1b5c-124">Volg deze instellingsstappen om virtuele entiteiten in uw omgeving in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="e1b5c-125">De app registreren in Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="e1b5c-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="e1b5c-126">U moet de app eerst registreren in de Azure-portal, zodat het Microsoft-identiteitsplatform verificatie- en machtigingsservices kan bieden voor de app en de gebruikers.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="e1b5c-127">Ga voor meer informatie over het registreren van apps in Azure naar [Snelstart: Een toepassing registreren bij het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="e1b5c-128">Open de [Microsoft Azure-portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="e1b5c-129">Selecteer in de lijst Azure-services de optie **App-registraties**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="e1b5c-130">Selecteer **Nieuwe registratie**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-130">Select **New registration**.</span></span>

4. <span data-ttu-id="e1b5c-131">Voer in het veld **Naam** een beschrijvende naam voor de app in.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="e1b5c-132">Bijvoorbeeld, **Dynamics 365 Human Resources Virtuele entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="e1b5c-133">Voer in het veld **URI omleiden** de naamruimte-URL in van uw instantie van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="e1b5c-134">Selecteer **Registreren**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-134">Select **Register**.</span></span>

7. <span data-ttu-id="e1b5c-135">Wanneer de registratie is voltooid, wordt in de Azure-portal het deelvenster **Overzicht** van de app-registratie weergegeven met de bijbehorende **Id van toepassing (client)**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="e1b5c-136">Maak nu een notitie van de **Id van toepassing (client)**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="e1b5c-137">U voert deze gegevens in wanneer u [de gegevensbron van de virtuele entiteit configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="e1b5c-138">Selecteer in het linkernavigatievenster de optie **Certificaten en geheimen**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="e1b5c-139">Selecteer in het gedeelte **Clientgeheimen** van de pagina de optie **Nieuw clientgeheim**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="e1b5c-140">Geef een omschrijving op, selecteer een duur en selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="e1b5c-141">Leg de waarde van het geheim vast.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-141">Record the secret's value.</span></span> <span data-ttu-id="e1b5c-142">U voert deze gegevens in wanneer u [de gegevensbron van de virtuele entiteit configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e1b5c-143">Maak nu een notitie van de waarde van het geheim.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="e1b5c-144">Het geheim wordt nooit meer weergegeven nadat u deze pagina hebt verlaten.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="e1b5c-145">De Dynamics 365 HR Virtual Entity-app installeren</span><span class="sxs-lookup"><span data-stu-id="e1b5c-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="e1b5c-146">Installeer de Dynamics 365 HR Virtual Entity-app in uw Power Apps-omgeving om het pakket van de virtuele entiteit te implementeren naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="e1b5c-147">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="e1b5c-148">Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="e1b5c-149">Selecteer in het gedeelte **Resources** van de pagina de optie **Dynamics 365-apps**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="e1b5c-150">Selecteer de actie **App installeren**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="e1b5c-151">Selecteer **Dynamics 365 HR Virtual Entity** en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="e1b5c-152">Controleer en markeer om de servicevoorwaarden te accepteren.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="e1b5c-153">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-153">Select **Install**.</span></span>

<span data-ttu-id="e1b5c-154">De installatie duurt een paar minuten.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-154">The install takes a few minutes.</span></span> <span data-ttu-id="e1b5c-155">Wanneer de installatie is voltooid, gaat u door naar de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-155">When it completes, continue to the next steps.</span></span>

![De Dynamics 365 HR Virtual Entity-app installeren vanuit het Power Platform-beheercentrum](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="e1b5c-157">De gegevensbron van de virtuele entiteit configureren</span><span class="sxs-lookup"><span data-stu-id="e1b5c-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="e1b5c-158">In de volgende stap configureert u de gegevensbron van de virtuele entiteit in de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="e1b5c-159">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="e1b5c-160">Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="e1b5c-161">Selecteer de **Omgevings-URL** in het gedeelte **Details** van de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="e1b5c-162">Selecteer op de **Oplossingsstatushub** het pictogram **Geavanceerd zoeken** in de rechtsbovenhoek van de toepassingspagina.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="e1b5c-163">Selecteer op de pagina **Geavanceerd zoeken** in de vervolgkeuzelijst **Zoeken naar** de optie **Finance and Operations Virtual Data Source Configurations**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="e1b5c-164">Selecteer **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-164">Select **Results**.</span></span>

7. <span data-ttu-id="e1b5c-165">Selecteer de record **Microsoft HR-gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="e1b5c-166">Voer de vereiste informatie in voor de gegevensbronconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="e1b5c-167">**Doel-URL** : de URL van uw Human Resources-naamruimte.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="e1b5c-168">**Tenant-id**: de tenant-id van Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="e1b5c-169">**AAD-toepassings-id** : de toepassings-id (client) die is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="e1b5c-170">U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="e1b5c-171">**AAD-toepassingsgeheim**: het clientgeheim dat is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="e1b5c-172">U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="e1b5c-173">Selecteer **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-173">Select **Save & Close**.</span></span>

   ![Microsoft HR-gegevensbron](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="e1b5c-175">App-machtigingen verlenen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="e1b5c-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="e1b5c-176">Verleen als volgt machtigingen voor de twee Azure AD-toepassingen in Human Resources:</span><span class="sxs-lookup"><span data-stu-id="e1b5c-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="e1b5c-177">De app die is gemaakt voor uw tenant in de Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="e1b5c-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="e1b5c-178">De Dynamics 365 HR Virtual Entity-app die is geïnstalleerd in de Power Apps-omgeving</span><span class="sxs-lookup"><span data-stu-id="e1b5c-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="e1b5c-179">Open in Human Resources de pagina **Azure Active Directory-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="e1b5c-180">Selecteer **Nieuw** om een nieuwe toepassingsrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="e1b5c-181">Voer in het veld **Client-id** de client-id in van de app die u in de Microsoft Azure-portal hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="e1b5c-182">Voer in het veld **Naam** de naam in van de app die u in de Microsoft Azure-portal hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="e1b5c-183">Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="e1b5c-184">Selecteer **Nieuw** om een tweede toepassingsrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="e1b5c-185">**Client-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="e1b5c-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="e1b5c-186">**Naam**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="e1b5c-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="e1b5c-187">Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="e1b5c-188">Virtuele entiteiten genereren</span><span class="sxs-lookup"><span data-stu-id="e1b5c-188">Generate virtual entities</span></span>

<span data-ttu-id="e1b5c-189">Wanneer het instellen is voltooid, kunt u de virtuele entiteiten selecteren die u in uw Common Data Service-exemplaar wilt genereren en inschakelen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="e1b5c-190">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="e1b5c-191">Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="e1b5c-192">Selecteer de **Omgevings-URL** in het gedeelte **Details** van de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="e1b5c-193">Selecteer in de **Oplossingsstatushub** het pictogram **Geavanceerd zoeken** in de rechtsbovenhoek van de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="e1b5c-194">Selecteer op de pagina **Geavanceerd zoeken** in de vervolgkeuzelijst **Zoeken naar** de optie **Beschikbare HR-entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="e1b5c-195">Gebruik de filteropties om naar de entiteit of entiteiten te zoeken die u wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="e1b5c-196">Selecteer een entiteit in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="e1b5c-197">Wijzig op de entiteitpagina de eigenschap **Is gegenereerd** in **Ja** voor de entiteit.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="e1b5c-198">Sla de entiteitpagina op en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="e1b5c-199">U kunt meerdere virtuele entiteiten tegelijk genereren op de pagina **Meerdere records wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="e1b5c-200">Selecteer meerdere records op de pagina en selecteer **Bewerken** op het lint.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="e1b5c-201">U kunt vervolgens de eigenschap **Is gegenereerd** wijzigen voor alle geselecteerde records.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Beschikbare HR-entiteiten](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="e1b5c-203">Om het proces van het genereren van virtuele entiteiten in toekomstige versies te stroom lijnen, wordt het proces uitgevoerd op een pagina in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1b5c-204">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e1b5c-204">See also</span></span>

[<span data-ttu-id="e1b5c-205">Wat is Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="e1b5c-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="e1b5c-206">Overzicht van entiteiten</span><span class="sxs-lookup"><span data-stu-id="e1b5c-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="e1b5c-207">Overzicht van entiteitsrelaties</span><span class="sxs-lookup"><span data-stu-id="e1b5c-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="e1b5c-208">Virtuele entiteiten maken en bewerken die gegevens uit een externe gegevensbron bevatten</span><span class="sxs-lookup"><span data-stu-id="e1b5c-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="e1b5c-209">Wat zijn Power Apps-portals?</span><span class="sxs-lookup"><span data-stu-id="e1b5c-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="e1b5c-210">Overzicht van het maken van apps in Power Apps</span><span class="sxs-lookup"><span data-stu-id="e1b5c-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
