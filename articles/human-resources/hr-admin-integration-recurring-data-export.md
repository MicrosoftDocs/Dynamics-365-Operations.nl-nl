---
title: Een app voor terugkerende gegevensexporten maken
description: In dit artikel wordt beschreven hoe u in Microsoft Azure een logische app kunt maken waarmee gegevens vanuit Microsoft Dynamics 365 Human Resources worden geëxporteerd volgens een gepland terugkeerpatroon.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 97972d2179c42e9d2d672cbebb75643ef0a02a62
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112052"
---
# <a name="create-a-recurring-data-export-app"></a>Een app voor terugkerende gegevensexporten maken

In dit artikel wordt beschreven hoe u in Microsoft Azure een logische app kunt maken waarmee gegevens vanuit Microsoft Dynamics 365 Human Resources worden geëxporteerd volgens een gepland terugkeerpatroon. In de zelfstudie wordt gebruikgemaakt van de REST-API (Application Programming Interface) in het DMF-pakket van Human Resources om de gegevens te exporteren. Nadat de gegevens zijn geëxporteerd, wordt het geëxporteerde gegevenspakket door de logische app opgeslagen in een map op Microsoft OneDrive voor Bedrijven.

## <a name="business-scenario"></a>Bedrijfsscenario

In een veelvoorkomend bedrijfsscenario voor Microsoft Dynamics 365-integraties moeten gegevens worden geëxporteerd naar een downstream-systeem volgens een gepland terugkeerpatroon. In deze zelfstudie ziet u hoe u alle medewerkersrecords uit Microsoft Dynamics 365 Human Resources exporteert en de lijst met medewerkers in een map op OneDrive voor Bedrijven opslaat.

> [!TIP]
> De specifieke gegevens die in deze zelfstudie worden geëxporteerd en de bestemming van de geëxporteerde gegevens zijn slechts voorbeelden. U kunt ze eenvoudig wijzigen om aan uw bedrijfsbehoeften te voldoen.

## <a name="technologies-used"></a>Gebruikte technologieën

