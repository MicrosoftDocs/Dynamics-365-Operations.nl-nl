---
title: Invoegtoepassing Voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor de zichtbaarheid van de voorraad installeert en configureert voor Dynamics 365 Supply Chain Management.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625060"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="57f04-103">Invoegtoepassing Voorraadzichtbaarheid</span><span class="sxs-lookup"><span data-stu-id="57f04-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="57f04-104">De invoegtoepassing voor de zichtbaarheid van de voorraad is een onafhankelijke en zeer schaalbare microservice waarmee real-time tracking van voorhanden voorraad wordt ingeschakeld om een globale weergave van de voorraadzichtbaarheid te genereren.</span><span class="sxs-lookup"><span data-stu-id="57f04-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="57f04-105">Alle informatie die betrekking heeft op de voorhanden voorraad, wordt in bijna real-time met behulp van SQL-integratie op laag niveau geëxporteerd naar de service.</span><span class="sxs-lookup"><span data-stu-id="57f04-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="57f04-106">Externe systemen openen de service via RESTful API's om informatie over voorhanden voorraad voor bepaalde sets dimensies op te vragen, waardoor een lijst met beschikbare voorhanden posities wordt opgehaald.</span><span class="sxs-lookup"><span data-stu-id="57f04-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="57f04-107">Voorraadzichtbaarheid is een microservice die is gebouwd op de Common Data Service, wat betekent dat u deze kunt uitbreiden door Power Apps te bouwen en Power BI toe te passen voor aangepaste functionaliteit om aan uw zakelijke vereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="57f04-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="57f04-108">Het is ook mogelijk om de index te upgraden om voorraadquery's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="57f04-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="57f04-109">Voorraadzichtbaarheid bevat configuratieopties waarmee de service kan worden geïntegreerd met systemen van derden.</span><span class="sxs-lookup"><span data-stu-id="57f04-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="57f04-110">De service ondersteunt de gestandaardiseerde voorraaddimensie, aangepaste uitbreidbaarheid en gestandaardiseerde, configureerbare berekende hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="57f04-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="57f04-111">In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor voorraadzichtbaarheid installeert en configureert voor Dynamics 365 Supply Chain Management en hoe u de API (Application Programming Interface) ervan gebruikt.</span><span class="sxs-lookup"><span data-stu-id="57f04-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="57f04-112">Invoegtoepassing Voorraadzichtbaarheid installeren</span><span class="sxs-lookup"><span data-stu-id="57f04-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="57f04-113">U moet de invoegtoepassing voor voorraadzichtbaarheid installeren met behulp van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="57f04-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="57f04-114">LCS is een portal voor samenwerking die een omgeving en een reeks regelmatig bijgewerkte services biedt waarmee u de toepassingslevensduur van uw Dynamics 365 Finance and Operations-apps kunt beheren.</span><span class="sxs-lookup"><span data-stu-id="57f04-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="57f04-115">Zie voor meer informatie [Lifecycle Services-resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="57f04-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="57f04-116">Vereisten</span><span class="sxs-lookup"><span data-stu-id="57f04-116">Prerequisites</span></span>

<span data-ttu-id="57f04-117">Voordat u de invoegtoepassing voor voorraadzichtbaarheid kunt installeren, moet u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="57f04-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="57f04-118">Schaf een LCS-implementatieproject aan met minimaal één geïmplementeerde omgeving.</span><span class="sxs-lookup"><span data-stu-id="57f04-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="57f04-119">Genereer de bètasleutels voor uw aanbod in LCS.</span><span class="sxs-lookup"><span data-stu-id="57f04-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="57f04-120">Schakel de bètasleutels in voor uw aanbod voor uw gebruiker in LCS.</span><span class="sxs-lookup"><span data-stu-id="57f04-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="57f04-121">Neem contact op met het Microsoft Voorraadzichtbaarheid-productteam en geef een omgevings-ID op waar u de invoegtoepassing voor voorraadzichtbaarheid wilt implementeren.</span><span class="sxs-lookup"><span data-stu-id="57f04-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="57f04-122">Als u vragen hebt over deze vereisten, neemt u contact op met het productteam voor voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="57f04-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="57f04-123">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="57f04-123">Install the add-in</span></span>

