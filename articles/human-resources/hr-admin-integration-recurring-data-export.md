---
title: Een app voor terugkerende gegevensexporten maken
description: In dit artikel wordt beschreven hoe u in Microsoft Azure een logische app kunt maken waarmee gegevens vanuit Microsoft Dynamics 365 Human Resources worden geëxporteerd volgens een gepland terugkeerpatroon.
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
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008576"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="a57cc-103">Een app voor terugkerende gegevensexporten maken</span><span class="sxs-lookup"><span data-stu-id="a57cc-103">Create a recurring data export app</span></span>

<span data-ttu-id="a57cc-104">In dit artikel wordt beschreven hoe u in Microsoft Azure een logische app kunt maken waarmee gegevens vanuit Microsoft Dynamics 365 Human Resources worden geëxporteerd volgens een gepland terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="a57cc-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="a57cc-105">In de zelfstudie wordt gebruikgemaakt van de REST-API (Application Programming Interface) in het DMF-pakket van Human Resources om de gegevens te exporteren.</span><span class="sxs-lookup"><span data-stu-id="a57cc-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="a57cc-106">Nadat de gegevens zijn geëxporteerd, wordt het geëxporteerde gegevenspakket door de logische app opgeslagen in een map op Microsoft OneDrive voor Bedrijven.</span><span class="sxs-lookup"><span data-stu-id="a57cc-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="a57cc-107">Bedrijfsscenario</span><span class="sxs-lookup"><span data-stu-id="a57cc-107">Business scenario</span></span>

<span data-ttu-id="a57cc-108">In een veelvoorkomend bedrijfsscenario voor Microsoft Dynamics 365-integraties moeten gegevens worden geëxporteerd naar een downstream-systeem volgens een gepland terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="a57cc-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="a57cc-109">In deze zelfstudie ziet u hoe u alle medewerkersrecords uit Microsoft Dynamics 365 Human Resources exporteert en de lijst met medewerkers in een map op OneDrive voor Bedrijven opslaat.</span><span class="sxs-lookup"><span data-stu-id="a57cc-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="a57cc-110">De specifieke gegevens die in deze zelfstudie worden geëxporteerd en de bestemming van de geëxporteerde gegevens zijn slechts voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="a57cc-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="a57cc-111">U kunt ze eenvoudig wijzigen om aan uw bedrijfsbehoeften te voldoen.</span><span class="sxs-lookup"><span data-stu-id="a57cc-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="a57cc-112">Gebruikte technologieën</span><span class="sxs-lookup"><span data-stu-id="a57cc-112">Technologies used</span></span>

