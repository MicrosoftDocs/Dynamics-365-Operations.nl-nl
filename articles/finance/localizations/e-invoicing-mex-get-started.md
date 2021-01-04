---
title: Aan de slag met de invoegtoepassing voor elektronische facturering voor Mexico
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Mexico in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6d15a79a359b3c708b2b33893d700377a57c3eb7
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512229"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a><span data-ttu-id="d5cc4-103">Aan de slag met de invoegtoepassing voor elektronische facturering voor Mexico</span><span class="sxs-lookup"><span data-stu-id="d5cc4-103">Get started with the Electronic invoicing add-on for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="d5cc4-104">De invoegtoepassing Elektronische facturering voor Mexico ondersteunt momenteel mogelijk niet alle functies die beschikbaar zijn in het document Comprobante Fiscal Digital por Internet (CFDI) en in de gerelateerde integratie die in Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management is ingebouwd.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-104">The Electronic invoicing add-on for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d5cc4-105">Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Mexico.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Mexico.</span></span> <span data-ttu-id="d5cc4-106">U wordt door de configuratiestappen geleid die landafhankelijk zijn in de Regulatory Configuration Services (RCS) en Finance.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="d5cc4-107">Daarnaast begeleidt het u door de stappen die u moet volgen om CFDI-facturen via de service in te dienen en er wordt uitgelegd hoe u de verwerkingsresultaten en de status van CFDI-facturen controleert.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d5cc4-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="d5cc4-108">Prerequisites</span></span>

