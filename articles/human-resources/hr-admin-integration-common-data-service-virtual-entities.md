---
title: Virtuele Dataverse-tabellen configureren
description: In dit onderwerp wordt beschreven hoe u virtuele tabellen configureert voor Dynamics 365 Human Resources. Genereer bestaande virtuele tabellen, werk ze bij en analyseer gegenereerde en beschikbare tabellen.
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
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae36f1436ddd7f41bf0c3510b47cbc440224f484
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890047"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="ccd4c-104">Virtuele Dataverse-tabellen configureren</span><span class="sxs-lookup"><span data-stu-id="ccd4c-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ccd4c-105">Dynamics 365 Human Resources is een virtuele gegevensbron in Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="ccd4c-106">De gegevensbron biedt volledige bewerkingen voor maken, lezen, bijwerken en verwijderen vanuit Dataverse en Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="ccd4c-107">De gegevens voor virtuele tabellen worden niet opgeslagen in Dataverse, maar in de toepassingsdatabase.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="ccd4c-108">Als u bewerkingen voor maken, lezen, bijwerken en verwijderen voor entiteiten van Human Resources wilt inschakelen vanuit Dataverse, moet u de entiteiten beschikbaar maken als virtuele tabellen in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="ccd4c-109">Op deze manier kunt u bewerkingen voor maken, lezen, bijwerken en verwijderen uitvoeren vanuit Dataverse en Microsoft Power Platform op gegevens in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="ccd4c-110">De bewerkingen ondersteunen ook de validaties van de volledige bedrijfslogica van Human Resources om de gegevensintegriteit te waarborgen bij het schrijven van gegevens naar de entiteiten.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd4c-111">Human Resources-entiteiten komen overeen met Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="ccd4c-112">Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="ccd4c-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="ccd4c-113">Beschikbare virtuele tabellen voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="ccd4c-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="ccd4c-114">Alle OData-entiteiten (Open Data Protocol) in Human Resources zijn beschikbaar als virtuele tabellen in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="ccd4c-115">Ze zijn ook beschikbaar in Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-115">They're also available in Power Platform.</span></span> <span data-ttu-id="ccd4c-116">U kunt nu apps en ervaringen met gegevens rechtstreeks vanuit Human Resources maken met alle mogelijkheden voor maken, lezen, bijwerken en verwijderen, zonder dat u gegevens hoeft te kopiëren of synchroniseren naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="ccd4c-117">U kunt Power Apps-portals gebruiken om extern gerichte websites te maken die samenwerkingsscenario's mogelijk maken voor bedrijfsprocessen in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="ccd4c-118">U kunt de lijst met virtuele tabellen die in de omgeving zijn ingeschakeld, weergeven en in [Power Apps](https://make.powerapps.com) met de tabellen gaan werken in de oplossing **Dynamics 365 HR Virtual Tables**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR Virtual Tables in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="ccd4c-120">Virtuele tabellen versus native tabellen</span><span class="sxs-lookup"><span data-stu-id="ccd4c-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="ccd4c-121">Virtuele tabellen voor Human Resources zijn niet hetzelfde als de native Dataverse-tabellen die voor Human Resources zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="ccd4c-122">De native tabellen voor Human Resources worden afzonderlijk gegenereerd en onderhouden in de HCM Common-oplossing in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="ccd4c-123">Met native tabellen worden de gegevens opgeslagen in Dataverse en is synchronisatie met de Human Resources-toepassingdatabase vereist.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd4c-124">Zie [Dataverse-tabellen](./hr-developer-entities.md) voor een lijst met de native Dataverse-tabellen voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="ccd4c-125">Instelling</span><span class="sxs-lookup"><span data-stu-id="ccd4c-125">Setup</span></span>

