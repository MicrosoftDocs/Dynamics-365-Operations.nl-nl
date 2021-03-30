---
title: Het voorspellingsmodel verbeteren (preview)
description: In dit onderwerp worden de functies beschreven die u kunt gebruiken om de prestaties van voorspellingsmodellen te verbeteren.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1028af6e702f2118fabcbc71b17daca36072c691
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208455"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="7527e-103">Het voorspellingsmodel verbeteren (preview)</span><span class="sxs-lookup"><span data-stu-id="7527e-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7527e-104">In dit onderwerp worden de functies beschreven die u kunt gebruiken om de prestaties van voorspellingsmodellen te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="7527e-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="7527e-105">U begint uw model te verbeteren in het werkgebied **Voorspellingen voor klantbetalingen** in Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7527e-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="7527e-106">De stappen voor verbetering worden vervolgens uitgevoerd in de AI Builder.</span><span class="sxs-lookup"><span data-stu-id="7527e-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="7527e-107">Historische resultaten selecteren</span><span class="sxs-lookup"><span data-stu-id="7527e-107">Select historical outcomes</span></span>

<span data-ttu-id="7527e-108">U selecteert eerst een of meer van de drie mogelijke resultaten voor facturen: **op tijd**, **te laat** en **zeer laat**.</span><span class="sxs-lookup"><span data-stu-id="7527e-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="7527e-109">Alle drie de resultaten moeten worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="7527e-109">All three outcomes should be selected.</span></span> <span data-ttu-id="7527e-110">Als u de selectie van een van de resultaten wist, worden facturen uit het trainingsproces gefilterd en wordt de nauwkeurigheid van de voorspelling verlaagd.</span><span class="sxs-lookup"><span data-stu-id="7527e-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="7527e-111">[![Resultaten bevestigen](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="7527e-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="7527e-112">Als uw organisatie slechts twee resultaten nodig heeft, wijzigt u de drempels **te laat** en **zeer laat** in 0 (nul) dagen.</span><span class="sxs-lookup"><span data-stu-id="7527e-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="7527e-113">Op deze manier vouwt u de voorspelling samen tot een binaire status **op tijd** of **te laat**.</span><span class="sxs-lookup"><span data-stu-id="7527e-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="7527e-114">Velden selecteren</span><span class="sxs-lookup"><span data-stu-id="7527e-114">Select fields</span></span>

<span data-ttu-id="7527e-115">Wanneer u velden selecteert die u in het model wilt opnemen, moet u er rekening mee houden dat de lijst alle beschikbare velden bevat in de Microsoft Dataverse-tabel die is toegewezen aan de gegevens in de Azure data lake.</span><span class="sxs-lookup"><span data-stu-id="7527e-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="7527e-116">Sommige van deze velden mogen **niet** zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="7527e-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="7527e-117">De velden die niet mogen worden geselecteerd, vallen in een van de volgende drie categorieën:</span><span class="sxs-lookup"><span data-stu-id="7527e-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="7527e-118">Het veld is vereist voor de Dataverse-tabel, maar er zijn geen gegevens voor in de data lake.</span><span class="sxs-lookup"><span data-stu-id="7527e-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="7527e-119">Het veld is een ID en is daarom niet zinvol voor een machine learning-functie.</span><span class="sxs-lookup"><span data-stu-id="7527e-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="7527e-120">Het veld bevat informatie die niet beschikbaar is tijdens de voorspelling.</span><span class="sxs-lookup"><span data-stu-id="7527e-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="7527e-121">In de volgende secties worden de velden weergegeven die beschikbaar zijn voor de factuur- en klantentiteiten, en worden de velden weergegeven die **niet** voor de training moeten worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="7527e-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="7527e-122">De categorie die voor elk van deze velden is opgegeven, verwijst naar de categorieën in de voorgaande lijst.</span><span class="sxs-lookup"><span data-stu-id="7527e-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="7527e-123">Dataverse-tabel Factuur</span><span class="sxs-lookup"><span data-stu-id="7527e-123">Invoice Dataverse table</span></span>

<span data-ttu-id="7527e-124">In de volgende afbeelding ziet u de velden die beschikbaar zijn voor de tabel Factuur.</span><span class="sxs-lookup"><span data-stu-id="7527e-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="7527e-125">[![Beschikbare velden voor de tabel Factuur](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="7527e-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="7527e-126">De volgende velden moeten niet zijn geselecteerd voor training:</span><span class="sxs-lookup"><span data-stu-id="7527e-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="7527e-127">**Factuurrekening** (categorie 2)</span><span class="sxs-lookup"><span data-stu-id="7527e-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="7527e-128">**Is gesloten** (categorie 3): dit veld wordt gebruikt om facturen te filteren voor training (gesloten) en voorspelling (niet afgesloten).</span><span class="sxs-lookup"><span data-stu-id="7527e-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="7527e-129">**Naam** (categorie 1)</span><span class="sxs-lookup"><span data-stu-id="7527e-129">**Name** (category 1)</span></span>
- <span data-ttu-id="7527e-130">**Bron-ID** (categorie 2)</span><span class="sxs-lookup"><span data-stu-id="7527e-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="7527e-131">**Bronrecord** (categorie 2)</span><span class="sxs-lookup"><span data-stu-id="7527e-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="7527e-132">**Brontabel** (categorie 2)</span><span class="sxs-lookup"><span data-stu-id="7527e-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="7527e-133">Dataverse-tabel Klant</span><span class="sxs-lookup"><span data-stu-id="7527e-133">Customer Dataverse table</span></span>

<span data-ttu-id="7527e-134">In de volgende afbeelding ziet u de velden die beschikbaar zijn voor de tabel Klant.</span><span class="sxs-lookup"><span data-stu-id="7527e-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="7527e-135">[![Beschikbare velden voor de tabel Klant](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="7527e-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="7527e-136">Het volgende veld moet niet zijn geselecteerd voor training:</span><span class="sxs-lookup"><span data-stu-id="7527e-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="7527e-137">**Unieke sleutel rij** (categorie 2)</span><span class="sxs-lookup"><span data-stu-id="7527e-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="7527e-138">Filters</span><span class="sxs-lookup"><span data-stu-id="7527e-138">Filters</span></span>

<span data-ttu-id="7527e-139">De filters ondersteunen momenteel het voorspellingsscenario voor klantbetalingen niet.</span><span class="sxs-lookup"><span data-stu-id="7527e-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="7527e-140">Selecteer daarom **Deze stap overslaan** en ga naar de overzichtspagina.</span><span class="sxs-lookup"><span data-stu-id="7527e-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="7527e-141">[![Focusmodel met filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="7527e-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="7527e-142">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="7527e-142">Privacy notice</span></span>
<span data-ttu-id="7527e-143">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="7527e-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]