---
title: Verbruik registreren
description: In dit onderwerp wordt uitgelegd hoe u verbruik registreert in Activabeheer.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f38b01d94fd2efcce5de210f77124fdc24be6e39
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837892"
---
# <a name="register-consumption"></a><span data-ttu-id="13ba0-103">Verbruik registreren</span><span class="sxs-lookup"><span data-stu-id="13ba0-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="13ba0-104">Wanneer een onderhoudstaak voor een werkorder is voltooid, is de volgende stap het maken van verbruiksregistraties en het boeken van de journalen.</span><span class="sxs-lookup"><span data-stu-id="13ba0-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="13ba0-105">U kunt registraties maken voor de volgende verbruikstypen: uren, artikelen en onkosten.</span><span class="sxs-lookup"><span data-stu-id="13ba0-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="13ba0-106">De verschillende verbruikstypen worden geregistreerd en geboekt op de pagina **Werkorderjournalen**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="13ba0-107">De journaalinstellingen in **Activabeheer** worden gebruikt voor het maken en boeken van afzonderlijke journalen voor uren, artikelen en onkosten in de module **Projectbeheer en boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="13ba0-108">In sommige gevallen kunt u prognoseregels toevoegen aan of verwijderen uit een werkorder.</span><span class="sxs-lookup"><span data-stu-id="13ba0-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="13ba0-109">De instelling van een levenscyclusstatus, het gerelateerde project type en de faseregels die betrekking hebben op het projecttype bepalen of u journaalregels kunt toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="13ba0-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="13ba0-110">Zie [Prognoses, werkorders en projecten](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md) voor meer informatie over levenscyclusstatussen van werkorders en gerelateerde projectfasen.</span><span class="sxs-lookup"><span data-stu-id="13ba0-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="13ba0-111">U kunt het automatisch boeken van journalen instellen in de levenscyclusstatus van werkorders.</span><span class="sxs-lookup"><span data-stu-id="13ba0-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="13ba0-112">Zie [Levenscyclusstatussen van werkorder](../setup-for-work-orders/work-order-lifecycle-states.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="13ba0-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="13ba0-113">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="13ba0-114">Selecteer de werkorder en klik op **Journalen**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="13ba0-115">Klik op **Kopiëren van prognose** om prognoseregels over te boeken die mogelijk met de werkorder zijn verbonden.</span><span class="sxs-lookup"><span data-stu-id="13ba0-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="13ba0-116">U kunt selecteren welke verbruikstypen u wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="13ba0-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="13ba0-117">U kunt zo nodig meer verbruiksregels toevoegen op het relevante sneltabblad door op **Regel toevoegen** te klikken en gegevens op de regel in te vullen.</span><span class="sxs-lookup"><span data-stu-id="13ba0-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="13ba0-118">Klik op **Journalen valideren** om de journaalregels te valideren voordat deze worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="13ba0-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="13ba0-119">Klik op **Journalen boeken** om de journaalregels te boeken.</span><span class="sxs-lookup"><span data-stu-id="13ba0-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="13ba0-120">Nadat u de verbruiksjournalen hebt geboekt, kunt u de levenscyclusstatus van de werkorder bijwerken.</span><span class="sxs-lookup"><span data-stu-id="13ba0-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="13ba0-121">Als u bijvoorbeeld wilt aangeven dat de werkorder is voltooid, kunt u de levenscyclusstatus wijzigen in 'Beëindigd'.</span><span class="sxs-lookup"><span data-stu-id="13ba0-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="13ba0-122">Selecteer in het veld **Weergeven** bovenaan de pagina **Werkorderjournalen** de journaalregels die u wilt zien: **Alle**, **Niet geboekt** of **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="13ba0-123">Voor geboekte journalen is het selectievakje **Geboekt** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="13ba0-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="13ba0-124">Wanneer er artikelregels worden gemaakt in het werkorderjournaal, worden productdimensies en traceringsdimensies die betrekking hebben op het artikel automatisch overgenomen op de journaalregel.</span><span class="sxs-lookup"><span data-stu-id="13ba0-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="13ba0-125">In de volgende schermafbeelding ziet u een voorbeeld van uren- en artikelregistraties in een werkorder in **Werkorderjournalen**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Figuur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="13ba0-127">Uren splitsen in werkorders met meerdere werkordertaken</span><span class="sxs-lookup"><span data-stu-id="13ba0-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="13ba0-128">Als een werkorder verschillende werkordertaken bevat, kunt u openingstijden registreren met de functie **Uren splitsen**, wat betekent dat één uurregistratieregel gelijkmatig kan worden verdeeld over alle werkordertaken.</span><span class="sxs-lookup"><span data-stu-id="13ba0-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="13ba0-129">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="13ba0-130">Selecteer de werkorder en klik op **Journalen**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="13ba0-131">Selecteer de uurregistratieregel die u wilt splitsen en klik op **Uren splitsen**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="13ba0-132">In het dialoog venster **Gesplitste uren voor onderhoudstaken voor werkorders** wordt de naam van de medewerker die is aangemeld automatisch weergegeven in het veld **Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="13ba0-133">Selecteer desgewenst een andere medewerker.</span><span class="sxs-lookup"><span data-stu-id="13ba0-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="13ba0-134">Selecteer een categorie voor de uurregistratie in het veld **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="13ba0-135">Voeg in het veld **Uren** het aantal werkuren in dat moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="13ba0-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Figuur 2](media/02-consumption.png)