<span data-ttu-id="57f04-124">Om de invoegtoepassing voor voorraadzichtbaarheid te installeren, moet u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="57f04-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="57f04-125">Meld u aan bij de [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portal.</span><span class="sxs-lookup"><span data-stu-id="57f04-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="57f04-126">Selecteer op de startpagina het project waar uw omgeving is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="57f04-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="57f04-127">Selecteer op de projectpagina de omgeving waarin u de invoegtoepassing wilt installeren.</span><span class="sxs-lookup"><span data-stu-id="57f04-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="57f04-128">Schuif op de omgevingspagina naar beneden totdat u de sectie **Invoegtoepassingen voor omgeving** ziet.</span><span class="sxs-lookup"><span data-stu-id="57f04-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="57f04-129">Als de sectie niet zichtbaar is, controleert u of de vereiste bètasleutels volledig zijn verwerkt.</span><span class="sxs-lookup"><span data-stu-id="57f04-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="57f04-130">Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="57f04-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="57f04-131">![De omgevingspagina in LCS](media/inventory-visibility-environment.png "De omgevingspagina in LCS")</span><span class="sxs-lookup"><span data-stu-id="57f04-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="57f04-132">Selecteer de koppeling **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="57f04-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="57f04-133">Er wordt een lijst met beschikbare invoegtoepassingen geopend.</span><span class="sxs-lookup"><span data-stu-id="57f04-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="57f04-134">Selecteer **Voorraadservice** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="57f04-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="57f04-135">(Deze kan nu worden weergegeven als **Invoegtoepassing Voorraadzichtbaarheid voor Dynamics 365 Supply Chain Management** .)</span><span class="sxs-lookup"><span data-stu-id="57f04-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="57f04-136">Voer waarden in voor de volgende velden voor uw omgeving:</span><span class="sxs-lookup"><span data-stu-id="57f04-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="57f04-137">**AAD-toepassings-id**</span><span class="sxs-lookup"><span data-stu-id="57f04-137">**AAD application ID**</span></span>
    - <span data-ttu-id="57f04-138">**AAD-tenant-id**</span><span class="sxs-lookup"><span data-stu-id="57f04-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="57f04-139">![Toevoegen in installatiepagina](media/inventory-visibility-setup.png "Instellingspagina invoegtoepassing")</span><span class="sxs-lookup"><span data-stu-id="57f04-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="57f04-140">Ga akkoord met de voorwaarden door het selectievakje **Voorwaarden** in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="57f04-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="57f04-141">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="57f04-141">Select **Install**.</span></span> <span data-ttu-id="57f04-142">De status van de invoegtoepassing wordt weergegeven als **Wordt geïnstalleerd**.</span><span class="sxs-lookup"><span data-stu-id="57f04-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="57f04-143">Na voltooiing vernieuwt u de pagina zodat de status wordt gewijzigd in **Geïnstalleerd**.</span><span class="sxs-lookup"><span data-stu-id="57f04-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="57f04-144">Een beveiligingsservicetoken ophalen</span><span class="sxs-lookup"><span data-stu-id="57f04-144">Get a security service token</span></span>

