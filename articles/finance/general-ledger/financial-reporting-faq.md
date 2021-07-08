---
title: Veelgestelde vragen over Financiële rapportage
description: Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over Financiële rapportage.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266628"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="dcbd4-103">Veelgestelde vragen over Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="dcbd4-103">Financial reporting FAQ</span></span>

<span data-ttu-id="dcbd4-104">Dit onderwerp biedt antwoorden op veelgestelde vragen over Financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="dcbd4-105">Hoe beperk ik de toegang tot een rapport door middel van structuurbeveiliging?</span><span class="sxs-lookup"><span data-stu-id="dcbd4-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="dcbd4-106">In het volgende voorbeeld ziet u hoe u de toegang tot een rapport beperkt met structuurbeveiliging.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="dcbd4-107">Het USMF-demobedrijf heeft een **balansrapport** waartoe niet alle gebruikers van Financiële rapportage toegang moeten krijgen.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="dcbd4-108">U kunt structuurbeveiliging gebruiken om de toegang tot één rapport te beperken, zodat alleen bepaalde gebruikers toegang hebben.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="dcbd4-109">Meld u aan bij Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="dcbd4-110">Selecteer **Bestand \> Nieuw \> Structuurdefinitie** om een nieuwe structuurdefinitie te maken.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="dcbd4-111">Tik of klik twee keer op de regel **Samenvatting** in de kolom **Beveiliging van eenheid**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="dcbd4-112">Klik op **Gebruikers en groepen**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="dcbd4-113">Selecteer de gebruikers of groepen die toegang tot het rapport moeten krijgen.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="dcbd4-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-114">Select **Save**.</span></span>
7. <span data-ttu-id="dcbd4-115">Voeg in de rapportdefinitie uw nieuwe structuurdefinitie toe.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="dcbd4-116">Selecteer **Instelling** in de structuurdefinitie.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="dcbd4-117">Selecteer vervolgens onder **Rapporteringseenheden selecteren** de optie **Alle eenheden opnemen**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="dcbd4-118">Hoe bepaal ik welke rekeningen niet met mijn saldi overeenkomen?</span><span class="sxs-lookup"><span data-stu-id="dcbd4-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="dcbd4-119">Als u een niet-salderend rapport hebt, gebruikt u de volgende procedures om de rekeningen en afwijkingen te identificeren.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="dcbd4-120">In Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="dcbd4-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="dcbd4-121">Maak een nieuwe rijdefinitie.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-121">Create a new row definition.</span></span>
2. <span data-ttu-id="dcbd4-122">Selecteer **Bewerken \> Rijen invoegen uit dimensies**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="dcbd4-123">Selecteer **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="dcbd4-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-124">Select **OK**.</span></span>
5. <span data-ttu-id="dcbd4-125">Sla de rijdefinitie op.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-125">Save the row definition.</span></span>
6. <span data-ttu-id="dcbd4-126">Maak een nieuwe kolomdefinitie.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-126">Create a new column definition.</span></span>
7. <span data-ttu-id="dcbd4-127">Maak een nieuwe rapportdefinitie.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-127">Create a new report definition.</span></span>
8. <span data-ttu-id="dcbd4-128">Selecteer **Instellingen** en schakel deze optie uit.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="dcbd4-129">Genereer het rapport.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-129">Generate the report.</span></span> 
10. <span data-ttu-id="dcbd4-130">Exporteer het rapport naar Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="dcbd4-131">In Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="dcbd4-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="dcbd4-132">Ga naar **Grootboek \> Query's en rapporten \> Proefbalans**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="dcbd4-133">Stel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="dcbd4-133">Set the following fields:</span></span>

    - <span data-ttu-id="dcbd4-134">**Begindatum**: voer het begindatum van het fiscale jaar in.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="dcbd4-135">**Einddatum**: voer de datum in waarvoor u het rapport genereert.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="dcbd4-136">**Financiële dimensie**: stel dit veld in op **Hoofdrekening ingesteld**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="dcbd4-137">Selecteer **Berekenen**.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="dcbd4-138">Exporteer het rapport naar Excel.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-138">Export the report to Excel.</span></span>

<span data-ttu-id="dcbd4-139">U kunt de gegevens nu uit het Excel-rapport in Financial Reporter kopiëren naar het **proefbalansrapport** zodat u de kolommen **Eindsaldo** kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="dcbd4-140">Als ik een rapport ontwerp in Report Designer of tijdens het genereren van een financieel rapport, zie ik het volgende bericht: "De bewerking kan niet worden voltooid vanwege een probleem in het gegevensproviderraamwerk."</span><span class="sxs-lookup"><span data-stu-id="dcbd4-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="dcbd4-141">Hoe moet ik reageren?</span><span class="sxs-lookup"><span data-stu-id="dcbd4-141">How should I respond?</span></span>

<span data-ttu-id="dcbd4-142">Het bericht geeft aan dat er een probleem is opgetreden op het moment dat het systeem heeft geprobeerd om financiële metagegevens op te halen uit de datamart terwijl u Financiële rapportage gebruikte.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="dcbd4-143">U kunt op twee manieren op dit probleem reageren:</span><span class="sxs-lookup"><span data-stu-id="dcbd4-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="dcbd4-144">Controleer de integratiestatus van de gegevens met **Hulpmiddelen \> Integratiestatus** in Report Designer.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="dcbd4-145">Als de integratie onvolledig is, moet u wachten tot deze is voltooid.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="dcbd4-146">Probeer vervolgens dezelfde actie opnieuw uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="dcbd4-147">Neem contact op met Ondersteuning om het probleem vast te stellen en op te lossen.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="dcbd4-148">Het systeem kan inconsistente gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="dcbd4-149">Ondersteuningsmedewerkers kunnen u helpen om dat probleem op de server te vinden en de specifieke gegevens te bepalen waarvoor een update nodig is.</span><span class="sxs-lookup"><span data-stu-id="dcbd4-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