<span data-ttu-id="d5cc4-109">Voordat u de stappen in dit onderwerp uitvoert, moet u de stappen uitvoeren in [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="d5cc4-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="d5cc4-110">RCS-instellingen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-110">RCS setup</span></span>

<span data-ttu-id="d5cc4-111">Tijdens de RCS-instelling voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="d5cc4-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="d5cc4-112">De functie e-Facturering voor het verwerken van CFDI-facturen importeren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="d5cc4-113">Controleer de indelingsconfiguraties die nodig zijn voor het genereren, verzenden en ontvangen van antwoorden over CFDI-facturen en het indienen en ontvangen van antwoorden over annulering.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="d5cc4-114">De gebeurtenissen configureren die de scenario's voor verzending van CFDI-facturen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="d5cc4-115">De functie e-Facturering voor CFDI-facturen publiceren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="d5cc4-116">'De functie e-Facturering' is de algemene naam voor de resource die wordt geconfigureerd en gepubliceerd voor gebruik op de server van de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="d5cc4-117">In dit geval zijn CFDI-facturen (MX) de functie e-Facturering die u gaat instellen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="d5cc4-118">De functie e-Facturering importeren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="d5cc4-119">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="d5cc4-120">Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Functies** de tegel **e-Facturering**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="d5cc4-121">Op de pagina **Functies voor e-Facturering** selecteert u **Importeren** om de **CFDI-facturen (MX)** uit de algemene opslagplaats te importeren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5cc4-122">Als de functie niet in de lijst wordt weergeven, selecteert u **Synchroniseren** en herhaalt u stap 3.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![De CFDI-facturen (MX)-functie importeren](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="d5cc4-124">Wanneer u de **CFDI-facturen (MX)** importeert vanuit de algemene opslagplaats, worden alle functie-instellingen, inclusief configuraties en acties, ook geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="d5cc4-125">Een nieuwe versie van de functie CFDI-facturen (MX) maken</span><span class="sxs-lookup"><span data-stu-id="d5cc4-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="d5cc4-126">U kunt een nieuwe versie maken als bijvoorbeeld URL's moeten worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="d5cc4-127">Zie [e-Facturering CFDI](tasks/mx-00010-e-invoicing-cfdi.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="d5cc4-128">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Een nieuwe versie van de functie e-Facturering toevoegen](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="d5cc4-130">De configuratieversie bijwerken</span><span class="sxs-lookup"><span data-stu-id="d5cc4-130">Update the configuration version</span></span>

1. <span data-ttu-id="d5cc4-131">Op de pagina **Functies voor e-Facturering** selecteert u op het tabblad **Configuraties** de optie **Toevoegen** of **Verwijderen** om de configuratieversies (configuraties van de ER-bestandsindeling) te beheren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Configuraties voor de functies van e-Facturering beheren](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="d5cc4-133">Wanneer u een nieuwe versie maakt, worden alle configuraties overgenomen van de laatst gepubliceerde versie.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="d5cc4-134">Voor het verwerken van CFDI-facturen zijn de volgende configuraties vereist:</span><span class="sxs-lookup"><span data-stu-id="d5cc4-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="d5cc4-135">CFDI-factuur (BusinessdocumentService)</span><span class="sxs-lookup"><span data-stu-id="d5cc4-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="d5cc4-136">CFDI-antwoordbericht importeren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-136">CFDI response message import</span></span>
    - <span data-ttu-id="d5cc4-137">CFDI-foutenlogboek importeren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-137">CFDI error log import</span></span>
    - <span data-ttu-id="d5cc4-138">CFDI-annuleringsverzoek (MX) (BusinessdocumentService)</span><span class="sxs-lookup"><span data-stu-id="d5cc4-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="d5cc4-139">CFDI-factuur (BusinessdocumentService)</span><span class="sxs-lookup"><span data-stu-id="d5cc4-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="d5cc4-140">Selecteer een configuratieversie in de lijst en selecteer **Bewerken** of **Weergeven** om de pagina **Indelingsontwerper** te openen. Hier kunt u de configuratie bewerken of weergeven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![De pagina Indelingsontwerper openen](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="d5cc4-142">Gebruik de pagina **Indelingsontwerper** om de configuratie van bestanden met een ER-indeling te bewerken en weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="d5cc4-143">Zie [Configuraties voor elektronische documenten maken](../../dev-itpro/analytics/electronic-reporting-configuration.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Pagina Indelingsontwerper](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="d5cc4-145">De instellingen voor de functie e-Facturering beheren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="d5cc4-146">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** de optie **Toevoegen**, **Verwijderen** of **Bewerken** om de instellingen van de functie e-Facturering te beheren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![De instellingen voor de functie e-Facturering beheren](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="d5cc4-148">Als u CFDI-facturen wilt indienen voor autorisatie (het XML-bestand genereren, het XML-bestand verzenden en het antwoord verwerken), moet u de functie **Verkoopfactuur** instellen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="d5cc4-149">Voor het indienen van een annulering van een CFDI-factuur, moet u de functie **Annulering** en **Annuleren** instellen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="d5cc4-150">De instellingen van de functie Verkoopfactuur configureren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="d5cc4-151">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** in de kolom **Functie-instelling** de optie **Verkoopfactuur**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="d5cc4-152">Selecteer **Bewerken** om de acties, regels voor toepasbaarheid en variabelen te configureren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![De instellingen voor de functie e-Facturering bewerken](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="d5cc4-154">Selecteer op de pagina **Instellingen functieversie** het tabblad **Acties** om de lijst met acties te beheren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="d5cc4-155">Met acties kunt u een lijst met bewerkingen definiëren die na elkaar moeten worden uitgevoerd om de gebeurtenis volledig uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Tabblad Acties](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="d5cc4-157">Actie-ID</span><span class="sxs-lookup"><span data-stu-id="d5cc4-157">Action ID</span></span> | <span data-ttu-id="d5cc4-158">Actie</span><span class="sxs-lookup"><span data-stu-id="d5cc4-158">Action</span></span>                   | <span data-ttu-id="d5cc4-159">Naam actie</span><span class="sxs-lookup"><span data-stu-id="d5cc4-159">Action name</span></span>                                  | <span data-ttu-id="d5cc4-160">Omschrijving van de actie</span><span class="sxs-lookup"><span data-stu-id="d5cc4-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="d5cc4-161">1</span><span class="sxs-lookup"><span data-stu-id="d5cc4-161">1</span></span>         | <span data-ttu-id="d5cc4-162">Document transformeren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-162">Transform document</span></span>       | <span data-ttu-id="d5cc4-163">CFDI e-Factuur genereren zonder digitale handtekening</span><span class="sxs-lookup"><span data-stu-id="d5cc4-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="d5cc4-164">Genereer de CFDI e-Factuur.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="d5cc4-165">2</span><span class="sxs-lookup"><span data-stu-id="d5cc4-165">2</span></span>         | <span data-ttu-id="d5cc4-166">Document ondertekenen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-166">Sign document</span></span>            | <span data-ttu-id="d5cc4-167">Digitale handtekening</span><span class="sxs-lookup"><span data-stu-id="d5cc4-167">Digital sign</span></span>                                 | <span data-ttu-id="d5cc4-168">De elektronische factuur digitaal ondertekenen voor verzending.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="d5cc4-169">3</span><span class="sxs-lookup"><span data-stu-id="d5cc4-169">3</span></span>         | <span data-ttu-id="d5cc4-170">Mexicaanse PAC-service aanroepen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-170">Call Mexican PAC service</span></span> | <span data-ttu-id="d5cc4-171">CFDI e-Factuur indienen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="d5cc4-172">De WCF-client (Windows Communication Foundation) verzendt de CFDI e-Factuur.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="d5cc4-173">4</span><span class="sxs-lookup"><span data-stu-id="d5cc4-173">4</span></span>         | <span data-ttu-id="d5cc4-174">Reactie verwerken</span><span class="sxs-lookup"><span data-stu-id="d5cc4-174">Process response</span></span>         | <span data-ttu-id="d5cc4-175">Reactie van webservice analyseren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-175">Analyze web service response</span></span>                 | <span data-ttu-id="d5cc4-176">Analyseer de reactie van de webservice en stuur het foutenlogboek terug.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="d5cc4-177">De URL voor Mexicaanse PAC-webservices instellen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="d5cc4-178">Ga naar de pagina **Instellingen functieversie** en selecteer op het tabblad **Acties**, op het sneltabblad **Acties** de optie **Mexicaanse PAC-service aanroepen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="d5cc4-179">Voer op het sneltabblad **Parameters** in het veld **URL-adres** de URL van de webservice voor het indienen van CFDI-facturen in.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="d5cc4-180">Gebruik dezelfde stappen om de URL voor de actie **Mexicaanse PAC-service aanroepen** bij te werken voor de functie-instellingen van **Annuleren** en **Annuleringsverzoek**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="d5cc4-181">De conceptversie toewijzen aan een e-Factureringsomgeving</span><span class="sxs-lookup"><span data-stu-id="d5cc4-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="d5cc4-182">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Omgevingen** de optie **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="d5cc4-183">Selecteer de omgeving in het veld **Omgeving**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="d5cc4-184">Selecteer in het veld **Geldig vanaf** de ingangsdatum van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="d5cc4-185">Selecteer **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-185">Select **Enable**.</span></span>

![Een e-Factureringsomgeving inschakelen](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="d5cc4-187">De versiestatus wijzigen in Voltooid</span><span class="sxs-lookup"><span data-stu-id="d5cc4-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="d5cc4-188">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="d5cc4-189">Selecteer **Status wijzigen \> Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="d5cc4-190">De versiestatus wijzigen in Gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="d5cc4-190">Change the version status to Published</span></span>

- <span data-ttu-id="d5cc4-191">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de optie **Status wijzigen \> Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="d5cc4-192">De functie e-Facturering publiceren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="d5cc4-193">Op de pagina **Functies voor e-Facturering** selecteert u het tabblad **Versies** om de status van de functie **CFDI-facturen (MX)** te beheren.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="d5cc4-194">Selecteer **Status wijzigen** als u de status van de functie wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-194">Select **Change status** to change the status of the feature.</span></span>

![De status van de functie e-Facturering wijzigen](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="d5cc4-196">Integratie van invoegtoepassing voor elektronisch factureren instellen in Finance</span><span class="sxs-lookup"><span data-stu-id="d5cc4-196">Set up Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="d5cc4-197">Als u de invoegtoepassing voor elektronische facturering in Finance wilt instellen, voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="d5cc4-197">To set up the Electronic invoicing add-on in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="d5cc4-198">Importeer het ER-gegevensmodel, de toewijzing voor het ER-gegevensmodel en de indelingen die nodig zijn voor CFDI-facturen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="d5cc4-199">Responstypen configureren voor het bijwerken van de CFDI-facturen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="d5cc4-200">Deze responstypen worden gebruikt voor de respons van de PAC-server (geautoriseerde certificeringsaanbieder).</span><span class="sxs-lookup"><span data-stu-id="d5cc4-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="d5cc4-201">Het ER-gegevensmodel, de toewijzing voor het ER-gegevensmodel en contextconfiguraties voor CFDI-facturen importeren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="d5cc4-202">Meld u aan bij Finance.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="d5cc4-203">Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="d5cc4-204">Controleer of deze configuratieaanbieder is ingesteld op **Actief**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="d5cc4-205">Zie [Aanbieders van configuraties maken en deze als actief markeren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) voor informatie over de manier waarop u een aanbieder als deze als **Actief** kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="d5cc4-206">Selecteer **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="d5cc4-207">Selecteer **Algemene resource \> Openen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="d5cc4-208">Importeer **Factuurmodel**, **Factuurmodeltoewijzing**, **CFDI-factuurindeling (MX)**, **Indeling annuleringsverzoek CFDI-factuur (MX)** en **Indeling annulering CFDI-factuur (MX)**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="d5cc4-209">De functie voor de verwerking van CFDI-facturen inschakelen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="d5cc4-210">Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="d5cc4-211">Schakel op het tabblad **Functies** het selectievakje **Inschakelen** in bij de rijen voor functiereferenties **MX-00010** en **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![De functies voor de verwerking van CFDI-facturen inschakelen](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="d5cc4-213">ER-configuraties importeren en responstypen instellen voor het bijwerken van CFDI-facturen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="d5cc4-214">ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="d5cc4-214">Import ER configurations</span></span>

1. <span data-ttu-id="d5cc4-215">Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="d5cc4-216">Selecteer **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="d5cc4-217">Selecteer **Algemene resource \> Openen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="d5cc4-218">Importeer **Model responsbericht**, **CFDI-foutenlogboek importeren (MX)** en **CFDI-responsbericht importeren (MX)**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="d5cc4-219">De responstypen instellen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-219">Set up the response types</span></span>

1. <span data-ttu-id="d5cc4-220">Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="d5cc4-221">Selecteer op het tabblad **Elektronisch document** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="d5cc4-222">Voer het klantfactuurjournaal in en selecteer in het veld **Tabelnaam** de projectfactuur.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="d5cc4-223">Definieer voor elke tabel een gerelateerde documentcontext:</span><span class="sxs-lookup"><span data-stu-id="d5cc4-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="d5cc4-224">Voer voor **Klantfactuurjournaal** de optie **Klantfactuurcontext** in.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="d5cc4-225">Voer voor **Projectfactuur** de optie **Projectfactuurcontext** in.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="d5cc4-226">Selecteer **Responstypen** om de responstypen te configureren die kunnen worden geretourneerd vanuit de invoegtoepassing voor elektronische facturering en die worden opgenomen in een klantfactuurjournaal of projectfactuur.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-226">Select **Response types** to configure the response types that can be returned from the Electronic invoicing add-on and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="d5cc4-227">Selecteer **Nieuw** en selecteer in het veld **Responstype** de optie **Respons**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="d5cc4-228">Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="d5cc4-229">Selecteer in het veld **Modeltoewijzing** de optie **Importindeling responsbericht – Modeltoewijzing van responsbericht**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="d5cc4-230">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-230">Select **Save**.</span></span>
9. <span data-ttu-id="d5cc4-231">Selecteer **Nieuw** en selecteer in het veld **Responstype** de optie **Responsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="d5cc4-232">Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="d5cc4-233">Selecteer in het veld **Modeltoewijzing** de optie **Importindeling CFDI-responsgegevens (details) – Responsgegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="d5cc4-234">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="d5cc4-235">Elektronische facturen in Finance verwerken</span><span class="sxs-lookup"><span data-stu-id="d5cc4-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="d5cc4-236">Tijdens de verwerking van CFDI-facturen in Finance via de invoegtoepassing voor elektronische facturering kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="d5cc4-236">During the processing of CFDI invoices in Finance through the Electronic invoicing add-on, you can perform the following tasks:</span></span>

- <span data-ttu-id="d5cc4-237">CFDI-facturen indienen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="d5cc4-238">De uitvoeringslogboeken voor het indienen weergeven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-238">View the submission execution logs.</span></span>
- <span data-ttu-id="d5cc4-239">De annulering van een CFDI-factuur indienen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="d5cc4-240">CFDI-facturen indienen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-240">Submit CFDI invoices</span></span>

<span data-ttu-id="d5cc4-241">Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, kunt u het proces **Elektronische factuur exporteren/importeren** (**Klanten \> Facturen \> E-facturen**) voor het indienen van CFDI-facturen niet meer gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-241">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="d5cc4-242">Het wordt vervangen door een nieuw proces met de naam **Elektronische documenten indienen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="d5cc4-243">Voordat u het nieuwe proces **Elektronische documenten indienen** gebruikt, moet u controleren of de instellingen die nodig zijn voor de Mexicaanse e-facturen zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="d5cc4-244">Zie [CFDI-indeling versie 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="d5cc4-245">Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Elektronische documenten indienen**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="d5cc4-246">Als u een document voor het eerst indient, moet u altijd de optie **Documenten opnieuw indienen** op **Nee** instellen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="d5cc4-247">Stel deze optie in op **Ja** als u een document opnieuw moet indienen via de service.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="d5cc4-248">Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het dialoogvenster **Query** te openen. Hier kunt u een query samenstellen om documenten te selecteren die u wilt indienen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Een CFDI-document indienen](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="d5cc4-250">Wanneer u voor het eerst een document via de service verzendt, wordt u gevraagd de verbinding met de invoegtoepassing voor elektronische facturering te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="d5cc4-251">Selecteer **Klik hier om verbinding te maken met de service voor het indienen van elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="d5cc4-252">Indieningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="d5cc4-252">View submission logs</span></span>

<span data-ttu-id="d5cc4-253">U kunt de indieningslogboeken voor alle ingediende documenten of voor slechts één ingediend document weergeven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="d5cc4-254">Alle indieningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="d5cc4-254">View all submission logs</span></span>

<span data-ttu-id="d5cc4-255">Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, is er een nieuwe pagina beschikbaar waarmee u het indieningsproces voor documenten kunt opvolgen.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-255">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="d5cc4-256">U kunt deze pagina gebruiken om de indieningslogboeken voor alle ingediende documenten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="d5cc4-257">Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="d5cc4-258">Selecteer in het veld **Documenttype** **Klantfactuurjournaal** om te filteren op de vereiste elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Een documenttype selecteren om de indieningslogboeken weer te geven](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="d5cc4-260">Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Details van indieningslogboeken weergeven](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="d5cc4-262">De informatie in de indieningslogboeken wordt verdeeld over drie sneltabbladen:</span><span class="sxs-lookup"><span data-stu-id="d5cc4-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="d5cc4-263">**Verwerkingsacties**: dit sneltabblad toont het uitvoeringslogboek voor de acties die zijn geconfigureerd in de functieversie die is ingesteld in RCS.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="d5cc4-264">De kolom **Status** geeft aan of de actie met goed gevolg is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="d5cc4-265">**Actiebestanden**: dit sneltabblad toont de tussenliggende bestanden die zijn gegenereerd tijdens de uitvoering van de acties.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="d5cc4-266">U kunt **Weergave** selecteren om het bestand te downloaden en weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="d5cc4-267">**Logboek verwerkingsacties**: dit sneltabblad toont de resultaten van de communicatie tussen de invoegtoepassing voor elektronische facturering en de doelwebservice.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-267">**Processing action log** – This FastTab shows the results of the communication between the Electronic invoicing add-on and the target web service.</span></span> <span data-ttu-id="d5cc4-268">Het toont ook wat er is geretourneerd door de verwerking vanuit de webservice.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="d5cc4-269">De kolom **Foutcode** geeft de retourcode weer die is geretourneerd door de autorisatie-webservice.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="d5cc4-270">Wanneer de ingediende CFDI-factuur is geautoriseerd, wordt de status ervan gewijzigd in **Goedgekeurd**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="d5cc4-271">Indieningslogboeken weergeven vanuit CFDI-facturen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="d5cc4-272">Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, kunt u ook de indieningslogboeken van CFDI-facturen weergeven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-272">After you turn on the **ConfigurableElectronic invoicing add-on integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="d5cc4-273">Ga naar **Klanten \> Query's en rapporten \> CFDI (elektronische facturen)**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="d5cc4-274">Selecteer een CFDI-factuur die is ingediend nadat de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>
3. <span data-ttu-id="d5cc4-275">Selecteer in het actievenster op het tabblad **Historie** de optie **Logboek elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Indieningslogboeken weergeven vanuit CFDI-facturen](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="d5cc4-277">Voor CFDI-facturen die zijn ingediend voordat de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** is ingeschakeld, is de knop **Historie** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing add-on integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="d5cc4-278">De knop **Historie** is niet beschikbaar voor CFDI-facturen die zijn ingediend nadat de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="d5cc4-279">De annulering van CFDI-facturen indienen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="d5cc4-280">Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, kan het oude proces voor het annuleren van CFDI-facturen niet meer worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-280">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="d5cc4-281">Deze wordt vervangen door een nieuw annuleringsproces dat is ingesloten op de pagina **Indieningslogboek voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="d5cc4-282">Ga naar **Klanten \> Query's en rapporten \> CFDI (elektronische facturen)**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="d5cc4-283">Als de CFDI-factuur de status **Goedgekeurd** heeft , selecteert u **Functies \> CFDI annuleren**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="d5cc4-284">Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="d5cc4-285">Selecteer de CFDI-factuur en selecteer **Functies \> Gerelateerde indieningen verzenden**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="d5cc4-286">Voer een omschrijving voor de gerelateerde indiening in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="d5cc4-287">Indieningslogboeken van annuleringen weergeven</span><span class="sxs-lookup"><span data-stu-id="d5cc4-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="d5cc4-288">Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="d5cc4-289">Selecteer in het veld **Documenttype** **Klantfactuurjournaal** om alleen te filteren op klantfactuurjournaaldocumenten.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="d5cc4-290">Selecteer de CFDI-factuur en selecteer in het actievenster **Query's \> Gerelateerde indiening**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="d5cc4-291">De pagina **Gerelateerde indieningen** toont alle gerelateerde indieningen en de bijbehorende status voor een bepaalde CFDI-factuur.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="d5cc4-292">In de volgende afbeelding staat de eerste regel voor de indiening waarin om goedkeuring van de CFDI-factuur werd gevraagd.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="d5cc4-293">De tweede regel staat voor de indiening waarmee die CFDI-factuur werd geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Indieningslogboeken van annuleringen weergeven](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="d5cc4-295">Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Details van indieningslogboeken van annuleringen weergeven](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="d5cc4-297">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="d5cc4-297">Privacy notice</span></span>
<span data-ttu-id="d5cc4-298">Als u de functies MX-00010 en MX-00016 (CFDI-factuur en CFDI-annulering) inschakelt, moet u misschien beperkte gegevens verzenden, waaronder de btw-id van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-298">Enabling the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="d5cc4-299">Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar de belastingdienst te verzenden in de vooraf gedefinieerde indeling die nodig is voor integratie met de webservice van de overheid.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="d5cc4-300">Een beheerder kan de functies MX-00010 en MX-00016 (CFDI-factuur en CFDI-annulering) in- en uitschakelen door te navigeren naar **Organisatiebeheer \> Instellingen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-300">An administrator can enable and disable the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="d5cc4-301">Selecteer het tabblad **Functies** en selecteer de rijen met de functies MX-00010 en MX-00016 en maak de gewenste selectie.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-301">Select the **Features** tab, select the rows containing the MX-00010 and MX-00016 features, and then make the appropriate selection.</span></span> <span data-ttu-id="d5cc4-302">Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="d5cc4-303">Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d5cc4-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5cc4-304">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-304">Additional resources</span></span>

- [<span data-ttu-id="d5cc4-305">Overzicht van de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="d5cc4-305">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="d5cc4-306">Aan de slag met de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="d5cc4-306">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="d5cc4-307">De invoegtoepassing voor elektronische facturering instellen</span><span class="sxs-lookup"><span data-stu-id="d5cc4-307">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