<span data-ttu-id="57f04-145">Ga als volgt te werk om een beveiligingsservicetoken te verkrijgen:</span><span class="sxs-lookup"><span data-stu-id="57f04-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="57f04-146">Haal uw `aadToken` op en roep het eindpunt aan: https://securityservice.operations365.dynamics.com/token.</span><span class="sxs-lookup"><span data-stu-id="57f04-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="57f04-147">Vervang de `client_assertion` in de body door uw `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="57f04-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="57f04-148">Vervang de context in de body door de omgeving waarin u de invoegtoepassing wilt implementeren.</span><span class="sxs-lookup"><span data-stu-id="57f04-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="57f04-149">Vervang het bereik in de body door het volgende:</span><span class="sxs-lookup"><span data-stu-id="57f04-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="57f04-150">Bereik voor MCK: "https://inventoryservice.operations365.dynamics.cn/.default"</span><span class="sxs-lookup"><span data-stu-id="57f04-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="57f04-151">(U kunt de Azure Active Directory-toepassings-id en tenant-id voor MCK vinden in `appsettings.mck.json` .)</span><span class="sxs-lookup"><span data-stu-id="57f04-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="57f04-152">Bereik voor PROD: "https://inventoryservice.operations365.dynamics.com/.default"</span><span class="sxs-lookup"><span data-stu-id="57f04-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="57f04-153">(U kunt de Azure Active Directory-toepassings-id en tenant-id voor PROD vinden in `appsettings.prod.json` .)</span><span class="sxs-lookup"><span data-stu-id="57f04-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="57f04-154">Het resultaat moet lijken op het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="57f04-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="57f04-155">U ontvangt als reactie een `access_token`.</span><span class="sxs-lookup"><span data-stu-id="57f04-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="57f04-156">Dit is wat u nodig hebt als Bearer-token voor het aanroepen van de Voorraadzichtbaarheid-API.</span><span class="sxs-lookup"><span data-stu-id="57f04-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="57f04-157">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="57f04-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="57f04-158">De invoegtoepassing verwijderen</span><span class="sxs-lookup"><span data-stu-id="57f04-158">Uninstall the add-in</span></span>

<span data-ttu-id="57f04-159">Selecteer **Verwijderen** als u de invoegtoepassing wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="57f04-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="57f04-160">Vernieuw LCS en de invoegtoepassing Voorraadzichtbaarheid wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="57f04-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="57f04-161">Met het verwijderingsproces wordt de registratie van de invoegtoepassing verwijderd en wordt ook een taak gestart om alle bedrijfsgegevens te verwijderen die in de service zijn opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="57f04-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="57f04-162">Openbare API invoegtoepassing Voorraadzichtbaarheid</span><span class="sxs-lookup"><span data-stu-id="57f04-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="57f04-163">De openbare REST API van de invoegtoepassing Voorraadzichtbaarheid biedt verschillende specifieke integratie-eindpunten.</span><span class="sxs-lookup"><span data-stu-id="57f04-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="57f04-164">Deze ondersteunt drie hoofdinteractietypen:</span><span class="sxs-lookup"><span data-stu-id="57f04-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="57f04-165">Wijzigingen in de voorhanden voorraad van een extern systeem naar de invoegtoepassing boeken.</span><span class="sxs-lookup"><span data-stu-id="57f04-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="57f04-166">Huidige voorhanden hoeveelheden opvragen vanuit een extern systeem.</span><span class="sxs-lookup"><span data-stu-id="57f04-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="57f04-167">Automatische synchronisatie met voorhanden Supply Chain Management-voorraad.</span><span class="sxs-lookup"><span data-stu-id="57f04-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="57f04-168">De automatische synchronisatie maakt geen deel uit van de openbare API, maar wordt in plaats daarvan verwerkt op de achtergrond voor omgevingen die de invoegtoepassing Voorraadzichtbaarheid hebben ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="57f04-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="57f04-169">Authenticatie</span><span class="sxs-lookup"><span data-stu-id="57f04-169">Authentication</span></span>

<span data-ttu-id="57f04-170">Het platformbeveiligingstoken wordt gebruikt om de invoegtoepassing Voorraadzichtbaarheid aan te roepen, dus u moet een Azure Active Directory-token genereren met uw Azure Active Directory-toepassing.</span><span class="sxs-lookup"><span data-stu-id="57f04-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="57f04-171">Zie [De invoegtoepassing Voorraadzichtbaarheid installeren](#install-add-in) voor meer informatie over het verkrijgen van het beveiligingstoken.</span><span class="sxs-lookup"><span data-stu-id="57f04-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="57f04-172">De Voorraadzichtbaarheid-API configureren</span><span class="sxs-lookup"><span data-stu-id="57f04-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="57f04-173">Voordat u de service gaat gebruiken, moet u de configuraties uitvoeren die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="57f04-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="57f04-174">De configuratie kan variëren afhankelijk van de details van uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="57f04-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="57f04-175">Deze bevat hoofdzakelijk vier delen:</span><span class="sxs-lookup"><span data-stu-id="57f04-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="57f04-176">Partitionering</span><span class="sxs-lookup"><span data-stu-id="57f04-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="57f04-177">Dimensieconfiguraties</span><span class="sxs-lookup"><span data-stu-id="57f04-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="57f04-178">Bezig met indexeren</span><span class="sxs-lookup"><span data-stu-id="57f04-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="57f04-179">Aangepaste meting</span><span class="sxs-lookup"><span data-stu-id="57f04-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="57f04-180">Partitionering</span><span class="sxs-lookup"><span data-stu-id="57f04-180">Partitioning</span></span>

<span data-ttu-id="57f04-181">Het partitioneren kan de prestaties van de API voor Voorraadzichtbaarheid aanzienlijk beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="57f04-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="57f04-182">Het is een goed idee om een schema te definiëren waarmee kleine groeperingen van gegevens mogelijk zijn, terwijl er toch betekenisvolle gegevensquery's kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="57f04-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="57f04-183">De `organizationId` (`dataAreaId` in Supply Chain Management) zal altijd deel uitmaken van de partitionering en Voorraadzichtbaarheid is standaard ingesteld op partitioneren op dimensies als *Site + locatie*.</span><span class="sxs-lookup"><span data-stu-id="57f04-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="57f04-184">Dit betekent dat er altijd query's voor de service moeten worden uitgevoerd met deze dimensies gedefinieerd in de filters.</span><span class="sxs-lookup"><span data-stu-id="57f04-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="57f04-185">*Site* en *Locatie* zijn twee algemene standaarddimensies in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="57f04-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="57f04-186">In Supply Chain Management worden deze dimensies *Site* (`InventSiteId`) en *Magazijn* (`InventLocationId`) genoemd.</span><span class="sxs-lookup"><span data-stu-id="57f04-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="57f04-187">Dimensieconfiguraties</span><span class="sxs-lookup"><span data-stu-id="57f04-187">Dimension configurations</span></span>

<span data-ttu-id="57f04-188">In Voorraadzichtbaarheid wordt een lijst met algemene standaarddimensies geboden waarmee de integratie met meerdere bronsystemen wordt mogelijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="57f04-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="57f04-189">In de volgende tabel worden de voorraaddimensies weergegeven die de standaarddimensienamen zijn in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="57f04-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="57f04-190">Dimensietype</span><span class="sxs-lookup"><span data-stu-id="57f04-190">Dimension type</span></span> | <span data-ttu-id="57f04-191">Dimensienaam</span><span class="sxs-lookup"><span data-stu-id="57f04-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="57f04-192">Artikel</span><span class="sxs-lookup"><span data-stu-id="57f04-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="57f04-193">Artikel</span><span class="sxs-lookup"><span data-stu-id="57f04-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="57f04-194">Artikel</span><span class="sxs-lookup"><span data-stu-id="57f04-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="57f04-195">Artikel</span><span class="sxs-lookup"><span data-stu-id="57f04-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="57f04-196">Tracering</span><span class="sxs-lookup"><span data-stu-id="57f04-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="57f04-197">Tracering</span><span class="sxs-lookup"><span data-stu-id="57f04-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="57f04-198">Locatie</span><span class="sxs-lookup"><span data-stu-id="57f04-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="57f04-199">Locatie</span><span class="sxs-lookup"><span data-stu-id="57f04-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="57f04-200">Voorraadstatus</span><span class="sxs-lookup"><span data-stu-id="57f04-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="57f04-201">Magazijnspecifiek</span><span class="sxs-lookup"><span data-stu-id="57f04-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="57f04-202">Magazijnspecifiek</span><span class="sxs-lookup"><span data-stu-id="57f04-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="57f04-203">Magazijnspecifiek</span><span class="sxs-lookup"><span data-stu-id="57f04-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="57f04-204">Het dimensietype vermeld in de vorige tabel is alleen ter referentie.</span><span class="sxs-lookup"><span data-stu-id="57f04-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="57f04-205">U hoeft het dimensietype niet te definiëren in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="57f04-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="57f04-206">Als er een aangepaste dimensie bestaat en naar een standaardwaarde moet stromen bij verbruik door Voorraadzichtbaarheid, kunt u de naam **Aangepaste dimensie** in Voorraadzichtbaarheid configureren.</span><span class="sxs-lookup"><span data-stu-id="57f04-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="57f04-207">Externe systemen hebben toegang tot Voorraadzichtbaarheid via RESTful API's waarmee gegevens van voorhanden voorraad over bepaalde sets met dimensies kunnen worden opgevraagd.</span><span class="sxs-lookup"><span data-stu-id="57f04-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="57f04-208">Voor de integratie kunt u met Voorraadzichtbaarheid de *gegevensbron van het externe kanaal* en de brondimensie naar de *doeldimensies* configureren in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="57f04-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="57f04-209">De doeldimensies moeten een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="57f04-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="57f04-210">Standaarddimensies in Voorraadzichtbaarheid</span><span class="sxs-lookup"><span data-stu-id="57f04-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="57f04-211">Aangepaste dimensies</span><span class="sxs-lookup"><span data-stu-id="57f04-211">Custom dimensions</span></span>

<span data-ttu-id="57f04-212">Het doel van dimensieconfiguratie is het standaardiseren van de integratie met meerdere systemen voor de query voor dimensies en de boekingsgebeurtenis met dimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="57f04-213">Bezig met indexeren</span><span class="sxs-lookup"><span data-stu-id="57f04-213">Indexing</span></span>

<span data-ttu-id="57f04-214">Meestal is de query voor de voorhanden voorraad niet alleen op het hoogste niveau 'totaal', maar wilt u mogelijk de resultaten bekijken die zijn samengevoegd op basis van de voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="57f04-215">Voorraadzichtbaarheid is flexibel omdat u de indexen kunt instellen die zijn gebaseerd op de dimensie of de combinatie van de dimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="57f04-216">Op dit moment kunt u maximaal vijf indexen configureren.</span><span class="sxs-lookup"><span data-stu-id="57f04-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="57f04-217">U moet voorafgaand aan de implementatie zorgvuldig overwegen welke dimensie of dimensiecombinatie u gaat gebruiken om er zeker van te zijn dat deze aan uw bedrijfsbehoeften voldoet.</span><span class="sxs-lookup"><span data-stu-id="57f04-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="57f04-218">Als u bijvoorbeeld als volgt producten wilt opvragen:</span><span class="sxs-lookup"><span data-stu-id="57f04-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="57f04-219">Vraag de geaggregeerde voorhanden producten op basis van de dimensies *Kleur* en *Grootte* op.</span><span class="sxs-lookup"><span data-stu-id="57f04-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="57f04-220">In sommige gevallen wilt u alleen in totaal een query voor het product uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="57f04-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="57f04-221">U zou twee indexen hebben die als volgt zijn gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="57f04-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="57f04-222">Het lege haakje aggregeert op basis van de product-ID binnen de partitie.</span><span class="sxs-lookup"><span data-stu-id="57f04-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="57f04-223">De indexering bepaalt hoe u de resultaten kunt groeperen op basis van de `groupBy`-queryinstelling.</span><span class="sxs-lookup"><span data-stu-id="57f04-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="57f04-224">Als u in dit geval geen `groupBy`-waarden definieert, krijgt u totalen op `productid`.</span><span class="sxs-lookup"><span data-stu-id="57f04-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="57f04-225">Als u `groupBy` als `groupBy=ColorId&groupBy=SizeId` definieert, worden meerdere regels als resultaat gegeven, op basis van de verschillende combinaties van kleur en grootte in het systeem.</span><span class="sxs-lookup"><span data-stu-id="57f04-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="57f04-226">U kunt uw querycriteria in de aanvraagbody plaatsen.</span><span class="sxs-lookup"><span data-stu-id="57f04-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="57f04-227">Hier volgt een voorbeeldquery voor het product met de combinatie kleur en grootte.</span><span class="sxs-lookup"><span data-stu-id="57f04-227">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="57f04-228">Aangepaste meting</span><span class="sxs-lookup"><span data-stu-id="57f04-228">Custom measurement</span></span>

<span data-ttu-id="57f04-229">De standaardmetingshoeveelheden worden gekoppeld aan Supply Chain Management, maar mogelijk wilt u een hoeveelheid hebben die bestaat uit een combinatie van de standaardmetingen.</span><span class="sxs-lookup"><span data-stu-id="57f04-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="57f04-230">Hiervoor kunt u een configuratie van aangepaste hoeveelheden hebben, die worden toegevoegd aan de uitvoer van de query's voor voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="57f04-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="57f04-231">Met deze functie kunt u een set maateenheden definiëren die wordt toegevoegd, en/of een set maateenheden die wordt afgetrokken, zodat de aangepaste meting wordt gevormd.</span><span class="sxs-lookup"><span data-stu-id="57f04-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="57f04-232">Met de volgende queryvoorwaarde bijvoorbeeld configureert u de aangepaste metingshoeveelheid als `MyCustomAvailableforReservation` om te worden verbruikt door het verbruikssysteem.</span><span class="sxs-lookup"><span data-stu-id="57f04-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="57f04-233">Verbruikssysteem</span><span class="sxs-lookup"><span data-stu-id="57f04-233">Consumption system</span></span> | <span data-ttu-id="57f04-234">Berekende meters</span><span class="sxs-lookup"><span data-stu-id="57f04-234">Calculated measurers</span></span> | <span data-ttu-id="57f04-235">Gegevensbron</span><span class="sxs-lookup"><span data-stu-id="57f04-235">Data source</span></span> | <span data-ttu-id="57f04-236">Modificator</span><span class="sxs-lookup"><span data-stu-id="57f04-236">Modifier</span></span> | <span data-ttu-id="57f04-237">Berekeningstype modificator</span><span class="sxs-lookup"><span data-stu-id="57f04-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="57f04-238">Optelling</span><span class="sxs-lookup"><span data-stu-id="57f04-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="57f04-239">Optelling</span><span class="sxs-lookup"><span data-stu-id="57f04-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="57f04-240">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="57f04-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="57f04-241">Optelling</span><span class="sxs-lookup"><span data-stu-id="57f04-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="57f04-242">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="57f04-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="57f04-243">Optelling</span><span class="sxs-lookup"><span data-stu-id="57f04-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="57f04-244">Optelling</span><span class="sxs-lookup"><span data-stu-id="57f04-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="57f04-245">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="57f04-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="57f04-246">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="57f04-246">Subtraction</span></span> |

<span data-ttu-id="57f04-247">Hiermee retourneert de query voor de aangepaste metingshoeveelheid de volgende uitvoer.</span><span class="sxs-lookup"><span data-stu-id="57f04-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="57f04-248">De `MyCustomAvailableforReservation`-uitvoer is gebaseerd op de berekeningsinstelling in de aangepaste metingen als:</span><span class="sxs-lookup"><span data-stu-id="57f04-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="57f04-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="57f04-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="57f04-250">Wijzigingen voorhanden voorraad boeken</span><span class="sxs-lookup"><span data-stu-id="57f04-250">Posting on-hand changes</span></span>

<span data-ttu-id="57f04-251">De exacte URL waarnaar de gebeurtenis wordt geboekt, is afhankelijk van uw geografische regio.</span><span class="sxs-lookup"><span data-stu-id="57f04-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="57f04-252">Deze heeft de volgende vorm:</span><span class="sxs-lookup"><span data-stu-id="57f04-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="57f04-253">Na verificatie kan deze URL worden gebruikt in combinatie met de HTTP `POST`-methode voor het verzenden van gebeurtenissen voor wijzigingen van de voorhanden voorraad naar de service.</span><span class="sxs-lookup"><span data-stu-id="57f04-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="57f04-254">Een speciale koptekst wordt gebruikt voor de communicatie met Dynamics 365-services via HTTP-aanvragen, waarbij de omgevings-ID van het Supply Chain Management-exemplaar wordt aangegeven waaraan de gegevens zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="57f04-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="57f04-255">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="57f04-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="57f04-256">Queryvoorbeeld 1 voor boeken van wijzigingen voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="57f04-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="57f04-257">In dit voorbeeld ziet u een scenario waarin u de dimensieconfiguratie in Power Apps kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="57f04-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="57f04-258">Met de volgende query configureert u de dimensietoewijzing in Power Apps:</span><span class="sxs-lookup"><span data-stu-id="57f04-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="57f04-259">U kunt nu de `dimensionDataSource` opgeven en aangepaste dimensies gebruiken in uw query's.</span><span class="sxs-lookup"><span data-stu-id="57f04-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="57f04-260">Aangepaste dimensies worden automatisch omgezet in basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="57f04-261">Queryvoorbeeld 2 voor boeken van wijzigingen voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="57f04-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="57f04-262">In dit voorbeeld ziet u een scenario waarin er geen toewijzingen zijn ingesteld voor de dimensieconfiguratie in Power Apps. Daarom moet de boeking ook gebruikmaken van de basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="57f04-263">Alle dimensies moeten basisdimensies zijn als het veld `dimensionDataSource` null, leeg of een spatie is.</span><span class="sxs-lookup"><span data-stu-id="57f04-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="57f04-264">JSON-documentveldeigenschappen</span><span class="sxs-lookup"><span data-stu-id="57f04-264">JSON document field properties</span></span>

<span data-ttu-id="57f04-265">De velden uit de eerdere JSON-queryvoorbeelden hebben de eigenschappen die in de volgende tabel worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="57f04-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="57f04-266">Veld-ID</span><span class="sxs-lookup"><span data-stu-id="57f04-266">Field ID</span></span> | <span data-ttu-id="57f04-267">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="57f04-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="57f04-268">Een unieke ID voor de specifieke wijzigingsgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="57f04-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="57f04-269">Deze ID wordt gebruikt om ervoor te zorgen dat als bij het boeken de communicatie met de service mislukt, het opnieuw indienen van de gebeurtenis niet ertoe leidt dat dezelfde gebeurtenis tweemaal in het systeem wordt geteld.</span><span class="sxs-lookup"><span data-stu-id="57f04-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="57f04-270">De id van de organisatie die aan de gebeurtenis is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="57f04-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="57f04-271">Deze is toegewezen aan Supply Chain Management-organisaties of -gegevensgebied-id's.</span><span class="sxs-lookup"><span data-stu-id="57f04-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="57f04-272">De id van het betreffende product.</span><span class="sxs-lookup"><span data-stu-id="57f04-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="57f04-273">De hoeveelheid waarmee de voorhanden voorraad moet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="57f04-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="57f04-274">Als er bijvoorbeeld 10 nieuwe bagels aan een plank zijn toegevoegd, is deze waarde 10.</span><span class="sxs-lookup"><span data-stu-id="57f04-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="57f04-275">Als 3 bagels van de plank worden verwijderd of verkocht, zou deze waarde -3 zijn.</span><span class="sxs-lookup"><span data-stu-id="57f04-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="57f04-276">De gegevensbron van de dimensies gebruikt bij het boeken van de wijzigingsgebeurtenis en query.</span><span class="sxs-lookup"><span data-stu-id="57f04-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="57f04-277">Als u de gegevensbron opgeeft, kunt u de aangepaste dimensies gebruiken van de opgegeven gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="57f04-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="57f04-278">Met de dimensieconfiguratie kan Voorraadzichtbaarheid de aangepaste dimensies toewijzen aan de algemene standaarddimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="57f04-279">Als de `dimensionDataSource` niet is opgegeven, kunt u alleen de algemene standaarddimensies in uw query's gebruiken.</span><span class="sxs-lookup"><span data-stu-id="57f04-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="57f04-280">Een dynamische verzameling sleutel-waardeparen.</span><span class="sxs-lookup"><span data-stu-id="57f04-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="57f04-281">Deze worden toegewezen aan enkele dimensies in Supply Chain Management, maar u kunt ook aangepaste dimensies (zoals *Bron*) toevoegen die aangeven of de gebeurtenis afkomstig is van Supply Chain Management of een extern systeem.</span><span class="sxs-lookup"><span data-stu-id="57f04-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="57f04-282">Query uitvoeren voor huidige voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="57f04-282">Querying current on-hand</span></span>

<span data-ttu-id="57f04-283">Het eindpunt voor het uitvoeren van query's voor de huidige voorhanden voorraad heeft een vergelijkbare URL:</span><span class="sxs-lookup"><span data-stu-id="57f04-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="57f04-284">Hiervoor worden query's uitgevoerd met de HTTP `POST`-methode.</span><span class="sxs-lookup"><span data-stu-id="57f04-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="57f04-285">Queryvoorbeeld 1 huidige voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="57f04-285">Current on-hand query example 1</span></span>

<span data-ttu-id="57f04-286">In dit voorbeeld ziet u een scenario waarin u de dimensieconfiguratie al hebt voltooid in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="57f04-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="57f04-287">Met de volgende query configureert u de dimensietoewijzing in Power Apps:</span><span class="sxs-lookup"><span data-stu-id="57f04-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="57f04-288">U kunt nu de `dimensionDataSource` opgeven en aangepaste dimensies gebruiken in uw query's.</span><span class="sxs-lookup"><span data-stu-id="57f04-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="57f04-289">Aangepaste dimensies worden automatisch omgezet in basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="57f04-290">U kunt de `DimensionDataSource` opgeven in `filters` en aangepaste dimensies opgeven in `filters` en `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="57f04-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="57f04-291">Aangepaste dimensies worden automatisch omgezet in basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="57f04-292">Queryvoorbeeld 2 huidige voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="57f04-292">Current on-hand query example 2</span></span>

<span data-ttu-id="57f04-293">In dit voorbeeld ziet u een scenario waarin er geen toewijzingen zijn ingesteld voor de dimensieconfiguratie in Power Apps. Daarom moet de boeking ook gebruikmaken van de basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="57f04-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="57f04-294">Alle dimensies moeten basisdimensies zijn als het veld `dimensionDataSource` onder `filters` null, leeg of een spatie is.</span><span class="sxs-lookup"><span data-stu-id="57f04-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="57f04-295">Voorbeeldretourresultaat</span><span class="sxs-lookup"><span data-stu-id="57f04-295">Example return result</span></span>

<span data-ttu-id="57f04-296">De query's die in de vorige voorbeelden worden weergegeven, kunnen een resultaat als dit retourneren.</span><span class="sxs-lookup"><span data-stu-id="57f04-296">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="57f04-297">De velden met hoeveelheden zijn gestructureerd als een woordenboek met metingen en de bijbehorende waarden.</span><span class="sxs-lookup"><span data-stu-id="57f04-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
