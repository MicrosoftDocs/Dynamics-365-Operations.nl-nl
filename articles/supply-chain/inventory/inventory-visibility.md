---
title: Invoegtoepassing Voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor de zichtbaarheid van de voorraad installeert en configureert voor Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910420"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="567bb-103">Invoegtoepassing Voorraadzichtbaarheid</span><span class="sxs-lookup"><span data-stu-id="567bb-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="567bb-104">De invoegtoepassing voor de zichtbaarheid van de voorraad is een onafhankelijke en zeer schaalbare microservice waarmee real-time tracking van voorhanden voorraad wordt ingeschakeld om een globale weergave van de voorraadzichtbaarheid te genereren.</span><span class="sxs-lookup"><span data-stu-id="567bb-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="567bb-105">Alle informatie die betrekking heeft op de voorhanden voorraad, wordt in bijna real-time met behulp van SQL-integratie op laag niveau geëxporteerd naar de service.</span><span class="sxs-lookup"><span data-stu-id="567bb-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="567bb-106">Externe systemen openen de service via RESTful API's om informatie over voorhanden voorraad voor bepaalde sets dimensies op te vragen, waardoor een lijst met beschikbare voorhanden posities wordt opgehaald.</span><span class="sxs-lookup"><span data-stu-id="567bb-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="567bb-107">Voorraadzichtbaarheid is een microservice die is gebouwd op Microsoft Dataverse, wat betekent dat u deze kunt uitbreiden door Power Apps te bouwen en Power BI toe te passen voor aangepaste functionaliteit om aan uw zakelijke vereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="567bb-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="567bb-108">Het is ook mogelijk om de index te upgraden om voorraadquery's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="567bb-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="567bb-109">Voorraadzichtbaarheid bevat configuratieopties waarmee de service kan worden geïntegreerd met systemen van derden.</span><span class="sxs-lookup"><span data-stu-id="567bb-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="567bb-110">De service ondersteunt de gestandaardiseerde voorraaddimensie, aangepaste uitbreidbaarheid en gestandaardiseerde, configureerbare berekende hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="567bb-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="567bb-111">In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor voorraadzichtbaarheid installeert en configureert voor Dynamics 365 Supply Chain Management en hoe u de API (Application Programming Interface) ervan gebruikt.</span><span class="sxs-lookup"><span data-stu-id="567bb-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="567bb-112">Invoegtoepassing Voorraadzichtbaarheid installeren</span><span class="sxs-lookup"><span data-stu-id="567bb-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="567bb-113">U moet de invoegtoepassing voor voorraadzichtbaarheid installeren met behulp van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="567bb-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="567bb-114">LCS is een portal voor samenwerking die een omgeving en een reeks regelmatig bijgewerkte services biedt waarmee u de toepassingslevensduur van uw Dynamics 365 Finance and Operations-apps kunt beheren.</span><span class="sxs-lookup"><span data-stu-id="567bb-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="567bb-115">Zie voor meer informatie [Lifecycle Services-resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="567bb-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="567bb-116">Vereisten</span><span class="sxs-lookup"><span data-stu-id="567bb-116">Prerequisites</span></span>

<span data-ttu-id="567bb-117">Voordat u de invoegtoepassing voor voorraadzichtbaarheid kunt installeren, moet u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="567bb-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="567bb-118">Schaf een LCS-implementatieproject aan met minimaal één geïmplementeerde omgeving.</span><span class="sxs-lookup"><span data-stu-id="567bb-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="567bb-119">Zorg ervoor dat aan de vereisten voor het instellen van invoegvoegingen die beschikbaar zijn in het [Overzicht van invoegvoegingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) is voldaan.</span><span class="sxs-lookup"><span data-stu-id="567bb-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="567bb-120">Voor Voorraadzichtbaarheid is geen koppeling voor twee keer wegschrijven vereist.</span><span class="sxs-lookup"><span data-stu-id="567bb-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="567bb-121">Neem contact op met het team op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) om de volgende drie vereiste bestanden op te halen:</span><span class="sxs-lookup"><span data-stu-id="567bb-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="567bb-122">`Inventory Visibility Integration.zip` (als u een eerdere versie van Supply Chain Management uitvoert dan versie 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="567bb-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="567bb-123">Volg de instructies in [Quickstart: registreer een toepassing bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app) om een toepassing te registreren en een clientgeheim aan AAD toe te voegen in uw Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="567bb-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="567bb-124">Een toepassing registreren</span><span class="sxs-lookup"><span data-stu-id="567bb-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="567bb-125">Een clientgeheim toevoegen</span><span class="sxs-lookup"><span data-stu-id="567bb-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="567bb-126">De **Toepassings-id (client)**, **Clientgeheim** en **Tenant-id** worden in de volgende stappen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="567bb-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="567bb-127">De landen en regio's die momenteel worden ondersteund, zijn Canada, de Verenigde Staten en de Europese Unie (EU).</span><span class="sxs-lookup"><span data-stu-id="567bb-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="567bb-128">Als u vragen hebt over deze vereisten, neemt u contact op met het productteam voor voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="567bb-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="567bb-129">Dataverse instellen</span><span class="sxs-lookup"><span data-stu-id="567bb-129">Set up Dataverse</span></span>

