--- 
title: Periodieke journalen boeken
description: De periodieke journalen worden soms terugkerende journalen genoemd, omdat het bedrag, de tekst en andere informatie telkens worden herhaald als het periodieke journaal wordt opgehaald.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: deae523d922e1d6a4f7bb05433e9b1568c9c1ee9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="2aff5-103">Periodieke journalen boeken</span><span class="sxs-lookup"><span data-stu-id="2aff5-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2aff5-104">De periodieke journalen worden soms terugkerende journalen genoemd, omdat het bedrag, de tekst en andere informatie telkens worden herhaald als het periodieke journaal wordt opgehaald.</span><span class="sxs-lookup"><span data-stu-id="2aff5-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="2aff5-105">Wanneer u een periodiek journaal maakt, geeft u het periode-interval op voor het terugkeerpatroon, zoals dagen of maanden.</span><span class="sxs-lookup"><span data-stu-id="2aff5-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="2aff5-106">Deze taakbegeleiding maakt een periodiek journaal met een maandelijkse herhaling.</span><span class="sxs-lookup"><span data-stu-id="2aff5-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="2aff5-107">Ga naar Grootboek > Periodieke taken > Periodieke journalen.</span><span class="sxs-lookup"><span data-stu-id="2aff5-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="2aff5-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2aff5-108">Click New.</span></span>
3. <span data-ttu-id="2aff5-109">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="2aff5-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="2aff5-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2aff5-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2aff5-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="2aff5-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2aff5-112">De omschrijving wordt de naam van het periodieke journaal wanneer deze later wordt opgehaald, dus zorg ervoor dat u een relevante naam opgeeft.</span><span class="sxs-lookup"><span data-stu-id="2aff5-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="2aff5-113">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="2aff5-113">Click Lines.</span></span>
    * <span data-ttu-id="2aff5-114">Een periodiek journaal bevat doorgaans meerdere journaalregels.</span><span class="sxs-lookup"><span data-stu-id="2aff5-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="2aff5-115">Deze taakbegeleiding voegt echter slechts één regel toe.</span><span class="sxs-lookup"><span data-stu-id="2aff5-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="2aff5-116">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="2aff5-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="2aff5-117">Het veld Datum bevat de boekingsdatum voor de volgende overboeking naar het dagelijks journaal.</span><span class="sxs-lookup"><span data-stu-id="2aff5-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="2aff5-118">Voor journalen die elke maand worden opgehaald is het raadzaam om de datum in de maand te gebruiken wanneer het wordt geboekt, meestal de eerste of de laatste datum in de periode.</span><span class="sxs-lookup"><span data-stu-id="2aff5-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="2aff5-119">Het is mogelijk om het datumveld leeg te laten en een datum te geven wanneer het journaal wordt opgehaald door het lege datumveld te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2aff5-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="2aff5-120">Het veld wordt automatisch bijgewerkt naar de volgende terugkerende datum waarop transacties worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="2aff5-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="2aff5-121">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="2aff5-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="2aff5-122">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="2aff5-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="2aff5-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2aff5-123">Close the page.</span></span>
11. <span data-ttu-id="2aff5-124">Voer een nummer in het veld Debet in.</span><span class="sxs-lookup"><span data-stu-id="2aff5-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="2aff5-125">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="2aff5-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="2aff5-126">Selecteer Maanden in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="2aff5-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="2aff5-127">Voer 1 in het veld Aantal eenheden in.</span><span class="sxs-lookup"><span data-stu-id="2aff5-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="2aff5-128">Voer een datum in het veld Laatste datum in.</span><span class="sxs-lookup"><span data-stu-id="2aff5-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="2aff5-129">Het invoeren van de laatste datum in de eerdere periode voorkomt dat het terugkerende journaal per ongeluk in de verkeerde beginperiode wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2aff5-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="2aff5-130">De laatste datum wordt later bijgewerkt telkens als het periodieke journaal wordt opgehaald.</span><span class="sxs-lookup"><span data-stu-id="2aff5-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="2aff5-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="2aff5-131">Click Save.</span></span>
17. <span data-ttu-id="2aff5-132">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="2aff5-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="2aff5-133">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="2aff5-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="2aff5-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2aff5-134">Click New.</span></span>
20. <span data-ttu-id="2aff5-135">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="2aff5-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="2aff5-136">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="2aff5-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="2aff5-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2aff5-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="2aff5-138">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="2aff5-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="2aff5-139">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="2aff5-139">Click Lines.</span></span>
25. <span data-ttu-id="2aff5-140">Klik op Periodejournaal.</span><span class="sxs-lookup"><span data-stu-id="2aff5-140">Click Period journal.</span></span>
26. <span data-ttu-id="2aff5-141">Klik op Journaal ophalen.</span><span class="sxs-lookup"><span data-stu-id="2aff5-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="2aff5-142">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="2aff5-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="2aff5-143">De einddatum dient als de afsluitdatum voor de periodieke boekstukregels.</span><span class="sxs-lookup"><span data-stu-id="2aff5-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="2aff5-144">Gebaseerd op de herhalingsinstelling kunnen de laatste datum en de einddatum van dezelfde regel meer dan één keer in het resulterende journaal worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="2aff5-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="2aff5-145">De einddatum wordt automatisch bijgewerkt op basis van de sessiedatum van de laatste keer dat de periodieke regel is overgeboekt naar een journaal.</span><span class="sxs-lookup"><span data-stu-id="2aff5-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="2aff5-146">Typ of selecteer een waarde in het veld Periodiek-journaalnummer.</span><span class="sxs-lookup"><span data-stu-id="2aff5-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="2aff5-147">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2aff5-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="2aff5-148">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2aff5-148">Click OK.</span></span>
    * <span data-ttu-id="2aff5-149">Het periodejournaal kan nu worden gecontroleerd, goedgekeurd of geboekt, afhankelijk van vereisten en instellingen.</span><span class="sxs-lookup"><span data-stu-id="2aff5-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