In deze zelfstudie worden de volgende technologieën gebruikt:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – De hoofdgegevensbron voor medewerkers die worden geëxporteerd.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – De technologie waarmee de terugkerende exportbewerking kan worden georganiseerd en gepland.

    - **[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – De technologie die wordt gebruikt om de logische app aan de vereiste eindpunten te koppelen.

        - [HTTP met Azure AD](https://docs.microsoft.com/connectors/webcontents/)-connector
        - [OneDrive voor Bedrijven](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-connector

- **[REST API uit het DMF-pakket](../dev-itpro/data-entities/data-management-api.md)** – De technologie die wordt gebruikt om het exportproces te activeren en de voortgang te controleren.
- **[OneDrive voor bedrijven](https://onedrive.live.com/about/business/)** – De bestemming voor de geëxporteerde medewerkers.

## <a name="prerequisites"></a>Vereisten

Voordat u begint met de oefening in deze zelfstudie, moet u over het volgende beschikken:

- Een Human Resources-omgeving met machtigingen op beheerdersniveau in de omgeving
- Een [Azure-abonnement](https://azure.microsoft.com/free/) voor het hosten van de logische app

## <a name="the-exercise"></a>De oefening

Aan het einde van deze oefening hebt u een logische app die is verbonden met uw Human Resources-omgeving en uw OneDrive voor Bedrijven-account. De logische app exporteert een gegevenspakket uit Human Resources, wacht tot de export is voltooid, downloadt vervolgens het geëxporteerde gegevenspakket en slaat het gegevenspakket op in de map op OneDrive voor Bedrijven die u hebt opgegeven.

De voltooide logische app zal er ongeveer zo uitzien als in de volgende afbeelding.

![Overzicht van de logische app](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Stap 1: Een gegevensexportproject maken in Human Resources

Maak in Human Resources een gegevensexportproject waarmee medewerkers worden geëxporteerd. Geef het project de naam **Medewerkers exporteren** en zorg dat de optie **Gegevenspakket genereren** is ingesteld op **Ja**. Voeg een enkele entiteit (**Medewerker**) toe aan het project en selecteer de indeling waarin u wilt exporteren. (In deze zelfstudie wordt de Microsoft Excel-indeling gebruikt.)

![Het project met de gegevens van medewerkers exporteren](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Onthoud de naam van het gegevensexportproject. U hebt deze naam nodig wanneer u de logische app maakt in de volgende stap.

### <a name="step-2-create-the-logic-app"></a>Stap 2: De logische app maken

Het grootste deel van de oefening bestaat uit het maken van de logische app.

1. Maak een logische app in de Azure-portal.

    ![Pagina voor het maken van logische apps](media/integration-logic-app-creation-1.png)

2. Start in Logic Apps Designer met een lege logische app.
3. Voeg een [trigger voor de planning met terugkeerpatroon](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) toe om de logische app elke 24 uur (of volgens een door u gewenste planning) uit te voeren.

    ![Dialoogvenster voor terugkeerpatroon](media/integration-logic-app-recurrence-step.png)

4. Roep de DMF REST API [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) aan om de export van uw gegevenspakket te plannen.

    1. Gebruik de actie **Een HTTP-aanvraag aanroepen** vanuit de HTTP met de Azure AD-connector.

        - **Basisbron-URL:** de URL van uw Human Resources-omgeving (geef geen pad- of naam ruimte-informatie op.)
        - **Azure AD-bron-URI:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > De Human Resources-service biedt nog geen connector waarmee alle API's worden weergegeven die de REST API van het DMF-pakket vormen, zoals **ExportToPackage**. In plaats daarvan moet u de API's aanroepen door gebruik te maken van onbewerkte HTTPS-aanvragen via HTTP met de Azure AD-connector. Deze connector gebruikt Azure Active Directory (Azure AD) voor verificatie en autorisatie voor Human Resources.

        ![HTTP met Azure AD-connector](media/integration-logic-app-http-aad-connector-step.png)

    2. Meld u aan bij uw Human Resources-omgeving via de HTTP met de Azure AD-connector.
    3. Stel een HTTP **POST**-aanvraag in om de DMF Rest API **ExportToPackage** aan te roepen.

        - **Methode:** POST
        - **URL van de aanvraag:** https://\<hostname\>/namespaces\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Hoofdtekst van de aanvraag:**

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
    > U kunt desgewenst elke stap een andere naam geven die meer zegt dan de standaardnaam, **Een HTTP-aanvraag aanroepen**. U kunt bijvoorbeeld de naam van deze stap veranderen in **ExportToPackage**.

5. [Initialiseer een variabele](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) om de uitvoeringsstatus van de **ExportToPackage**-aanvraag op te slaan.

    ![Actie Variabele initialiseren](media/integration-logic-app-initialize-variable-step.png)

6. Wacht tot de uitvoeringsstatus van de gegevensexport **Voltooid** is.

    1. Voeg een [Until-lus](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) toe die wordt herhaald totdat de variabele **ExecutionStatus** de waarde **Voltooid** heeft.
    2. Voeg de actie **Vertraging** toe, zodat vijf seconden wordt gewacht voordat de huidige uitvoeringsstatus van de export wordt gecontroleerd.

        ![Container Until-lus](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Stel het aantal iteraties in op **15** om maximaal 75 seconden (15 keer 5 seconden) te wachten totdat de export is voltooid. Als het exporteren langer duurt, past u het aantal iteraties aan.        

    3. Voeg de actie **HTTP-aanvraag aanroepen** aan om de DMF REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) aan te roepen en stel de variabele **ExecutionStatus** in op het resultaat van de **GetExecutionSummaryStatus**-respons.

        > In dit voorbeeld wordt geen foutcontrole uitgevoerd. De API **GetExecutionSummaryStatus** kan ook definitieve mislukt-statussen retourneren (dat wil zeggen een andere status dan **Voltooid**). Zie de [API-documentatie](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) voor meer informatie.

        - **Methode:** POST
        - **URL van de aanvraag:** https://\<hostname\>/namespaces\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Hoofdtekst van de aanvraag:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Mogelijk moet u de waarde voor **hoofdtekst van de aanvraag** invoeren in de codeweergave of in de functie-editor in de ontwerpfunctie.

        ![Actie Een HTTP-aanvraag aanroepen 2](media/integration-logic-app-get-execution-status-step.png)

        ![Actie Variabele instellen](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > De waarde voor de actie **Variabele instellen** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) verschilt van de waarde voor de hoofdtekst **Een HTTP-aanvraag aanroepen 2**, hoewel de waarden in de ontwerpfunctie op dezelfde manier worden weergegeven.

7. Haal de download-URL van het geëxporteerde pakket op.

    - Voeg de actie **HTTP-aanvraag aanroepen** toe om de DMF REST API [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) aan te roepen.

        - **Methode:** POST
        - **URL van de aanvraag:** https://\<hostname\>/namespaces\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Hoofdtekst van de aanvraag:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![Actie GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. Download het geëxporteerde pakket.

    - Voeg een HTTP **GET**-aanvraag (een ingebouwde [HTTP-connectoractie](https://docs.microsoft.com/azure/connectors/connectors-native-http)) toe om het pakket te downloaden van de URL die in de vorige stap is geretourneerd.

        - **Methode:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Mogelijk moet u de **URI**-waarde invoeren in de codeweergave of in de functie-editor in de ontwerpfunctie.

        ![Actie HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Voor deze aanvraag is geen extra verificatie vereist omdat de URL die de API **GetExportedPackageUrl** retourneert, een token voor handtekeningen voor gedeelde toegang bevat dat toegang geeft tot het downloaden van het bestand.

9. Sla het gedownloade pakket op met de [OneDrive voor Bedrijven](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-connector.

    - De OneDrive voor Bedrijven-actie [Bestand maken](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) toevoegen.
    - Maak zo nodig verbinding met uw OneDrive voor Bedrijven-account.

        - **Mappad:** een door u gekozen map
        - **Bestandsnaam:** worker\_package.zip
        - **Bestandsinhoud:** de hoofdtekst van de vorige stap (dynamische inhoud)

        ![Actie Bestand maken](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Stap 3: De logische app testen

Als u de logische app wilt testen, selecteert u de knop **Uitvoeren** in de ontwerpfunctie. U ziet dat de stappen van de logische app worden uitgevoerd. Na 30 tot 40 seconden moet de logische app zijn voltooid en moet in uw OneDrive voor Bedrijven-map een nieuw pakketbestand zijn opgenomen dat de geëxporteerde medewerkers bevat.

Als er een fout wordt gerapporteerd voor een stap, selecteert u de mislukte stap in de ontwerpfunctie en bekijkt u de velden **Invoer** en **Uitvoer** voor deze stap. Spoor fouten op en pas de stap zo nodig aan om de fouten te corrigeren.

In de volgende afbeelding ziet u hoe de Logic Apps Designer eruitziet wanneer alle stappen van de logische app met succes zijn uitgevoerd.

![Geslaagde uitvoering van de logische app](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Overzicht

In deze zelfstudie hebt u geleerd hoe u een logische app kunt gebruiken om gegevens uit Human Resources te exporteren en de geëxporteerde gegevens in een OneDrive voor Bedrijven-map op te slaan. U kunt de stappen van deze zelfstudie aanpassen aan de behoeften van uw bedrijf.




[!INCLUDE[footer-include](../includes/footer-banner.md)]