<span data-ttu-id="a57cc-113">In deze zelfstudie worden de volgende technologieën gebruikt:</span><span class="sxs-lookup"><span data-stu-id="a57cc-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="a57cc-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – De hoofdgegevensbron voor medewerkers die worden geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="a57cc-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="a57cc-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – De technologie waarmee de terugkerende exportbewerking kan worden georganiseerd en gepland.</span><span class="sxs-lookup"><span data-stu-id="a57cc-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="a57cc-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – De technologie die wordt gebruikt om de logische app aan de vereiste eindpunten te koppelen.</span><span class="sxs-lookup"><span data-stu-id="a57cc-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="a57cc-117">[HTTP met Azure AD](https://docs.microsoft.com/connectors/webcontents/)-connector</span><span class="sxs-lookup"><span data-stu-id="a57cc-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="a57cc-118">[OneDrive voor Bedrijven](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-connector</span><span class="sxs-lookup"><span data-stu-id="a57cc-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="a57cc-119">**[REST API uit het DMF-pakket](../dev-itpro/data-entities/data-management-api.md)** – De technologie die wordt gebruikt om het exportproces te activeren en de voortgang te controleren.</span><span class="sxs-lookup"><span data-stu-id="a57cc-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="a57cc-120">**[OneDrive voor bedrijven](https://onedrive.live.com/about/business/)** – De bestemming voor de geëxporteerde medewerkers.</span><span class="sxs-lookup"><span data-stu-id="a57cc-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a57cc-121">Vereisten</span><span class="sxs-lookup"><span data-stu-id="a57cc-121">Prerequisites</span></span>

<span data-ttu-id="a57cc-122">Voordat u begint met de oefening in deze zelfstudie, moet u over het volgende beschikken:</span><span class="sxs-lookup"><span data-stu-id="a57cc-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="a57cc-123">Een Human Resources-omgeving met machtigingen op beheerdersniveau in de omgeving</span><span class="sxs-lookup"><span data-stu-id="a57cc-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="a57cc-124">Een [Azure-abonnement](https://azure.microsoft.com/free/) voor het hosten van de logische app</span><span class="sxs-lookup"><span data-stu-id="a57cc-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="a57cc-125">De oefening</span><span class="sxs-lookup"><span data-stu-id="a57cc-125">The exercise</span></span>

<span data-ttu-id="a57cc-126">Aan het einde van deze oefening hebt u een logische app die is verbonden met uw Human Resources-omgeving en uw OneDrive voor Bedrijven-account.</span><span class="sxs-lookup"><span data-stu-id="a57cc-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="a57cc-127">De logische app exporteert een gegevenspakket uit Human Resources, wacht tot de export is voltooid, downloadt vervolgens het geëxporteerde gegevenspakket en slaat het gegevenspakket op in de map op OneDrive voor Bedrijven die u hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="a57cc-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="a57cc-128">De voltooide logische app zal er ongeveer zo uitzien als in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="a57cc-128">The completed logic app will resemble the following illustration.</span></span>

![Overzicht van de logische app](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="a57cc-130">Stap 1: Een gegevensexportproject maken in Human Resources</span><span class="sxs-lookup"><span data-stu-id="a57cc-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="a57cc-131">Maak in Human Resources een gegevensexportproject waarmee medewerkers worden geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="a57cc-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="a57cc-132">Geef het project de naam **Medewerkers exporteren** en zorg dat de optie **Gegevenspakket genereren** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a57cc-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="a57cc-133">Voeg een enkele entiteit (**Medewerker**) toe aan het project en selecteer de indeling waarin u wilt exporteren.</span><span class="sxs-lookup"><span data-stu-id="a57cc-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="a57cc-134">(In deze zelfstudie wordt de Microsoft Excel-indeling gebruikt.)</span><span class="sxs-lookup"><span data-stu-id="a57cc-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Het project met de gegevens van medewerkers exporteren](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="a57cc-136">Onthoud de naam van het gegevensexportproject.</span><span class="sxs-lookup"><span data-stu-id="a57cc-136">Remember the name of the data export project.</span></span> <span data-ttu-id="a57cc-137">U hebt deze naam nodig wanneer u de logische app maakt in de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="a57cc-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="a57cc-138">Stap 2: De logische app maken</span><span class="sxs-lookup"><span data-stu-id="a57cc-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="a57cc-139">Het grootste deel van de oefening bestaat uit het maken van de logische app.</span><span class="sxs-lookup"><span data-stu-id="a57cc-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="a57cc-140">Maak een logische app in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="a57cc-140">In the Azure portal, create a logic app.</span></span>

    ![Pagina voor het maken van logische apps](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="a57cc-142">Start in Logic Apps Designer met een lege logische app.</span><span class="sxs-lookup"><span data-stu-id="a57cc-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="a57cc-143">Voeg een [trigger voor de planning met terugkeerpatroon](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) toe om de logische app elke 24 uur (of volgens een door u gewenste planning) uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="a57cc-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Dialoogvenster voor terugkeerpatroon](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="a57cc-145">Roep de DMF REST API [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) aan om de export van uw gegevenspakket te plannen.</span><span class="sxs-lookup"><span data-stu-id="a57cc-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="a57cc-146">Gebruik de actie **Een HTTP-aanvraag aanroepen** vanuit de HTTP met de Azure AD-connector.</span><span class="sxs-lookup"><span data-stu-id="a57cc-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="a57cc-147">**Basisbron-URL:** de URL van uw Human Resources-omgeving (geef geen pad- of naam ruimte-informatie op.)</span><span class="sxs-lookup"><span data-stu-id="a57cc-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="a57cc-148">**Azure AD-bron-URI:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="a57cc-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="a57cc-149">De Human Resources-service biedt nog geen connector waarmee alle API's worden weergegeven die de REST API van het DMF-pakket vormen, zoals **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="a57cc-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="a57cc-150">In plaats daarvan moet u de API's aanroepen door gebruik te maken van onbewerkte HTTPS-aanvragen via HTTP met de Azure AD-connector.</span><span class="sxs-lookup"><span data-stu-id="a57cc-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="a57cc-151">Deze connector gebruikt Azure Active Directory (Azure AD) voor verificatie en autorisatie voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a57cc-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP met Azure AD-connector](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="a57cc-153">Meld u aan bij uw Human Resources-omgeving via de HTTP met de Azure AD-connector.</span><span class="sxs-lookup"><span data-stu-id="a57cc-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="a57cc-154">Stel een HTTP **POST**-aanvraag in om de DMF Rest API **ExportToPackage** aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="a57cc-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="a57cc-155">**Methode:** POST</span><span class="sxs-lookup"><span data-stu-id="a57cc-155">**Method:** POST</span></span>
        - <span data-ttu-id="a57cc-156">**URL van de aanvraag:** https://\<hostnaam\>/namespaces/\<naamruimte\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="a57cc-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="a57cc-157">**Hoofdtekst van de aanvraag:**</span><span class="sxs-lookup"><span data-stu-id="a57cc-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Actie Een HTTP-aanvraag aanroepen](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="a57cc-159">U kunt desgewenst elke stap een andere naam geven die meer zegt dan de standaardnaam, **Een HTTP-aanvraag aanroepen**.</span><span class="sxs-lookup"><span data-stu-id="a57cc-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="a57cc-160">U kunt bijvoorbeeld de naam van deze stap veranderen in **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="a57cc-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="a57cc-161">[Initialiseer een variabele](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) om de uitvoeringsstatus van de **ExportToPackage**-aanvraag op te slaan.</span><span class="sxs-lookup"><span data-stu-id="a57cc-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Actie Variabele initialiseren](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="a57cc-163">Wacht tot de uitvoeringsstatus van de gegevensexport **Voltooid** is.</span><span class="sxs-lookup"><span data-stu-id="a57cc-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="a57cc-164">Voeg een [Until-lus](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) toe die wordt herhaald totdat de variabele **ExecutionStatus** de waarde **Voltooid** heeft.</span><span class="sxs-lookup"><span data-stu-id="a57cc-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="a57cc-165">Voeg de actie **Vertraging** toe, zodat vijf seconden wordt gewacht voordat de huidige uitvoeringsstatus van de export wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="a57cc-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Container Until-lus](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="a57cc-167">Stel het aantal iteraties in op **15** om maximaal 75 seconden (15 keer 5 seconden) te wachten totdat de export is voltooid.</span><span class="sxs-lookup"><span data-stu-id="a57cc-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="a57cc-168">Als het exporteren langer duurt, past u het aantal iteraties aan.</span><span class="sxs-lookup"><span data-stu-id="a57cc-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="a57cc-169">Voeg de actie **HTTP-aanvraag aanroepen** aan om de DMF REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) aan te roepen en stel de variabele **ExecutionStatus** in op het resultaat van de **GetExecutionSummaryStatus**-respons.</span><span class="sxs-lookup"><span data-stu-id="a57cc-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="a57cc-170">In dit voorbeeld wordt geen foutcontrole uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a57cc-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="a57cc-171">De API **GetExecutionSummaryStatus** kan ook definitieve mislukt-statussen retourneren (dat wil zeggen een andere status dan **Voltooid**).</span><span class="sxs-lookup"><span data-stu-id="a57cc-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="a57cc-172">Zie de [API-documentatie](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a57cc-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="a57cc-173">**Methode:** POST</span><span class="sxs-lookup"><span data-stu-id="a57cc-173">**Method:** POST</span></span>
        - <span data-ttu-id="a57cc-174">**URL van de aanvraag:** https://\<hostnaam\>/namespaces/\<naamruimte\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="a57cc-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="a57cc-175">**Hoofdtekst van de aanvraag:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="a57cc-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="a57cc-176">Mogelijk moet u de waarde voor **hoofdtekst van de aanvraag** invoeren in de codeweergave of in de functie-editor in de ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="a57cc-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Actie Een HTTP-aanvraag aanroepen 2](media/integration-logic-app-get-execution-status-step.png)

        ![Actie Variabele instellen](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="a57cc-179">De waarde voor de actie **Variabele instellen** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) verschilt van de waarde voor de hoofdtekst **Een HTTP-aanvraag aanroepen 2**, hoewel de waarden in de ontwerpfunctie op dezelfde manier worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a57cc-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="a57cc-180">Haal de download-URL van het geëxporteerde pakket op.</span><span class="sxs-lookup"><span data-stu-id="a57cc-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="a57cc-181">Voeg de actie **HTTP-aanvraag aanroepen** toe om de DMF REST API [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="a57cc-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="a57cc-182">**Methode:** POST</span><span class="sxs-lookup"><span data-stu-id="a57cc-182">**Method:** POST</span></span>
        - <span data-ttu-id="a57cc-183">**URL van de aanvraag:** https://\<hostnaam\>/namespaces/\<naamruimte\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="a57cc-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="a57cc-184">**Hoofdtekst van de aanvraag:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="a57cc-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![Actie GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="a57cc-186">Download het geëxporteerde pakket.</span><span class="sxs-lookup"><span data-stu-id="a57cc-186">Download the exported package.</span></span>

    - <span data-ttu-id="a57cc-187">Voeg een HTTP **GET**-aanvraag (een ingebouwde [HTTP-connectoractie](https://docs.microsoft.com/azure/connectors/connectors-native-http)) toe om het pakket te downloaden van de URL die in de vorige stap is geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="a57cc-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="a57cc-188">**Methode:** GET</span><span class="sxs-lookup"><span data-stu-id="a57cc-188">**Method:** GET</span></span>
        - <span data-ttu-id="a57cc-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="a57cc-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="a57cc-190">Mogelijk moet u de **URI**-waarde invoeren in de codeweergave of in de functie-editor in de ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="a57cc-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![Actie HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="a57cc-192">Voor deze aanvraag is geen extra verificatie vereist omdat de URL die de API **GetExportedPackageUrl** retourneert, een token voor handtekeningen voor gedeelde toegang bevat dat toegang geeft tot het downloaden van het bestand.</span><span class="sxs-lookup"><span data-stu-id="a57cc-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="a57cc-193">Sla het gedownloade pakket op met de [OneDrive voor Bedrijven](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-connector.</span><span class="sxs-lookup"><span data-stu-id="a57cc-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="a57cc-194">De OneDrive voor Bedrijven-actie [Bestand maken](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a57cc-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="a57cc-195">Maak zo nodig verbinding met uw OneDrive voor Bedrijven-account.</span><span class="sxs-lookup"><span data-stu-id="a57cc-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="a57cc-196">**Mappad:** een door u gekozen map</span><span class="sxs-lookup"><span data-stu-id="a57cc-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="a57cc-197">**Bestandsnaam:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="a57cc-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="a57cc-198">**Bestandsinhoud:** de hoofdtekst van de vorige stap (dynamische inhoud)</span><span class="sxs-lookup"><span data-stu-id="a57cc-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Actie Bestand maken](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="a57cc-200">Stap 3: De logische app testen</span><span class="sxs-lookup"><span data-stu-id="a57cc-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="a57cc-201">Als u de logische app wilt testen, selecteert u de knop **Uitvoeren** in de ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="a57cc-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="a57cc-202">U ziet dat de stappen van de logische app worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a57cc-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="a57cc-203">Na 30 tot 40 seconden moet de logische app zijn voltooid en moet in uw OneDrive voor Bedrijven-map een nieuw pakketbestand zijn opgenomen dat de geëxporteerde medewerkers bevat.</span><span class="sxs-lookup"><span data-stu-id="a57cc-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="a57cc-204">Als er een fout wordt gerapporteerd voor een stap, selecteert u de mislukte stap in de ontwerpfunctie en bekijkt u de velden **Invoer** en **Uitvoer** voor deze stap.</span><span class="sxs-lookup"><span data-stu-id="a57cc-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="a57cc-205">Spoor fouten op en pas de stap zo nodig aan om de fouten te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="a57cc-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="a57cc-206">In de volgende afbeelding ziet u hoe de Logic Apps Designer eruitziet wanneer alle stappen van de logische app met succes zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a57cc-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Geslaagde uitvoering van de logische app](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="a57cc-208">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a57cc-208">Summary</span></span>

<span data-ttu-id="a57cc-209">In deze zelfstudie hebt u geleerd hoe u een logische app kunt gebruiken om gegevens uit Human Resources te exporteren en de geëxporteerde gegevens in een OneDrive voor Bedrijven-map op te slaan.</span><span class="sxs-lookup"><span data-stu-id="a57cc-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="a57cc-210">U kunt de stappen van deze zelfstudie aanpassen aan de behoeften van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="a57cc-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>


