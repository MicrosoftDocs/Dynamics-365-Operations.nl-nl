---
title: Verantwoordingsdocumenten voor budgetplanning
description: Verantwoordingsdocumenten bieden een beschrijving voor degenen die een budget aanvragen en willen uitleggen waarom een specifiek budget nodig is.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: eb616d6802e32d9dcbbeaf9c9866491c8a8d59c8
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="421e4-103">Verantwoordingsdocumenten voor budgetplanning</span><span class="sxs-lookup"><span data-stu-id="421e4-103">Budget planning justification documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="421e4-104">Verantwoordingsdocumenten bieden een beschrijving voor degenen die een budget aanvragen en willen uitleggen waarom een specifiek budget nodig is.</span><span class="sxs-lookup"><span data-stu-id="421e4-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="421e4-105">Een budgetplansjabloon wordt gemaakt door de budgetmanager in Microsoft Word en toegewezen aan het huidige budgetplanningsproces.</span><span class="sxs-lookup"><span data-stu-id="421e4-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="421e4-106">Budgeteigenaren kunnen de sjabloon vervolgens openen en gegevens automatisch in Word laten invullen op basis van hun budgetaanvraag.</span><span class="sxs-lookup"><span data-stu-id="421e4-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="421e4-107">Vervolgens kunnen ze extra tekst of gegevens toevoegen voordat hun gepersonaliseerde verantwoordingsdocument wordt opgeslagen en gekoppeld aan hun budgetplan.</span><span class="sxs-lookup"><span data-stu-id="421e4-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="421e4-108">Microsoft Dynamics Office-invoegtoepassing instellen voor Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="421e4-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="421e4-109">Open een nieuw Microsoft Word-document.</span><span class="sxs-lookup"><span data-stu-id="421e4-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="421e4-110">Klik op **Invoegen** in het lint en klik vervolgens op **Opslag**.</span><span class="sxs-lookup"><span data-stu-id="421e4-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="421e4-111">Zoek naar Microsoft Dynamics Office-invoegtoepassing en klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="421e4-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="421e4-112">Klik in Word in het rechterdeelvenster op **Servergegevens toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="421e4-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="421e4-113">Typ of plak de URL van de server en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="421e4-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="421e4-114">De sjabloon Reden definiëren in Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="421e4-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="421e4-115">Klik op **Ontwerp** in de Microsoft Dynamics Office-invoegtoepassing nadat u zich hebt aangemeld.</span><span class="sxs-lookup"><span data-stu-id="421e4-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="421e4-116">Gebruik voor koptekstgegevens de knop **Velden toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="421e4-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="421e4-117">Selecteer de gegevensbron voor de entiteit BudgetPlanJustification en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="421e4-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="421e4-118">**Opmerking:** deze entiteit is vereist voor elk verantwoordingsdocument.</span><span class="sxs-lookup"><span data-stu-id="421e4-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="421e4-119">Andere entiteiten kunnen worden gebruikt, maar weer uploaden naar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition is niet mogelijk als deze entiteit niet is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="421e4-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="421e4-120">Voeg de labels en waarden BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter en DocumentNumber in het Word-document toe.</span><span class="sxs-lookup"><span data-stu-id="421e4-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="421e4-121">**Opmerking:** u kunt desgewenst uw eigen aangepaste labels gebruiken in plaats van de standaardlabels.</span><span class="sxs-lookup"><span data-stu-id="421e4-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="421e4-122">Klik op **Gereed** om de koptekstsectie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="421e4-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="421e4-123">Klik voor regelniveaudetails van budgetplanbedragen op **Tabel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="421e4-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="421e4-124">Selecteer de gegevensbron voor de entiteit van BudgetPlanJustification opnieuw en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="421e4-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="421e4-125">Voeg velden voor EffectiveDate, ScenarioName, AccountDisplayValue en AccountingCurrencyExpenseAmount toe.</span><span class="sxs-lookup"><span data-stu-id="421e4-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="421e4-126">**Opmerking:** als er opmerkingen beschikbaar zijn om toe te voegen in afzonderlijke budgetplanregels, kunnen deze hier aan de tabel worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="421e4-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="421e4-127">Voeg eventuele aanvullende instructies voor de eindgebruiker toe en pas indien nodig opmaak of stijlen op het document toe.</span><span class="sxs-lookup"><span data-stu-id="421e4-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="421e4-128">Sla het document op uw lokale computer op en sluit het bestand voordat u doorgaat.</span><span class="sxs-lookup"><span data-stu-id="421e4-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="421e4-129">Het budgetplanningsproces instellen voor gebruik van de sjabloon Reden</span><span class="sxs-lookup"><span data-stu-id="421e4-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="421e4-130">Ga in Finance and Operations naar **Budgettering** &gt; **Instellen** &gt; **Budgetplanning** &gt; **Verantwoordingsdocumentsjablonen**.</span><span class="sxs-lookup"><span data-stu-id="421e4-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="421e4-131">Klik op **Nieuw** en blader naar het nieuwe Microsoft Word-document.</span><span class="sxs-lookup"><span data-stu-id="421e4-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="421e4-132">Voer een naam en beschrijving voor de sjabloonweergave in.</span><span class="sxs-lookup"><span data-stu-id="421e4-132">Enter a template display name and description.</span></span> <span data-ttu-id="421e4-133">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="421e4-133">Click **OK**.</span></span>
4.  <span data-ttu-id="421e4-134">Ga naar **Budgettering** &gt; **Instellen** &gt; **Budget****planning** &gt; **Budgetplanningsproces**.</span><span class="sxs-lookup"><span data-stu-id="421e4-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="421e4-135">Selecteer het proces waarin de redensjabloon moet worden gebruikt en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="421e4-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="421e4-136">Selecteer in het veld **Verantwoordingsdocumentsjabloon** de juiste sjabloon en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="421e4-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="421e4-137">Persoonlijke redendocumenten bewerken en opslaan</span><span class="sxs-lookup"><span data-stu-id="421e4-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="421e4-138">Maak in Finance and Operations een nieuw budgetplan of open een bestaand budgetplan.</span><span class="sxs-lookup"><span data-stu-id="421e4-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="421e4-139">Selecteer in het vervolgkeuzemenu **Reden** **Nieuwe verantwoording maken**.</span><span class="sxs-lookup"><span data-stu-id="421e4-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="421e4-140">Geef na het invullen van de details aan dat u het aangepaste document wilt uploaden in het vervolgkeuzemenu **Reden**.</span><span class="sxs-lookup"><span data-stu-id="421e4-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