<span data-ttu-id="ccd4c-126">Volg deze instellingsstappen om virtuele tabellen in uw omgeving in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="ccd4c-127">Virtuele tabellen in Human Resources inschakelen</span><span class="sxs-lookup"><span data-stu-id="ccd4c-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="ccd4c-128">Eerst moet u virtuele tabellen inschakelen in de werkruimte **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="ccd4c-129">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="ccd4c-130">Selecteer de tegel **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="ccd4c-131">Selecteer **Ondersteuning van virtuele tabellen voor HR in Dataverse** en selecteer **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="ccd4c-132">Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van previewfuncties.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="ccd4c-133">De app registreren in Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="ccd4c-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="ccd4c-134">U moet uw Human Resources-exemplaar registreren in de Azure-portal, zodat het Microsoft-identiteitsplatform verificatie- en machtigingsservices kan bieden voor de app en de gebruikers.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="ccd4c-135">Ga voor meer informatie over het registreren van apps in Azure naar [Snelstart: Een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="ccd4c-136">Open de [Microsoft Azure-portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="ccd4c-137">Selecteer in de lijst Azure-services de optie **App-registraties**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="ccd4c-138">Selecteer **Nieuwe registratie**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-138">Select **New registration**.</span></span>

4. <span data-ttu-id="ccd4c-139">Voer in het veld **Naam** een beschrijvende naam voor de app in.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="ccd4c-140">Bijvoorbeeld, **Dynamics 365 Human Resources Virtuele tabellen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="ccd4c-141">Voer in het veld **URI omleiden** de naamruimte-URL in van uw instantie van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="ccd4c-142">Selecteer **Registreren**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-142">Select **Register**.</span></span>

7. <span data-ttu-id="ccd4c-143">Wanneer de registratie is voltooid, wordt in de Azure-portal het deelvenster **Overzicht** van de app-registratie weergegeven met de bijbehorende **Id van toepassing (client)**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="ccd4c-144">Maak nu een notitie van de **Id van toepassing (client)**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="ccd4c-145">U voert deze gegevens in wanneer u [de gegevensbron van de virtuele tabel configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="ccd4c-146">Selecteer in het linkernavigatievenster de optie **Certificaten en geheimen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="ccd4c-147">Selecteer in het gedeelte **Clientgeheimen** van de pagina de optie **Nieuw clientgeheim**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="ccd4c-148">Geef een omschrijving op, selecteer een duur en selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="ccd4c-149">Registreer de waarde van het geheim uit de eigenschap **Waarde** van de tabel.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="ccd4c-150">U voert deze gegevens in wanneer u [de gegevensbron van de virtuele tabel configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ccd4c-151">Maak nu een notitie van de waarde van het geheim.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="ccd4c-152">Het geheim wordt nooit meer weergegeven nadat u deze pagina hebt verlaten.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="ccd4c-153">De Dynamics 365 HR Virtual Table-app installeren</span><span class="sxs-lookup"><span data-stu-id="ccd4c-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="ccd4c-154">Installeer de Dynamics 365 HR Virtual Table-app in uw Power Apps-omgeving om het pakket van de virtuele tabel te implementeren naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="ccd4c-155">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="ccd4c-156">Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="ccd4c-157">Selecteer in het gedeelte **Resources** van de pagina de optie **Dynamics 365-apps**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="ccd4c-158">Selecteer de actie **App installeren**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="ccd4c-159">Selecteer **Dynamics 365 HR Virtual Table** en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="ccd4c-160">Controleer en markeer om de servicevoorwaarden te accepteren.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="ccd4c-161">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-161">Select **Install**.</span></span>

<span data-ttu-id="ccd4c-162">De installatie duurt een paar minuten.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-162">The install takes a few minutes.</span></span> <span data-ttu-id="ccd4c-163">Wanneer de installatie is voltooid, gaat u door naar de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-163">When it completes, continue to the next steps.</span></span>

![De Dynamics 365 HR Virtual Table-app installeren vanuit het Power Platform-beheercentrum](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="ccd4c-165">De gegevensbron van de virtuele tabel configureren</span><span class="sxs-lookup"><span data-stu-id="ccd4c-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="ccd4c-166">In de volgende stap configureert u de gegevensbron van de virtuele tabel in de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="ccd4c-167">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="ccd4c-168">Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="ccd4c-169">Selecteer de **Omgevings-URL** in het gedeelte **Details** van de pagina.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="ccd4c-170">Selecteer op de **Oplossingsstatushub** het pictogram **Geavanceerd zoeken** in de rechtsbovenhoek van de toepassingspagina.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="ccd4c-171">Selecteer op de pagina **Geavanceerd zoeken** in de vervolgkeuzelijst **Zoeken naar** de optie **Finance and Operations Virtual Data Source Configurations**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="ccd4c-172">Selecteer **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-172">Select **Results**.</span></span>

7. <span data-ttu-id="ccd4c-173">Selecteer de record **Microsoft HR-gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="ccd4c-174">Voer de vereiste informatie in voor de gegevensbronconfiguratie:</span><span class="sxs-lookup"><span data-stu-id="ccd4c-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="ccd4c-175">**Doel-URL** : de URL van uw Human Resources-naamruimte.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="ccd4c-176">De doel-URL heeft het volgende formaat:</span><span class="sxs-lookup"><span data-stu-id="ccd4c-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="ccd4c-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="ccd4c-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="ccd4c-178">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="ccd4c-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="ccd4c-179">Vergeet niet het "**/**"-teken aan het einde van de URL toe te voegen om te voorkomen dat er een fout optreedt.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="ccd4c-180">**Tenant-id**: de tenant-id van Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="ccd4c-181">**AAD-toepassings-id** : de toepassings-id (client) die is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="ccd4c-182">U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="ccd4c-183">**AAD-toepassingsgeheim**: het clientgeheim dat is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="ccd4c-184">U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="ccd4c-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-gegevensbron](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="ccd4c-186">Selecteer **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="ccd4c-187">App-machtigingen verlenen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="ccd4c-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="ccd4c-188">Verleen als volgt machtigingen voor de twee Azure AD-toepassingen in Human Resources:</span><span class="sxs-lookup"><span data-stu-id="ccd4c-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="ccd4c-189">De app die is gemaakt voor uw tenant in de Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="ccd4c-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="ccd4c-190">De Dynamics 365 HR Virtual Table-app die is geïnstalleerd in de Power Apps-omgeving</span><span class="sxs-lookup"><span data-stu-id="ccd4c-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="ccd4c-191">Open in Human Resources de pagina **Azure Active Directory-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="ccd4c-192">Selecteer **Nieuw** om een nieuwe toepassingsrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="ccd4c-193">Voer in het veld **Client-id** de client-id in van de app die u in de Microsoft Azure-portal hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="ccd4c-194">Voer in het veld **Naam** de naam in van de app die u in de Microsoft Azure-portal hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="ccd4c-195">Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="ccd4c-196">Selecteer **Nieuw** om een tweede toepassingsrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="ccd4c-197">**Client-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="ccd4c-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="ccd4c-198">**Naam**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="ccd4c-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="ccd4c-199">Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="ccd4c-200">Virtuele tabellen genereren</span><span class="sxs-lookup"><span data-stu-id="ccd4c-200">Generate virtual tables</span></span>

<span data-ttu-id="ccd4c-201">Wanneer het instellen is voltooid, kunt u de virtuele tabellen selecteren die u in uw Dataverse-exemplaar wilt genereren en inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="ccd4c-202">Open in Human Resources de pagina **Integratie met Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="ccd4c-203">Selecteer het tabblad **Virtuele tabellen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd4c-204">De wisselknop **Virtuele tabellen inschakelen** wordt automatisch ingesteld op **Ja** als alle vereiste instellingen zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="ccd4c-205">Als de wisselknop is ingesteld op **Nee**, controleert u de stappen in vorige secties van dit document om ervoor te zorgen dat alle vereiste instellingen worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="ccd4c-206">Selecteer de tabel of tabellen die u wilt genereren in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="ccd4c-207">Selecteer **Genereren/vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-207">Select **Generate/refresh**.</span></span>

![Integratie met Dataverse](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="ccd4c-209">Status van het genereren van tabellen controleren</span><span class="sxs-lookup"><span data-stu-id="ccd4c-209">Check table generation status</span></span>

<span data-ttu-id="ccd4c-210">Virtuele tabellen worden gegenereerd in Dataverse via een asynchroon achtergrondproces.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="ccd4c-211">Updates in de procesweergave in het actiecentrum.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="ccd4c-212">Details over het proces, waaronder foutlogboeken, worden weergegeven op de pagina **Procesautomatiseringen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="ccd4c-213">Open in Human Resources de pagina **Procesautomatiseringen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="ccd4c-214">Selecteer het tabblad **Achtergrondprocessen**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="ccd4c-215">Selecteer **Achtergrondproces voor asynchrone bewerking van controle van virtuele tabel**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="ccd4c-216">Selecteer **Meest recente resultaten weergeven**.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-216">Select **View most recent results**.</span></span>

<span data-ttu-id="ccd4c-217">In het uitschuifvenster worden de meest recente uitvoeringsresultaten voor het proces weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="ccd4c-218">U kunt het logboek voor het proces weergeven, inclusief eventuele fouten die worden geretourneerd van Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ccd4c-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccd4c-219">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ccd4c-219">See also</span></span>

[<span data-ttu-id="ccd4c-220">Wat is Dataverse?</span><span class="sxs-lookup"><span data-stu-id="ccd4c-220">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="ccd4c-221">Tabellen in Dataverse</span><span class="sxs-lookup"><span data-stu-id="ccd4c-221">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="ccd4c-222">Overzicht van tabelrelaties</span><span class="sxs-lookup"><span data-stu-id="ccd4c-222">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="ccd4c-223">Virtuele tabellen maken en bewerken die gegevens uit een externe gegevensbron bevatten</span><span class="sxs-lookup"><span data-stu-id="ccd4c-223">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="ccd4c-224">Wat zijn Power Apps-portals?</span><span class="sxs-lookup"><span data-stu-id="ccd4c-224">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="ccd4c-225">Overzicht van het maken van apps in Power Apps</span><span class="sxs-lookup"><span data-stu-id="ccd4c-225">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]