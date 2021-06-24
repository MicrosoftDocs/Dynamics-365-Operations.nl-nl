---
title: Voorspellingen voor klantbetalingen inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Financiële inzichten.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222580"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="4b6d2-103">Voorspellingen voor klantbetalingen inschakelen (preview)</span><span class="sxs-lookup"><span data-stu-id="4b6d2-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4b6d2-104">In dit onderwerp wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="4b6d2-105">U schakelt de functie in het werkgebied **Functiebeheer** in en voert de configuratie-instellingen in op de pagina **Parameters voor financiële inzichten**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="4b6d2-106">Dit onderwerp bevat ook informatie die u kan helpen bij het effectief gebruik van de functie.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="4b6d2-107">Voordat u de volgende stappen uitvoert, moet u controleren of u de vereiste stappen in het onderwerp [Configureren voor Financiële inzichten](configure-for-fin-insites.md) hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="4b6d2-108">Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="4b6d2-109">Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="4b6d2-110">(Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="4b6d2-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="4b6d2-111">Sla deze stap over als u versie 10.0.20 of hoger gebruikt of als u een Service Fabric-implementatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="4b6d2-112">Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="4b6d2-113">Als de functie niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt wanneer u deze wilt inschakelen, neemt u contact op met <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="4b6d2-114">Schakel de functie Inzichten in klantbetalingen in:</span><span class="sxs-lookup"><span data-stu-id="4b6d2-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="4b6d2-115">Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="4b6d2-116">Zoek de functie met de naam **Inzichten in klantbetalingen (preview)**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="4b6d2-117">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-117">Select **Enable now**.</span></span>

    <span data-ttu-id="4b6d2-118">De functie Inzichten in klantbetalingen is nu ingeschakeld en kan worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="4b6d2-119">Configureer de functie Inzichten in klantbetalingen:</span><span class="sxs-lookup"><span data-stu-id="4b6d2-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="4b6d2-120">Ga naar **Crediteringen en aanmaningen \> Instellen \> Financiële inzichten \> Parameters voor financiële inzichten**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="4b6d2-121">[![Pagina Parameters voor financiële inzichten voordat de functie is geconfigureerd](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="4b6d2-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="4b6d2-122">Selecteer op de pagina **Parameters voor financiële inzichten** op het tabblad **Inzichten in klantbetalingen** de koppeling **De gegevensvelden weergeven die worden gebruikt in het voorspellingsmodel** om de pagina **Gegevensvelden voor voorspellingsmodel** te openen.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="4b6d2-123">Hier kunt u de standaardlijst weergeven met velden die worden gebruikt om het AI-voorspellingsmodel te maken voor voorspellingen van klantbetalingen.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="4b6d2-124">Als u de standaardlijst met velden wilt gebruiken om het voorspellingsmodel te maken, sluit u de pagina **Gegevensvelden voor voorspellingsmodel** en stelt u vervolgens op de pagina **Parameters voor financiële inzichten** de optie **Functie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="4b6d2-125">Geef de transactieperiode 'zeer laat' op om aan te geven wat de **zeer late** voorspellingsbucket voor uw bedrijf betekent.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="4b6d2-126">Voor elke openstaande factuur wordt de betalingswaarschijnlijkheid in drie buckets voorspeld: **op tijd**, **te laat** en **zeer laat**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="4b6d2-127">**Op tijd**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze op of vóór de vervaldatum van de transactie worden betaald.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="4b6d2-128">**Te laat**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze na de vervaldatum van de transactie worden betaald, maar vóór het begin van de 'zeer late' transactieperiode.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="4b6d2-129">**Zeer laat**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze na het begin van de 'zeer late' transactieperiode worden betaald.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="4b6d2-130">Als u de 'zeer late' transactieperiode wijzigt en **Drempel voor te laat wijzigen** selecteert nadat het AI-voorspellingsmodel voor klantbetalingen is gemaakt, wordt het bestaande voorspellingsmodel verwijderd en wordt er een nieuw model gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="4b6d2-131">Met het nieuwe voorspellingsmodel worden transacties naar de 'zeer late' periode verplaatst op basis van de instellingen die zijn ingevoerd om deze te definiëren.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="4b6d2-132">Wanneer u de 'zeer late' transactieperiode hebt gedefinieerd, selecteert u **Voorspellingsmodel maken** om het voorspellingsmodel te maken.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="4b6d2-133">In de sectie **Voorspellingsmodel** op de pagina **Parameters voor financiële inzichten** wordt de status van het voorspellingsmodel weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="4b6d2-134">Wanneer het voorspellingsmodel wordt gemaakt, kunt u **Modelaanmaak opnieuw instellen** selecteren om het proces opnieuw te starten.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="4b6d2-135">De functie is nu geconfigureerd en kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="4b6d2-136">Nadat de functie is ingeschakeld en geconfigureerd en het voorspellingsmodel is gemaakt en werkt, wordt in het gedeelte **Voorspellingsmodel** van de pagina **Parameters voor financiële inzichten** de nauwkeurigheid van het model weergegeven, zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="4b6d2-137">[![Nauwkeurigheid van het voorspellingsmodel op de pagina Parameters voor financiële inzichten](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="4b6d2-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="4b6d2-138">Releasegegevens</span><span class="sxs-lookup"><span data-stu-id="4b6d2-138">Release details</span></span>

<span data-ttu-id="4b6d2-139">De openbare preview van Financiële inzichten is beschikbaar voor proefimplementaties in de Verenigde Staten van Amerika, Europa en het Verenigd Koninkrijk.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="4b6d2-140">Microsoft voegt incrementeel ondersteuning toe voor meer regio's.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="4b6d2-141">Functies van de openbare preview kunnen en zouden alleen moeten worden ingeschakeld in Tier-2 sandbox-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="4b6d2-142">Setup-modellen en AI-modellen die in een sandbox-omgeving zijn gemaakt, kunnen niet naar een productieomgeving worden gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="4b6d2-143">Zie voor meer informatie [Aanvullende gebruiksrechtovereenkomst voor Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="4b6d2-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