<span data-ttu-id="567bb-130">Volg deze stappen om Dataverse in te stellen.</span><span class="sxs-lookup"><span data-stu-id="567bb-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="567bb-131">Een serviceprincipe aan uw tenant toevoegen:</span><span class="sxs-lookup"><span data-stu-id="567bb-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="567bb-132">Installeer Azure AD PowerShell Module v2, zoals beschreven in [Azure Active Directory PowerShell for Graph installeren](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="567bb-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="567bb-133">Voer de volgende PowerShell-opdracht uit.</span><span class="sxs-lookup"><span data-stu-id="567bb-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="567bb-134">Een toepassingsgebruiker voor Voorraadzichtbaarheid maken in Dataverse:</span><span class="sxs-lookup"><span data-stu-id="567bb-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="567bb-135">Open de URL van uw Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="567bb-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="567bb-136">Ga naar **Geavanceerde instellingen \> Systeem \> \> Gebruikers** en maak een toepassingsgebruiker.</span><span class="sxs-lookup"><span data-stu-id="567bb-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="567bb-137">Gebruik het weergavemenu om de paginaweergave te wijzigen in **Toepassingsgebruikers**.</span><span class="sxs-lookup"><span data-stu-id="567bb-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="567bb-138">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="567bb-138">Select **New**.</span></span> <span data-ttu-id="567bb-139">Stel de toepassings-id in op *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="567bb-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="567bb-140">(De object-id wordt automatisch geladen wanneer u de wijzigingen opslaat.) U kunt de naam aanpassen.</span><span class="sxs-lookup"><span data-stu-id="567bb-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="567bb-141">U kunt de naam bijvoorbeeld wijzigen in *Voorraadzichtbaarheid*.</span><span class="sxs-lookup"><span data-stu-id="567bb-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="567bb-142">Wanneer u klaar bent, selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="567bb-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="567bb-143">Selecteer **Rol toewijzen** en selecteer vervolgens **Systeembeheerder**.</span><span class="sxs-lookup"><span data-stu-id="567bb-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="567bb-144">Als er een rol is met de naam **Common Data Service-gebruiker**, selecteert u ook deze rol.</span><span class="sxs-lookup"><span data-stu-id="567bb-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="567bb-145">Zie [Een toepassingsgebruiker maken](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="567bb-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="567bb-146">Als de standaardtaal van Dataverse niet **Engels** is:</span><span class="sxs-lookup"><span data-stu-id="567bb-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="567bb-147">Ga naar **Geavanceerde instelling \> Beheer \> Talen**.</span><span class="sxs-lookup"><span data-stu-id="567bb-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="567bb-148">Selecteer **Engels (LanguageCode=1033)** en selecteer **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="567bb-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="567bb-149">Het bestand `Inventory Visibility Dataverse Solution.zip` met de gerelateerde entiteiten van de Dataverse-configuratie en Power Apps importeren:</span><span class="sxs-lookup"><span data-stu-id="567bb-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="567bb-150">Ga naar de pagina **Oplossingen**.</span><span class="sxs-lookup"><span data-stu-id="567bb-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="567bb-151">Selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="567bb-151">Select **Import**.</span></span>

1. <span data-ttu-id="567bb-152">De triggerstroom voor de configuratie-upgrade importeren:</span><span class="sxs-lookup"><span data-stu-id="567bb-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="567bb-153">Ga naar de pagina Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="567bb-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="567bb-154">Zorg ervoor dat de verbinding met de naam *Dataverse (verouderd)* bestaat.</span><span class="sxs-lookup"><span data-stu-id="567bb-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="567bb-155">(Als deze verbinding niet bestaat, maakt u deze.)</span><span class="sxs-lookup"><span data-stu-id="567bb-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="567bb-156">Importeer het bestand `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="567bb-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="567bb-157">Nadat dit bestand is geïmporteerd, wordt de trigger weergegeven onder **Mijn stromen**.</span><span class="sxs-lookup"><span data-stu-id="567bb-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="567bb-158">Initialiseer de volgende vier variabelen op basis van de omgevingsgegevens:</span><span class="sxs-lookup"><span data-stu-id="567bb-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="567bb-159">Tenant-id van Azure</span><span class="sxs-lookup"><span data-stu-id="567bb-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="567bb-160">Client-id van de Azure-toepassing</span><span class="sxs-lookup"><span data-stu-id="567bb-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="567bb-161">Client-geheim van de Azure-toepassing</span><span class="sxs-lookup"><span data-stu-id="567bb-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="567bb-162">Eindpunt van voorraadzichtbaarheid</span><span class="sxs-lookup"><span data-stu-id="567bb-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="567bb-163">Zie de sectie [Integratie van voorraadzichtbaarheid instellen](#setup-inventory-visibility-integration) verder op in dit onderwerp voor meer informatie over deze variabele.</span><span class="sxs-lookup"><span data-stu-id="567bb-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="567bb-164">![Configuratietrigger](media/configuration-trigger.png "Configuratietrigger")</span><span class="sxs-lookup"><span data-stu-id="567bb-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="567bb-165">Selecteer **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="567bb-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="567bb-166">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="567bb-166">Install the add-in</span></span>

<span data-ttu-id="567bb-167">Om de invoegtoepassing voor voorraadzichtbaarheid te installeren, moet u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="567bb-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="567bb-168">Meld u aan bij de [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portal.</span><span class="sxs-lookup"><span data-stu-id="567bb-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="567bb-169">Selecteer op de startpagina het project waar uw omgeving is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="567bb-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="567bb-170">Selecteer op de projectpagina de omgeving waarin u de invoegtoepassing wilt installeren.</span><span class="sxs-lookup"><span data-stu-id="567bb-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="567bb-171">Schuif op de omgevingspagina naar beneden tot u de sectie **Invoegvoegingen voor omgeving** ziet in de sectie **Power Platform-Integratie**, waar u de naam van de Dataverse-omgeving kunt vinden.</span><span class="sxs-lookup"><span data-stu-id="567bb-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="567bb-172">Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="567bb-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="567bb-173">![De omgevingspagina in LCS](media/inventory-visibility-environment.png "De omgevingspagina in LCS")</span><span class="sxs-lookup"><span data-stu-id="567bb-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="567bb-174">Selecteer de koppeling **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="567bb-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="567bb-175">Er wordt een lijst met beschikbare invoegtoepassingen geopend.</span><span class="sxs-lookup"><span data-stu-id="567bb-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="567bb-176">Selecteer **Voorraadzichtbaarheid** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="567bb-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="567bb-177">Voer waarden in voor de volgende velden voor uw omgeving:</span><span class="sxs-lookup"><span data-stu-id="567bb-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="567bb-178">**Id AAD-toepassing (client)**</span><span class="sxs-lookup"><span data-stu-id="567bb-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="567bb-179">**AAD-tenant-id**</span><span class="sxs-lookup"><span data-stu-id="567bb-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="567bb-180">![Toevoegen in installatiepagina](media/inventory-visibility-setup.png "Instellingspagina invoegtoepassing")</span><span class="sxs-lookup"><span data-stu-id="567bb-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="567bb-181">Ga akkoord met de voorwaarden door het selectievakje **Voorwaarden** in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="567bb-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="567bb-182">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="567bb-182">Select **Install**.</span></span> <span data-ttu-id="567bb-183">De status van de invoegtoepassing wordt weergegeven als **Wordt geïnstalleerd**.</span><span class="sxs-lookup"><span data-stu-id="567bb-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="567bb-184">Na voltooiing vernieuwt u de pagina zodat de status wordt gewijzigd in **Geïnstalleerd**.</span><span class="sxs-lookup"><span data-stu-id="567bb-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="567bb-185">De invoegtoepassing verwijderen</span><span class="sxs-lookup"><span data-stu-id="567bb-185">Uninstall the add-in</span></span>

<span data-ttu-id="567bb-186">Selecteer **Verwijderen** als u de invoegtoepassing wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="567bb-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="567bb-187">Wanneer u LCS vernieuwt, wordt de invoegtoepassing Voorraadzichtbaarheid verwijderd.</span><span class="sxs-lookup"><span data-stu-id="567bb-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="567bb-188">Met het verwijderingsproces wordt de registratie van de invoegtoepassing verwijderd en wordt ook een taak gestart om alle bedrijfsgegevens te verwijderen die in de service zijn opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="567bb-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="567bb-189">Gegevens van voorhanden voorraad verbruiken vanuit Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="567bb-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="567bb-190">Het integratiepakket voor voorraadzichtbaarheid implementeren</span><span class="sxs-lookup"><span data-stu-id="567bb-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="567bb-191">Als u Supply Chain Management versie 10.0.17 of eerder uitvoert, neemt u contact op met het ondersteuningsteam voor voorraadzichtbaarheid op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) om het pakketbestand op te halen.</span><span class="sxs-lookup"><span data-stu-id="567bb-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="567bb-192">Implementeer het pakket vervolgens in LCS.</span><span class="sxs-lookup"><span data-stu-id="567bb-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="567bb-193">Als er tijdens de implementatie een fout optreedt omdat de versies niet overeenkomen, moet u het X++-project handmatig in uw ontwikkelomgeving importeren.</span><span class="sxs-lookup"><span data-stu-id="567bb-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="567bb-194">Maak vervolgens het implementeerbare pakket in uw ontwikkelomgeving en implementeer dit in uw productieomgeving.</span><span class="sxs-lookup"><span data-stu-id="567bb-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="567bb-195">De code is opgenomen in Supply Chain Management versie 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="567bb-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="567bb-196">Als u die versie of een latere versie uitvoert, is implementatie niet vereist.</span><span class="sxs-lookup"><span data-stu-id="567bb-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="567bb-197">Zorg ervoor dat de volgende functies zijn ingeschakeld in uw Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="567bb-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="567bb-198">(Standaard zijn deze ingeschakeld.)</span><span class="sxs-lookup"><span data-stu-id="567bb-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="567bb-199">Beschrijving van functie</span><span class="sxs-lookup"><span data-stu-id="567bb-199">Feature description</span></span> | <span data-ttu-id="567bb-200">Codeversie</span><span class="sxs-lookup"><span data-stu-id="567bb-200">Code version</span></span> | <span data-ttu-id="567bb-201">Klasse in-/uitschakelen</span><span class="sxs-lookup"><span data-stu-id="567bb-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="567bb-202">Het gebruik van voorraaddimensies in de tabel InventSum in- of uitschakelen</span><span class="sxs-lookup"><span data-stu-id="567bb-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="567bb-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="567bb-203">10.0.11</span></span> | <span data-ttu-id="567bb-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="567bb-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="567bb-205">Het gebruik van voorraaddimensies in de tabel InventSumDelta in- of uitschakelen</span><span class="sxs-lookup"><span data-stu-id="567bb-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="567bb-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="567bb-206">10.0.12</span></span> | <span data-ttu-id="567bb-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="567bb-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="567bb-208">Integratie van voorraadzichtbaarheid instellen</span><span class="sxs-lookup"><span data-stu-id="567bb-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="567bb-209">Open in Supply Chain Management de werkruimte **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** en schakel de functie **Integratie van voorraadzichtbaarheid** in.</span><span class="sxs-lookup"><span data-stu-id="567bb-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="567bb-210">Ga naar **Voorraadbeheer \> Instellen \> Parameters voor integratie van voorraadzichtbaarheid** en voer de URL in van de omgeving in waarin u Voorraadzichtbaarheid uitvoert.</span><span class="sxs-lookup"><span data-stu-id="567bb-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="567bb-211">Zoek de Azure-regio van uw LCS-omgeving op en voer vervolgens de URL in.</span><span class="sxs-lookup"><span data-stu-id="567bb-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="567bb-212">De URL heeft de volgende notatie:</span><span class="sxs-lookup"><span data-stu-id="567bb-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="567bb-213">Als u bijvoorbeeld in Europa bent, heeft uw omgeving een van de volgende URL's:</span><span class="sxs-lookup"><span data-stu-id="567bb-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="567bb-214">De volgende regio's zijn momenteel niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="567bb-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="567bb-215">Azure-regio</span><span class="sxs-lookup"><span data-stu-id="567bb-215">Azure region</span></span> | <span data-ttu-id="567bb-216">Korte naam regio</span><span class="sxs-lookup"><span data-stu-id="567bb-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="567bb-217">Australië - oost</span><span class="sxs-lookup"><span data-stu-id="567bb-217">Australia east</span></span> | <span data-ttu-id="567bb-218">eau</span><span class="sxs-lookup"><span data-stu-id="567bb-218">eau</span></span> |
    | <span data-ttu-id="567bb-219">Australië - zuidoost</span><span class="sxs-lookup"><span data-stu-id="567bb-219">Australia southeast</span></span> | <span data-ttu-id="567bb-220">seau</span><span class="sxs-lookup"><span data-stu-id="567bb-220">seau</span></span> |
    | <span data-ttu-id="567bb-221">Canada - centraal</span><span class="sxs-lookup"><span data-stu-id="567bb-221">Canada central</span></span> | <span data-ttu-id="567bb-222">cca</span><span class="sxs-lookup"><span data-stu-id="567bb-222">cca</span></span> |
    | <span data-ttu-id="567bb-223">Canada - oost</span><span class="sxs-lookup"><span data-stu-id="567bb-223">Canada east</span></span> | <span data-ttu-id="567bb-224">eca</span><span class="sxs-lookup"><span data-stu-id="567bb-224">eca</span></span> |
    | <span data-ttu-id="567bb-225">Noord-Europa</span><span class="sxs-lookup"><span data-stu-id="567bb-225">North Europe</span></span> | <span data-ttu-id="567bb-226">neu</span><span class="sxs-lookup"><span data-stu-id="567bb-226">neu</span></span> |
    | <span data-ttu-id="567bb-227">West-Europa</span><span class="sxs-lookup"><span data-stu-id="567bb-227">West Europe</span></span> | <span data-ttu-id="567bb-228">weu</span><span class="sxs-lookup"><span data-stu-id="567bb-228">weu</span></span> |
    | <span data-ttu-id="567bb-229">VS - oost</span><span class="sxs-lookup"><span data-stu-id="567bb-229">East US</span></span> | <span data-ttu-id="567bb-230">eus</span><span class="sxs-lookup"><span data-stu-id="567bb-230">eus</span></span> |
    | <span data-ttu-id="567bb-231">VS - west</span><span class="sxs-lookup"><span data-stu-id="567bb-231">West US</span></span> | <span data-ttu-id="567bb-232">wus</span><span class="sxs-lookup"><span data-stu-id="567bb-232">wus</span></span> |

1. <span data-ttu-id="567bb-233">Ga naar **Voorraadbeheer \> Periodiek \> Integratie van voorraadzichtbaarheid** en schakel de taak in.</span><span class="sxs-lookup"><span data-stu-id="567bb-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="567bb-234">Alle gebeurtenissen voor voorraadwijziging van Supply Chain Management worden nu geboekt naar Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="567bb-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="567bb-235">De openbare API-invoegtoepassing Voorraadzichtbaarheid</span><span class="sxs-lookup"><span data-stu-id="567bb-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="567bb-236">De openbare REST API van de invoegtoepassing Voorraadzichtbaarheid biedt verschillende specifieke eindpunten voor integratie.</span><span class="sxs-lookup"><span data-stu-id="567bb-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="567bb-237">Deze ondersteunt drie hoofdinteractietypen:</span><span class="sxs-lookup"><span data-stu-id="567bb-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="567bb-238">Wijzigingen in de voorhanden voorraad naar de invoegtoepassing boeken vanuit een extern systeem</span><span class="sxs-lookup"><span data-stu-id="567bb-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="567bb-239">Huidige voorhanden hoeveelheden opvragen vanuit een extern systeem</span><span class="sxs-lookup"><span data-stu-id="567bb-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="567bb-240">Automatische synchronisatie met voorhanden Supply Chain Management-voorraad</span><span class="sxs-lookup"><span data-stu-id="567bb-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="567bb-241">Automatische synchronisatie maakt geen deel uit van de openbare API.</span><span class="sxs-lookup"><span data-stu-id="567bb-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="567bb-242">In plaats daarvan wordt de automatisch synchronisatie op de achtergrond verwerkt voor omgevingen waarin de Invoegvoeging Voorraadzichtbaarheid is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="567bb-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="567bb-243">Authenticatie</span><span class="sxs-lookup"><span data-stu-id="567bb-243">Authentication</span></span>

<span data-ttu-id="567bb-244">Het platformbeveiligingstoken wordt gebruikt om de invoegvoeging Voorraadzichtbaarheid aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="567bb-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="567bb-245">U moet daarom een *Azure Active Directory (Azure AD)-token* genereren met de Azure AD-toepassing.</span><span class="sxs-lookup"><span data-stu-id="567bb-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="567bb-246">Vervolgens moet u het Azure AD-token gebruiken om het *toegangstoken* op te halen van de beveiligingsservice.</span><span class="sxs-lookup"><span data-stu-id="567bb-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="567bb-247">Ga als volgt te werk om een beveiligingsservicetoken te verkrijgen:</span><span class="sxs-lookup"><span data-stu-id="567bb-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="567bb-248">Meld u aan bij Azure Portal en gebruik het token om `clientId` en `clientSecret` voor uw Supply Chain Management-toepassing te zoeken.</span><span class="sxs-lookup"><span data-stu-id="567bb-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="567bb-249">Haal een Azure Active Directory-token (`aadToken`) op door een HTTP-aanvraag met de volgende eigenschappen in te dienen:</span><span class="sxs-lookup"><span data-stu-id="567bb-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="567bb-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="567bb-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="567bb-251">**methode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="567bb-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="567bb-252">**Inhoud hoofdtekst (formuliergegevens)**:</span><span class="sxs-lookup"><span data-stu-id="567bb-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="567bb-253">key</span><span class="sxs-lookup"><span data-stu-id="567bb-253">key</span></span> | <span data-ttu-id="567bb-254">waarde</span><span class="sxs-lookup"><span data-stu-id="567bb-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="567bb-255">client_id</span><span class="sxs-lookup"><span data-stu-id="567bb-255">client_id</span></span> | <span data-ttu-id="567bb-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="567bb-256">${aadAppId}</span></span> |
        | <span data-ttu-id="567bb-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="567bb-257">client_secret</span></span> | <span data-ttu-id="567bb-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="567bb-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="567bb-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="567bb-259">grant_type</span></span> | <span data-ttu-id="567bb-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="567bb-260">client_credentials</span></span> |
        | <span data-ttu-id="567bb-261">resource</span><span class="sxs-lookup"><span data-stu-id="567bb-261">resource</span></span> | <span data-ttu-id="567bb-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="567bb-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="567bb-263">U moet als reactie een `aadToken` ontvangen, zoals in het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="567bb-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="567bb-264">Formuleer een JSON-aanvraag die op het volgende lijkt:</span><span class="sxs-lookup"><span data-stu-id="567bb-264">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="567bb-265">Hierin:</span><span class="sxs-lookup"><span data-stu-id="567bb-265">Where:</span></span>
    - <span data-ttu-id="567bb-266">De waarde `client_assertion` moet het in de vorige stap ontvangen `aadToken` zijn.</span><span class="sxs-lookup"><span data-stu-id="567bb-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="567bb-267">De waarde `context` moet de omgevings-ID zijn waarin u de invoegtoepassing wilt implementeren.</span><span class="sxs-lookup"><span data-stu-id="567bb-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="567bb-268">Stel alle andere waarden in zoals in het voorbeeld wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="567bb-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="567bb-269">Dien een HTTP-aanvraag in met de volgende eigenschappen:</span><span class="sxs-lookup"><span data-stu-id="567bb-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="567bb-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="567bb-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="567bb-271">**methode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="567bb-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="567bb-272">**HTTP-header**: neem de API-versie op (sleutel is `Api-Version` en waarde is `1.0`)</span><span class="sxs-lookup"><span data-stu-id="567bb-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="567bb-273">**Inhoud hoofdtekst**: neem de JSON-aanvraag op die u in de vorige stap hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="567bb-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="567bb-274">U ontvangt als reactie een `access_token`.</span><span class="sxs-lookup"><span data-stu-id="567bb-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="567bb-275">Dit is wat u nodig hebt als Bearer-token voor het aanroepen van de Voorraadzichtbaarheid-API.</span><span class="sxs-lookup"><span data-stu-id="567bb-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="567bb-276">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="567bb-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="567bb-277">Voorbeeldaanvraag</span><span class="sxs-lookup"><span data-stu-id="567bb-277">Sample Request</span></span>

<span data-ttu-id="567bb-278">Ter referentie is hier een voorbeeld-HTTP-aanvraag, waarin u alle hulpmiddelen of programmeertaal kunt gebruiken om deze aanvraag te verzenden, zoals ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="567bb-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="567bb-279">De Voorraadzichtbaarheid-API configureren</span><span class="sxs-lookup"><span data-stu-id="567bb-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="567bb-280">Voordat u de service gaat gebruiken, moet u de configuraties uitvoeren die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="567bb-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="567bb-281">De configuratie kan variëren afhankelijk van de details van uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="567bb-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="567bb-282">Deze bevat hoofdzakelijk vier delen:</span><span class="sxs-lookup"><span data-stu-id="567bb-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="567bb-283">Partitionering</span><span class="sxs-lookup"><span data-stu-id="567bb-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="567bb-284">Dimensieconfiguraties</span><span class="sxs-lookup"><span data-stu-id="567bb-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="567bb-285">Bezig met indexeren</span><span class="sxs-lookup"><span data-stu-id="567bb-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="567bb-286">Aangepaste meting</span><span class="sxs-lookup"><span data-stu-id="567bb-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="567bb-287">Partitionering</span><span class="sxs-lookup"><span data-stu-id="567bb-287">Partitioning</span></span>

<span data-ttu-id="567bb-288">Het partitioneren kan de prestaties van de API voor Voorraadzichtbaarheid aanzienlijk beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="567bb-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="567bb-289">Het is een goed idee om een schema te definiëren waarmee kleine groeperingen van gegevens mogelijk zijn, terwijl er toch betekenisvolle gegevensquery's kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="567bb-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="567bb-290">De `organizationId` (`dataAreaId` in Supply Chain Management) zal altijd deel uitmaken van de partitionering en Voorraadzichtbaarheid is standaard ingesteld op partitioneren op dimensies als *Site + locatie*.</span><span class="sxs-lookup"><span data-stu-id="567bb-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="567bb-291">Dit betekent dat er altijd query's voor de service moeten worden uitgevoerd met deze dimensies gedefinieerd in de filters.</span><span class="sxs-lookup"><span data-stu-id="567bb-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="567bb-292">*Site* en *Locatie* zijn twee algemene standaarddimensies in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="567bb-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="567bb-293">In Supply Chain Management worden deze dimensies *Site* (`InventSiteId`) en *Magazijn* (`InventLocationId`) genoemd.</span><span class="sxs-lookup"><span data-stu-id="567bb-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="567bb-294">Dimensieconfiguraties</span><span class="sxs-lookup"><span data-stu-id="567bb-294">Dimension configurations</span></span>

<span data-ttu-id="567bb-295">In Voorraadzichtbaarheid wordt een lijst met algemene standaarddimensies geboden waarmee de integratie met meerdere bronsystemen wordt mogelijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="567bb-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="567bb-296">In de volgende tabel worden de voorraaddimensies weergegeven die de standaarddimensienamen zijn in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="567bb-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="567bb-297">Dimensietype</span><span class="sxs-lookup"><span data-stu-id="567bb-297">Dimension type</span></span> | <span data-ttu-id="567bb-298">Dimensienaam</span><span class="sxs-lookup"><span data-stu-id="567bb-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="567bb-299">Artikel</span><span class="sxs-lookup"><span data-stu-id="567bb-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="567bb-300">Artikel</span><span class="sxs-lookup"><span data-stu-id="567bb-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="567bb-301">Artikel</span><span class="sxs-lookup"><span data-stu-id="567bb-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="567bb-302">Artikel</span><span class="sxs-lookup"><span data-stu-id="567bb-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="567bb-303">Tracering</span><span class="sxs-lookup"><span data-stu-id="567bb-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="567bb-304">Tracering</span><span class="sxs-lookup"><span data-stu-id="567bb-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="567bb-305">Locatie</span><span class="sxs-lookup"><span data-stu-id="567bb-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="567bb-306">Locatie</span><span class="sxs-lookup"><span data-stu-id="567bb-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="567bb-307">Voorraadstatus</span><span class="sxs-lookup"><span data-stu-id="567bb-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="567bb-308">Magazijnspecifiek</span><span class="sxs-lookup"><span data-stu-id="567bb-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="567bb-309">Magazijnspecifiek</span><span class="sxs-lookup"><span data-stu-id="567bb-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="567bb-310">Magazijnspecifiek</span><span class="sxs-lookup"><span data-stu-id="567bb-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="567bb-311">Het dimensietype vermeld in de vorige tabel is alleen ter referentie.</span><span class="sxs-lookup"><span data-stu-id="567bb-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="567bb-312">U hoeft het dimensietype niet te definiëren in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="567bb-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="567bb-313">Als er een aangepaste dimensie bestaat en naar een standaardwaarde moet stromen bij verbruik door Voorraadzichtbaarheid, kunt u de naam **Aangepaste dimensie** in Voorraadzichtbaarheid configureren.</span><span class="sxs-lookup"><span data-stu-id="567bb-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="567bb-314">Externe systemen hebben toegang tot Voorraadzichtbaarheid via RESTful API's waarmee gegevens van voorhanden voorraad over bepaalde sets met dimensies kunnen worden opgevraagd.</span><span class="sxs-lookup"><span data-stu-id="567bb-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="567bb-315">Voor de integratie kunt u met Voorraadzichtbaarheid de *gegevensbron van het externe kanaal* en de brondimensie naar de *doeldimensies* configureren in Voorraadzichtbaarheid.</span><span class="sxs-lookup"><span data-stu-id="567bb-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="567bb-316">De doeldimensies moeten een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="567bb-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="567bb-317">Standaarddimensies in Voorraadzichtbaarheid</span><span class="sxs-lookup"><span data-stu-id="567bb-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="567bb-318">Aangepaste dimensies</span><span class="sxs-lookup"><span data-stu-id="567bb-318">Custom dimensions</span></span>

<span data-ttu-id="567bb-319">Het doel van dimensieconfiguratie is het standaardiseren van de integratie met meerdere systemen voor de query voor dimensies en de boekingsgebeurtenis met dimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="567bb-320">Bezig met indexeren</span><span class="sxs-lookup"><span data-stu-id="567bb-320">Indexing</span></span>

<span data-ttu-id="567bb-321">Meestal is de query voor de voorhanden voorraad niet alleen op het hoogste niveau 'totaal', maar wilt u mogelijk de resultaten bekijken die zijn samengevoegd op basis van de voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="567bb-322">Voorraadzichtbaarheid is flexibel omdat u de indexen kunt instellen die zijn gebaseerd op de dimensie of de combinatie van de dimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="567bb-323">Op dit moment kunt u maximaal vijf indexen configureren.</span><span class="sxs-lookup"><span data-stu-id="567bb-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="567bb-324">U moet voorafgaand aan de implementatie zorgvuldig overwegen welke dimensie of dimensiecombinatie u gaat gebruiken om er zeker van te zijn dat deze aan uw bedrijfsbehoeften voldoet.</span><span class="sxs-lookup"><span data-stu-id="567bb-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="567bb-325">Als u bijvoorbeeld als volgt producten wilt opvragen:</span><span class="sxs-lookup"><span data-stu-id="567bb-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="567bb-326">Vraag de geaggregeerde voorhanden producten op basis van de dimensies *Kleur* en *Grootte* op.</span><span class="sxs-lookup"><span data-stu-id="567bb-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="567bb-327">In sommige gevallen wilt u alleen in totaal een query voor het product uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="567bb-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="567bb-328">U zou twee indexen hebben die als volgt zijn gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="567bb-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="567bb-329">Het lege haakje aggregeert op basis van de product-ID binnen de partitie.</span><span class="sxs-lookup"><span data-stu-id="567bb-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="567bb-330">De indexering bepaalt hoe u de resultaten kunt groeperen op basis van de `groupBy`-queryinstelling.</span><span class="sxs-lookup"><span data-stu-id="567bb-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="567bb-331">Als u in dit geval geen `groupBy`-waarden definieert, krijgt u totalen op `productid`.</span><span class="sxs-lookup"><span data-stu-id="567bb-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="567bb-332">Als u `groupBy` als `groupBy=ColorId&groupBy=SizeId` definieert, worden er meerdere regels als resultaat gegeven, op basis van de verschillende combinaties van kleur en grootte in het systeem.</span><span class="sxs-lookup"><span data-stu-id="567bb-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="567bb-333">U kunt uw querycriteria in de aanvraagbody plaatsen.</span><span class="sxs-lookup"><span data-stu-id="567bb-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="567bb-334">Hier volgt een voorbeeldquery voor het product met de combinatie kleur en grootte.</span><span class="sxs-lookup"><span data-stu-id="567bb-334">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="567bb-335">Voor het veld `filters` worden momenteel alleen meerdere waarden voor `ProductId` ondersteund.</span><span class="sxs-lookup"><span data-stu-id="567bb-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="567bb-336">Als `ProductId` een lege matrix is, worden alle producten opgevraagd.</span><span class="sxs-lookup"><span data-stu-id="567bb-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="567bb-337">Aangepaste meting</span><span class="sxs-lookup"><span data-stu-id="567bb-337">Custom measurement</span></span>

<span data-ttu-id="567bb-338">De standaardmetingshoeveelheden worden gekoppeld aan Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="567bb-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="567bb-339">Maar mogelijk wilt u een hoeveelheid hebben die bestaat uit een combinatie van de standaardmetingen.</span><span class="sxs-lookup"><span data-stu-id="567bb-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="567bb-340">Hiervoor kunt u een configuratie van aangepaste hoeveelheden hebben, die worden toegevoegd aan de uitvoer van de query's voor voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="567bb-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="567bb-341">Met deze functie kunt u een set maateenheden definiëren die wordt toegevoegd, en/of een set maateenheden die wordt afgetrokken, zodat de aangepaste meting wordt gevormd.</span><span class="sxs-lookup"><span data-stu-id="567bb-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="567bb-342">Met de volgende queryvoorwaarde bijvoorbeeld configureert u de aangepaste metingshoeveelheid als `MyCustomAvailableforReservation` om te worden verbruikt door het verbruikssysteem.</span><span class="sxs-lookup"><span data-stu-id="567bb-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="567bb-343">Verbruikssysteem</span><span class="sxs-lookup"><span data-stu-id="567bb-343">Consumption system</span></span> | <span data-ttu-id="567bb-344">Berekende meters</span><span class="sxs-lookup"><span data-stu-id="567bb-344">Calculated measurers</span></span> | <span data-ttu-id="567bb-345">Gegevensbron</span><span class="sxs-lookup"><span data-stu-id="567bb-345">Data source</span></span> | <span data-ttu-id="567bb-346">Modificator</span><span class="sxs-lookup"><span data-stu-id="567bb-346">Modifier</span></span> | <span data-ttu-id="567bb-347">Berekeningstype modificator</span><span class="sxs-lookup"><span data-stu-id="567bb-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="567bb-348">Optelling</span><span class="sxs-lookup"><span data-stu-id="567bb-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="567bb-349">Optelling</span><span class="sxs-lookup"><span data-stu-id="567bb-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="567bb-350">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="567bb-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="567bb-351">Optelling</span><span class="sxs-lookup"><span data-stu-id="567bb-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="567bb-352">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="567bb-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="567bb-353">Optelling</span><span class="sxs-lookup"><span data-stu-id="567bb-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="567bb-354">Optelling</span><span class="sxs-lookup"><span data-stu-id="567bb-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="567bb-355">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="567bb-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="567bb-356">Aftrekken</span><span class="sxs-lookup"><span data-stu-id="567bb-356">Subtraction</span></span> |

<span data-ttu-id="567bb-357">Hiermee retourneert de query voor de aangepaste metingshoeveelheid de volgende uitvoer.</span><span class="sxs-lookup"><span data-stu-id="567bb-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="567bb-358">De `MyCustomAvailableforReservation`-uitvoer is gebaseerd op de berekeningsinstelling in de aangepaste metingen als:</span><span class="sxs-lookup"><span data-stu-id="567bb-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="567bb-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="567bb-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="567bb-360">Wijzigingen voorhanden voorraad boeken</span><span class="sxs-lookup"><span data-stu-id="567bb-360">Posting on-hand changes</span></span>

<span data-ttu-id="567bb-361">De exacte URL waarnaar de gebeurtenis wordt geboekt, is afhankelijk van uw geografische regio.</span><span class="sxs-lookup"><span data-stu-id="567bb-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="567bb-362">Deze heeft de volgende vorm:</span><span class="sxs-lookup"><span data-stu-id="567bb-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="567bb-363">Na verificatie kan deze URL worden gebruikt in combinatie met de HTTP `POST`-methode voor het verzenden van gebeurtenissen voor wijzigingen van de voorhanden voorraad naar de service.</span><span class="sxs-lookup"><span data-stu-id="567bb-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="567bb-364">Een speciale header wordt gebruikt voor de communicatie met Dynamics 365-services via HTTP-aanvragen, waarbij de omgevings-ID van het Supply Chain Management-exemplaar wordt aangegeven waaraan de gegevens zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="567bb-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="567bb-365">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="567bb-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="567bb-366">Queryvoorbeeld 1 voor boeken van wijzigingen voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="567bb-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="567bb-367">In dit voorbeeld ziet u een scenario waarin u de dimensieconfiguratie in Power Apps kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="567bb-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="567bb-368">Met de volgende query configureert u de dimensietoewijzing in Power Apps:</span><span class="sxs-lookup"><span data-stu-id="567bb-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="567bb-369">U kunt nu de `dimensionDataSource` opgeven en aangepaste dimensies gebruiken in uw query's.</span><span class="sxs-lookup"><span data-stu-id="567bb-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="567bb-370">Aangepaste dimensies worden automatisch omgezet in basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="567bb-371">Queryvoorbeeld 2 voor boeken van wijzigingen voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="567bb-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="567bb-372">In dit voorbeeld ziet u een scenario waarin er geen toewijzingen zijn ingesteld voor de dimensieconfiguratie in Power Apps. Daarom moet de boeking ook gebruikmaken van de basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="567bb-373">Alle dimensies moeten basisdimensies zijn als het veld `dimensionDataSource` null, leeg of een spatie is.</span><span class="sxs-lookup"><span data-stu-id="567bb-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="567bb-374">JSON-documentveldeigenschappen</span><span class="sxs-lookup"><span data-stu-id="567bb-374">JSON document field properties</span></span>

<span data-ttu-id="567bb-375">De velden uit de eerdere JSON-queryvoorbeelden hebben de eigenschappen die in de volgende tabel worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="567bb-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="567bb-376">Veld-ID</span><span class="sxs-lookup"><span data-stu-id="567bb-376">Field ID</span></span> | <span data-ttu-id="567bb-377">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="567bb-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="567bb-378">Een unieke ID voor de specifieke wijzigingsgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="567bb-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="567bb-379">Deze ID wordt gebruikt om ervoor te zorgen dat als bij het boeken de communicatie met de service mislukt, het opnieuw indienen van de gebeurtenis niet ertoe leidt dat dezelfde gebeurtenis tweemaal in het systeem wordt geteld.</span><span class="sxs-lookup"><span data-stu-id="567bb-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="567bb-380">De id van de organisatie die aan de gebeurtenis is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="567bb-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="567bb-381">Deze is toegewezen aan Supply Chain Management-organisaties of -gegevensgebied-id's.</span><span class="sxs-lookup"><span data-stu-id="567bb-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="567bb-382">De id van het betreffende product.</span><span class="sxs-lookup"><span data-stu-id="567bb-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="567bb-383">De hoeveelheid waarmee de voorhanden voorraad moet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="567bb-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="567bb-384">Als er bijvoorbeeld 10 nieuwe bagels aan een plank zijn toegevoegd, is deze waarde 10.</span><span class="sxs-lookup"><span data-stu-id="567bb-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="567bb-385">Als 3 bagels van de plank worden verwijderd of verkocht, zou deze waarde -3 zijn.</span><span class="sxs-lookup"><span data-stu-id="567bb-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="567bb-386">De gegevensbron van de dimensies gebruikt bij het boeken van de wijzigingsgebeurtenis en query.</span><span class="sxs-lookup"><span data-stu-id="567bb-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="567bb-387">Als u de gegevensbron opgeeft, kunt u de aangepaste dimensies gebruiken van de opgegeven gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="567bb-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="567bb-388">Met de dimensieconfiguratie kan Voorraadzichtbaarheid de aangepaste dimensies toewijzen aan de algemene standaarddimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="567bb-389">Als de `dimensionDataSource` niet is opgegeven, kunt u alleen de algemene standaarddimensies in uw query's gebruiken.</span><span class="sxs-lookup"><span data-stu-id="567bb-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="567bb-390">Een dynamische verzameling sleutel-waardeparen.</span><span class="sxs-lookup"><span data-stu-id="567bb-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="567bb-391">Deze worden toegewezen aan enkele dimensies in Supply Chain Management, maar u kunt ook aangepaste dimensies (zoals *Bron*) toevoegen die aangeven of de gebeurtenis afkomstig is van Supply Chain Management of een extern systeem.</span><span class="sxs-lookup"><span data-stu-id="567bb-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="567bb-392">Query uitvoeren voor huidige voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="567bb-392">Querying current on-hand</span></span>

<span data-ttu-id="567bb-393">Het eindpunt voor het uitvoeren van query's voor de huidige voorhanden voorraad heeft een vergelijkbare URL:</span><span class="sxs-lookup"><span data-stu-id="567bb-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="567bb-394">Hiervoor worden query's uitgevoerd met de HTTP `POST`-methode.</span><span class="sxs-lookup"><span data-stu-id="567bb-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="567bb-395">Queryvoorbeeld 1 huidige voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="567bb-395">Current on-hand query example 1</span></span>

<span data-ttu-id="567bb-396">In dit voorbeeld ziet u een scenario waarin u de dimensieconfiguratie al hebt voltooid in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="567bb-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="567bb-397">Met de volgende query configureert u de dimensietoewijzing in Power Apps:</span><span class="sxs-lookup"><span data-stu-id="567bb-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="567bb-398">U kunt nu de `dimensionDataSource` opgeven en aangepaste dimensies gebruiken in uw query's.</span><span class="sxs-lookup"><span data-stu-id="567bb-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="567bb-399">Aangepaste dimensies worden automatisch omgezet in basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="567bb-400">U kunt de `DimensionDataSource` opgeven in `filters` en aangepaste dimensies opgeven in `filters` en `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="567bb-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="567bb-401">Aangepaste dimensies worden automatisch omgezet in basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="567bb-402">Queryvoorbeeld 2 huidige voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="567bb-402">Current on-hand query example 2</span></span>

<span data-ttu-id="567bb-403">In dit voorbeeld ziet u een scenario waarin er geen toewijzingen zijn ingesteld voor de dimensieconfiguratie in Power Apps. Daarom moet de boeking ook gebruikmaken van de basisdimensies.</span><span class="sxs-lookup"><span data-stu-id="567bb-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="567bb-404">Alle dimensies moeten basisdimensies zijn als het veld `dimensionDataSource` onder `filters` null, leeg of een spatie is.</span><span class="sxs-lookup"><span data-stu-id="567bb-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="567bb-405">Voorbeeldretourresultaat</span><span class="sxs-lookup"><span data-stu-id="567bb-405">Example return result</span></span>

<span data-ttu-id="567bb-406">De query's die in de vorige voorbeelden worden weergegeven, kunnen een resultaat als dit retourneren.</span><span class="sxs-lookup"><span data-stu-id="567bb-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="567bb-407">De velden met hoeveelheden zijn gestructureerd als een woordenboek met metingen en de bijbehorende waarden.</span><span class="sxs-lookup"><span data-stu-id="567bb-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]