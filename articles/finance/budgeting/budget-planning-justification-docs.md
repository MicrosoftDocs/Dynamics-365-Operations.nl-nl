---
title: Verantwoordingsdocumenten voor budgetplanning
description: Verantwoordingsdocumenten bieden een beschrijving voor degenen die een budget aanvragen en willen uitleggen waarom een specifiek budget nodig is.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 321da6643b421070ddd9f32bddd3e8d72f0adb86
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188551"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="6cd9d-103">Verantwoordingsdocumenten voor budgetplanning</span><span class="sxs-lookup"><span data-stu-id="6cd9d-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cd9d-104">Verantwoordingsdocumenten bieden een beschrijving voor degenen die een budget aanvragen en willen uitleggen waarom een specifiek budget nodig is.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="6cd9d-105">Een budgetplansjabloon wordt gemaakt door de budgetmanager in Microsoft Word en toegewezen aan het huidige budgetplanningsproces.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="6cd9d-106">Budgeteigenaren kunnen de sjabloon vervolgens openen en gegevens automatisch in Word laten invullen op basis van hun budgetaanvraag.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="6cd9d-107">Vervolgens kunnen ze extra tekst of gegevens toevoegen voordat hun gepersonaliseerde verantwoordingsdocument wordt opgeslagen en gekoppeld aan hun budgetplan.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="6cd9d-108">Instellen van Microsoft Dynamics Office-invoegtoepassing voor Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="6cd9d-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="6cd9d-109">Een nieuw Microsoft Word-document openen.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="6cd9d-110">Klik op **Invoegen** in het lint en klik vervolgens op **Opslag**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="6cd9d-111">Zoek naar Microsoft Dynamics Office-invoegtoepassing en klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="6cd9d-112">Klik in Word in het rechterdeelvenster op **Servergegevens toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="6cd9d-113">Typ of plak de URL van de server en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="6cd9d-114">De Redensjabloon definiëren in Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="6cd9d-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="6cd9d-115">Klik op **Ontwerp** in de Microsoft Dynamics Office-invoegtoepassing nadat u zich hebt aangemeld.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="6cd9d-116">Gebruik voor koptekstgegevens de knop **Velden toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="6cd9d-117">Selecteer de gegevensbron voor de entiteit BudgetPlanJustification en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="6cd9d-118">**Opmerking:** deze entiteit is vereist voor elk verantwoordingsdocument.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="6cd9d-119">Andere entiteiten kunnen worden gebruikt, maar weer uploaden naar Microsoft Dynamics 365 Finance is niet mogelijk als deze entiteit niet is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-119">Other entities can be used but the upload back to Microsoft Dynamics 365 Finance will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="6cd9d-120">Voeg de labels en waarden BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter en DocumentNumber in het Word-document toe.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="6cd9d-121">**Opmerking:** u kunt desgewenst uw eigen aangepaste labels gebruiken in plaats van de standaardlabels.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="6cd9d-122">Klik op **Gereed** om de koptekstsectie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="6cd9d-123">Klik voor regelniveaudetails van budgetplanbedragen op **Tabel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="6cd9d-124">Selecteer de gegevensbron voor de entiteit van BudgetPlanJustification opnieuw en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="6cd9d-125">Voeg velden voor EffectiveDate, ScenarioName, AccountDisplayValue en AccountingCurrencyExpenseAmount toe.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="6cd9d-126">**Opmerking:** als er opmerkingen beschikbaar zijn om toe te voegen in afzonderlijke budgetplanregels, kunnen deze hier aan de tabel worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="6cd9d-127">Voeg eventuele aanvullende instructies voor de eindgebruiker toe en pas indien nodig opmaak of stijlen op het document toe.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="6cd9d-128">Sla het document op uw lokale computer op en sluit het bestand voordat u doorgaat.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="6cd9d-129">Het budgetplanningsproces instellen voor gebruik van de sjabloon Reden</span><span class="sxs-lookup"><span data-stu-id="6cd9d-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="6cd9d-130">Ga naar **Budgettering** &gt; **Instellen** &gt; **Budgetplanning** &gt; **Verantwoordingsdocumentsjablonen**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-130">Go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="6cd9d-131">Klik op **Nieuw** en blader naar het nieuwe Microsoft Word-document.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="6cd9d-132">Voer een naam en beschrijving voor de sjabloonweergave in.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-132">Enter a template display name and description.</span></span> <span data-ttu-id="6cd9d-133">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-133">Click **OK**.</span></span>
4.  <span data-ttu-id="6cd9d-134">Ga naar **Budgettering** &gt; **Instellen** &gt; **Budget** **planning** &gt; **Budgetplanningsproces**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="6cd9d-135">Selecteer het proces waarin de redensjabloon moet worden gebruikt en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="6cd9d-136">Selecteer in het veld **Verantwoordingsdocumentsjabloon** de juiste sjabloon en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="6cd9d-137">Persoonlijke redendocumenten bewerken en opslaan</span><span class="sxs-lookup"><span data-stu-id="6cd9d-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="6cd9d-138">Maak een nieuw budgetplan of open een bestaand budgetplan.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-138">Create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="6cd9d-139">Selecteer in het vervolgkeuzemenu **Reden** **Nieuwe verantwoording maken**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="6cd9d-140">Geef na het invullen van de details aan dat u het aangepaste document wilt uploaden in het vervolgkeuzemenu **Reden**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>