7. <span data-ttu-id="13ba0-137">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="13ba0-137">Click **OK**.</span></span>

<span data-ttu-id="13ba0-138">*Voorbeeld*: in de onderstaande schermafbeelding worden journaalregels voor een werkorder met drie werkordertaken weergegeven.</span><span class="sxs-lookup"><span data-stu-id="13ba0-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="13ba0-139">De eerste regel, met drie werkuren, is gesplitst en één uur wordt geregistreerd voor elke werkordertaak.</span><span class="sxs-lookup"><span data-stu-id="13ba0-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="13ba0-140">Nadat de drie uurregistratieregels zijn gemaakt, beslist u wat u met de oorspronkelijke uurregistratieregel wilt doen (de eerste regel in het voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="13ba0-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="13ba0-141">U kunt deze houden of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="13ba0-141">You can keep it as is or delete it.</span></span> 

![Figuur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="13ba0-143">Financiële dimensies voor verbruiksregistraties</span><span class="sxs-lookup"><span data-stu-id="13ba0-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="13ba0-144">Wanneer u verbruiksregistraties uitvoert, worden financiële dimensies met betrekking tot de verschillende registratietypen in een specifieke volgorde aan de registraties toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="13ba0-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="13ba0-145">*Uur- en onkostenregistraties:* eerst worden financiële dimensies uit de journaalkoptekst toegevoegd, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="13ba0-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="13ba0-146">Vervolgens worden financiële dimensies uit het gerelateerde werkorderproject toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="13ba0-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="13ba0-147">Tot slot worden financiële dimensies van de resource (medewerker) toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="13ba0-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="13ba0-148">*Uurregistraties:* eerst worden financiële dimensies uit de journaalkoptekst toegevoegd, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="13ba0-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="13ba0-149">Vervolgens worden financiële dimensies uit het gerelateerde werkorderproject toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="13ba0-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="13ba0-150">Vervolgens worden financiële dimensies van de site toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="13ba0-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="13ba0-151">Tot slot worden financiële dimensies van het artikel toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="13ba0-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="13ba0-152">Voor alle drie de registratietypen wordt de combinatie van financiële dimensies gevalideerd en ongeldige combinaties worden blanco gemaakt.</span><span class="sxs-lookup"><span data-stu-id="13ba0-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="13ba0-153">Dit is standaardinstelling bij andere Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="13ba0-153">This is standard setup with other Finance and Operations apps.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]