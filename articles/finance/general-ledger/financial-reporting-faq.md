---
title: Veelgestelde vragen over financiële rapportage
description: In dit onderwerp vindt u antwoorden op eerdere vragen van andere gebruikers over financiële rapportage.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811301"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="bd2e2-103">Veelgestelde vragen over financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="bd2e2-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="bd2e2-104">In dit onderwerp vindt u antwoorden op eerdere vragen van andere gebruikers over financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="bd2e2-105">Hoe beperk ik de toegang tot een rapport met Structuurbeveiliging?</span><span class="sxs-lookup"><span data-stu-id="bd2e2-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="bd2e2-106">Scenario: Het demobedrijf USMF wil de toegang tot een balansrapport beperken om te voorkomen dat alle gebruikers van functies voor financiële rapportage het rapport in D365 kunnen weergeven.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="bd2e2-107">Oplossing: U kunt Structuurbeveiliging gebruiken om de toegang tot één rapport te beperken, zodat alleen bepaalde gebruikers toegang hebben tot het rapport.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="bd2e2-108">Meld u aan bij Report Designer voor financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="bd2e2-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="bd2e2-109">Maak een nieuwe structuurdefinitie (Bestand | Nieuw | Structuurdefinitie) a.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="bd2e2-110">Dubbelklik op de regel **Samenvatting** in de kolom **Beveiliging van eenheid**.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="bd2e2-111">i.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-111">i.</span></span>    <span data-ttu-id="bd2e2-112">Klik op Gebruikers en groepen.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="bd2e2-113">1. Selecteer de gebruiker(s) of groep die toegang tot dit rapport wil(len) hebben.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="bd2e2-114">[![Gebruikersscherm](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="bd2e2-115">[![Beveiligingsscherm](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="bd2e2-116">b.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-116">b.</span></span>    <span data-ttu-id="bd2e2-117">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-117">Click **Save**.</span></span>
  
<span data-ttu-id="bd2e2-118">[![De knop Opslaan](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="bd2e2-119">Voeg in uw rapportdefinitie uw nieuwe structuurdefinitie toe</span><span class="sxs-lookup"><span data-stu-id="bd2e2-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="bd2e2-120">[![Formulier voor structuurdefinitie](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="bd2e2-121">A.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-121">A.</span></span>  <span data-ttu-id="bd2e2-122">Klik in de structuurdefinitie op Instellingen en schakel onder Rapporteringseenheden selecteren het selectievakje Alle rapporteringseenheden opnemen in</span><span class="sxs-lookup"><span data-stu-id="bd2e2-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="bd2e2-123">[![Formulier voor selectie van rapporteringseenheden](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="bd2e2-124">**Voor:** [![Schermopname van Voor](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="bd2e2-125">**Na:** [![Schermopname van Na](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="bd2e2-126">Opmerking: de reden voor het bovenstaande bericht is dat de gebruiker geen toegang heeft tot dat rapport nadat Beveiliging van eenheid is toegepast</span><span class="sxs-lookup"><span data-stu-id="bd2e2-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="bd2e2-127">Hoe bepaal ik welke rekeningen niet overeenkomen met mijn saldi in D365?</span><span class="sxs-lookup"><span data-stu-id="bd2e2-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="bd2e2-128">Wanneer u een rapport hebt dat niet overeenkomt met uw verwachtingen in D365, kunt u het volgende doen om die rekeningen en de afwijkingen te identificeren.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="bd2e2-129">In Report Designer voor financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="bd2e2-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="bd2e2-130">Maak een nieuwe rijdefinitie a.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="bd2e2-131">Klik op Bewerken | Rijen invoegen uit dimensies i.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="bd2e2-132">Selecteer MainAccount [![Scherm voor selectie van MainAccount](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="bd2e2-133">ii.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-133">ii.</span></span> <span data-ttu-id="bd2e2-134">Klik op Ok b.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-134">Click Ok b.</span></span>    <span data-ttu-id="bd2e2-135">Sla de rijdefinitie op</span><span class="sxs-lookup"><span data-stu-id="bd2e2-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="bd2e2-136">Maak een nieuwe kolomdefinitie     [![Een nieuwe kolomdefinitie maken](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="bd2e2-137">Maak een nieuwe rapportdefinitie a.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="bd2e2-138">Klik op instellingen en schakel de gemarkeerde selectievakjes uit [![Formulier Instellingen](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="bd2e2-139">Genereer het rapport.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="bd2e2-140">Exporteer het rapport naar Excel.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="bd2e2-141">In D365:</span><span class="sxs-lookup"><span data-stu-id="bd2e2-141">In D365:</span></span> 
1.  <span data-ttu-id="bd2e2-142">Klik op Grootboek | Query's en rapporten | Proefbalans a.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="bd2e2-143">Parameters i.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-143">Parameters i.</span></span>  <span data-ttu-id="bd2e2-144">Begindatum: Begin van boekjaar ii.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="bd2e2-145">Einddatum: de datum waarvoor u het rapport hebt gegenereerd iii.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="bd2e2-146">Financiële-dimensieset ingesteld op Hoofdrekening ingesteld [![Formulier Hoofdrekening](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="bd2e2-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="bd2e2-147">b.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-147">b.</span></span>    <span data-ttu-id="bd2e2-148">Klik op Berekenen</span><span class="sxs-lookup"><span data-stu-id="bd2e2-148">Click Calculate</span></span>

2.  <span data-ttu-id="bd2e2-149">Exporteer het rapport naar Excel</span><span class="sxs-lookup"><span data-stu-id="bd2e2-149">Export the report to Excel</span></span>

<span data-ttu-id="bd2e2-150">U kunt de gegevens nu kopiëren uit het Excel-rapport in FR en het D365-proefbalansrapport om de kolommen Eindsaldo te vergelijken.</span><span class="sxs-lookup"><span data-stu-id="bd2e2-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]