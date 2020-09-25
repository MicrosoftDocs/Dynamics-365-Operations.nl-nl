---
title: ER-bestemmingstype voor e-mail
description: Dit onderwerp bevat informatie over het configureren van een e-mailbestemming voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745556"
---
# <a name="email-destination"></a><span data-ttu-id="68078-103">E-mailbestemming</span><span class="sxs-lookup"><span data-stu-id="68078-103">Email destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68078-104">U kunt een e-mailbestemming configureren voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.</span><span class="sxs-lookup"><span data-stu-id="68078-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="68078-105">Op basis van de doelinstelling wordt een gegenereerd document geleverd als een bijlage van een e-mailbericht.</span><span class="sxs-lookup"><span data-stu-id="68078-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="68078-106">Stel **Ingeschakeld** in op **Ja** om een uitvoerbestand per e-mail te verzenden.</span><span class="sxs-lookup"><span data-stu-id="68078-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="68078-107">Nadat deze optie is ingeschakeld, kunt u de e-mailontvangers opgeven en het onderwerp en de tekst van het e-mailbericht bewerken.</span><span class="sxs-lookup"><span data-stu-id="68078-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="68078-108">U kunt constante teksten voor het onderwerp en de hoofdtekst van het e-mailbericht instellen of u kunt ER-[formules](er-formula-language.md) gebruiken om e-mailteksten dynamisch te maken.</span><span class="sxs-lookup"><span data-stu-id="68078-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="68078-109">U kunt e-mailadressen voor ER op twee manieren configureren.</span><span class="sxs-lookup"><span data-stu-id="68078-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="68078-110">U kunt de configuratie voltooien op dezelfde manier als de afdrukbeheerfunctie of u kunt een e-mailadres oplossen door via een formule direct naar de nieuwe ER-configuratie te verwijzen.</span><span class="sxs-lookup"><span data-stu-id="68078-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="68078-111">[![E-mailbestemming inschakelen](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="68078-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="68078-112">E-mailadrestypen</span><span class="sxs-lookup"><span data-stu-id="68078-112">Email address types</span></span>

<span data-ttu-id="68078-113">Als u **Bewerken** selecteert in het veld **Aan** of **Cc**, wordt het dialoogvenster **E-mail naar** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="68078-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="68078-114">Vervolgens kunt u het type te gebruiken e-mailadres selecteren.</span><span class="sxs-lookup"><span data-stu-id="68078-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="68078-115">De e-mailtypen **Configuratie-e-mail** en **Afdrukbeheer** worden momenteel ondersteund.</span><span class="sxs-lookup"><span data-stu-id="68078-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="68078-116">[![E-mailtype selecteren](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="68078-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="68078-117">Afdrukbeheer</span><span class="sxs-lookup"><span data-stu-id="68078-117">Print management</span></span>

<span data-ttu-id="68078-118">Als u het e-mailtype **Afdrukbeheer** selecteert, kunt u vaste e-mailadressen invoeren in het veld **Aan**.</span><span class="sxs-lookup"><span data-stu-id="68078-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="68078-119">[![Vaste e-mailadressen configureren](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="68078-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="68078-120">Als u niet-vaste e-mailadressen wilt gebruiken, moet u het brontype voor e-mail selecteren voor een bestandsbestemming.</span><span class="sxs-lookup"><span data-stu-id="68078-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="68078-121">De volgende waarden worden ondersteund: **Klant**, **Leverancier**, **Prospect**, **Contact**, **Concurrent**, **Werknemer**, **Sollicitant**, **Potentiële leverancier** en **Niet-toegestane leverancier**.</span><span class="sxs-lookup"><span data-stu-id="68078-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="68078-122">Nadat u een e-mailbrontype hebt geselecteerd, gebruikt u de knop naast het veld **E-mail van bronrekening** om het formulier **Formuleontwerper** te openen.</span><span class="sxs-lookup"><span data-stu-id="68078-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="68078-123">U kunt dit formulier gebruiken om een formule toe te voegen die tijdens runtime de **partijrekening** retourneert van het geselecteerde brontype van het verwerkte document naar de e-mailbestemming.</span><span class="sxs-lookup"><span data-stu-id="68078-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="68078-124">[![E-mailbronaccount configureren](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="68078-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="68078-125">Formules zijn specifiek voor de ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="68078-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="68078-126">Voer in het veld **Formule** een documentspecifieke verwijzing naar een klant- of leverancierspartijtype in.</span><span class="sxs-lookup"><span data-stu-id="68078-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="68078-127">In plaats van te typen kunt u ook het gegevensbronknooppunt zoeken waarmee de klant- of leveranciersrekening wordt voorgesteld. Selecteer vervolgens **Gegevensbron toevoegen** om de formule bij te werken.</span><span class="sxs-lookup"><span data-stu-id="68078-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="68078-128">Als u bijvoorbeeld de configuratie **ISO 20022 Kredietoverdracht** gebruikt, is het knooppunt dat een leveranciersrekening vertegenwoordigt `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="68078-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="68078-129">Als u een tekenreekswaarde invoert, bijvoorbeeld `"DE-001"`, en een formule opslaat, wordt er een e-mail verzonden naar de contactpersoon van de leverancier, **de-001**.</span><span class="sxs-lookup"><span data-stu-id="68078-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="68078-130">[De pagina ![ER-formuleontwerper](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="68078-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="68078-131">[![Kenmerken van e-mailbronaccount configureren](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="68078-131">[![Configure email source attributes account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="68078-132">Configuratie-e-mail</span><span class="sxs-lookup"><span data-stu-id="68078-132">Configuration email</span></span>

<span data-ttu-id="68078-133">Gebruik dit e-mailtype als de configuratie die u gebruikt, een knooppunt heeft in de gegevensbronnen dat een **e-mailadres** retourneert.</span><span class="sxs-lookup"><span data-stu-id="68078-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="68078-134">U kunt gegevensbronnen en functies in de Formuleontwerper gebruiken om een correct opgemaakt e-mailadres te krijgen.</span><span class="sxs-lookup"><span data-stu-id="68078-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="68078-135">Als u bijvoorbeeld de configuratie **ISO 20022 Kredietoverdracht** gebruikt, is het knooppunt dat een e-mailadres van een contactpersoon van een leverancier vertegenwoordigt `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="68078-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="68078-136">[![E-mailadresbron configureren](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="68078-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68078-137">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="68078-137">Additional resources</span></span>

- [<span data-ttu-id="68078-138">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="68078-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="68078-139">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="68078-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="68078-140">Formuleontwerper in elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="68078-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
