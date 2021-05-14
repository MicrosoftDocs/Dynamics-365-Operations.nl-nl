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
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923020"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="0321c-103">Veelgestelde vragen over financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="0321c-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="0321c-104">Dit onderwerp biedt antwoorden op veelgestelde vragen over financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="0321c-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="0321c-105">Hoe beperk ik de toegang tot een rapport met structuurbeveiliging?</span><span class="sxs-lookup"><span data-stu-id="0321c-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="0321c-106">In het volgende voorbeeld ziet u hoe u de toegang tot een rapport beperkt in de structuurbeveiliging.</span><span class="sxs-lookup"><span data-stu-id="0321c-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="0321c-107">Het USMF-demobedrijf heeft een balansrapport waartoe niet alle gebruikers van Financiële rapportage toegang moeten krijgen.</span><span class="sxs-lookup"><span data-stu-id="0321c-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="0321c-108">Als u de toegang wilt beperken, kunt u structuurbeveiliging gebruiken om de toegang tot één rapport te beperken, zodat alleen bepaalde gebruikers toegang hebben tot het rapport.</span><span class="sxs-lookup"><span data-stu-id="0321c-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="0321c-109">Volg deze stappen om de toegang te beperken:</span><span class="sxs-lookup"><span data-stu-id="0321c-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="0321c-110">Meld u aan bij Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="0321c-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="0321c-111">Maak een nieuwe structuurdefinitie.</span><span class="sxs-lookup"><span data-stu-id="0321c-111">Create a new tree definition.</span></span> <span data-ttu-id="0321c-112">Ga naar **Bestand > Nieuw > Structuurdefinitie**.</span><span class="sxs-lookup"><span data-stu-id="0321c-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="0321c-113">Dubbelklik op de regel **Samenvatting** in de kolom **Beveiliging van eenheid**.</span><span class="sxs-lookup"><span data-stu-id="0321c-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="0321c-114">Klik op **Gebruikers en groepen**.</span><span class="sxs-lookup"><span data-stu-id="0321c-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="0321c-115">Selecteer de gebruikers of groepen die toegang tot dit rapport moeten hebben.</span><span class="sxs-lookup"><span data-stu-id="0321c-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="0321c-116">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0321c-116">Select **Save**.</span></span>
7. <span data-ttu-id="0321c-117">Voeg in de rapportdefinitie uw nieuwe structuurdefinitie toe.</span><span class="sxs-lookup"><span data-stu-id="0321c-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="0321c-118">Selecteer **Instelling** in de structuurdefinitie.</span><span class="sxs-lookup"><span data-stu-id="0321c-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="0321c-119">Selecteer onder **Rapporteringseenheden selecteren** de optie **Alle eenheden opnemen**.</span><span class="sxs-lookup"><span data-stu-id="0321c-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="0321c-120">Hoe bepaal ik welke rekeningen niet met mijn saldi overeenkomen?</span><span class="sxs-lookup"><span data-stu-id="0321c-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="0321c-121">Als u een niet-salderend rapport hebt, kunt u het volgende doen om die rekeningen en afwijkingen te identificeren.</span><span class="sxs-lookup"><span data-stu-id="0321c-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="0321c-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="0321c-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="0321c-123">Maak een nieuwe rijdefinitie in Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="0321c-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="0321c-124">Selecteer **Bewerken > Rijen invoegen uit dimensies**.</span><span class="sxs-lookup"><span data-stu-id="0321c-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="0321c-125">Selecteer **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="0321c-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="0321c-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0321c-126">Select **OK**.</span></span>
5. <span data-ttu-id="0321c-127">Sla de rijdefinitie op.</span><span class="sxs-lookup"><span data-stu-id="0321c-127">Save the row definition.</span></span>
6. <span data-ttu-id="0321c-128">Een nieuwe kolomdefinitie maken</span><span class="sxs-lookup"><span data-stu-id="0321c-128">Create a new column definition</span></span>
7. <span data-ttu-id="0321c-129">Maak een nieuwe rapportdefinitie.</span><span class="sxs-lookup"><span data-stu-id="0321c-129">Create a new report definition.</span></span>
8. <span data-ttu-id="0321c-130">Selecteer **Instellingen** en schakel deze optie uit.</span><span class="sxs-lookup"><span data-stu-id="0321c-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="0321c-131">Genereer het rapport.</span><span class="sxs-lookup"><span data-stu-id="0321c-131">Generate the report.</span></span> 
10. <span data-ttu-id="0321c-132">Exporteer het rapport naar Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0321c-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="0321c-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="0321c-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="0321c-134">Ga in Dynamics 365 Finance naar **Grootboek > Query's en rapporten > Proefbalans**.</span><span class="sxs-lookup"><span data-stu-id="0321c-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="0321c-135">Stel de volgende parameters in:</span><span class="sxs-lookup"><span data-stu-id="0321c-135">Set the following parameters:</span></span>
   - <span data-ttu-id="0321c-136">**Begindatum**: voer het begin van het boekjaar in.</span><span class="sxs-lookup"><span data-stu-id="0321c-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="0321c-137">**Einddatum**: voer de datum in waarvoor u het rapport genereert.</span><span class="sxs-lookup"><span data-stu-id="0321c-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="0321c-138">**Financiële dimensie**: stel dit veld in op **Hoofdrekening ingesteld**.</span><span class="sxs-lookup"><span data-stu-id="0321c-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="0321c-139">Selecteer **Berekenen**.</span><span class="sxs-lookup"><span data-stu-id="0321c-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="0321c-140">Exporteer het rapport naar Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0321c-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="0321c-141">U kunt de gegevens nu uit het Excel-rapport in Financial Reporter kopiëren naar het proefbalansrapport zodat u de kolommen **Eindsaldo** kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="0321c-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]