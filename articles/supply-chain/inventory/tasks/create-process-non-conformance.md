---
title: Een conformiteit maken en verwerken
description: Gebruik deze procedure om beheer van non-conformiteiten uit te voeren, op basis van een bestaande kwaliteitsorder.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572806"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="cf4e8-103">Een conformiteit maken en verwerken</span><span class="sxs-lookup"><span data-stu-id="cf4e8-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf4e8-104">Gebruik deze procedure om beheer van non-conformiteiten uit te voeren, op basis van een bestaande kwaliteitsorder.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="cf4e8-105">U kunt deze registratie in het demobedrijf USMF uitvoeren en u kunt de voorgestelde waarden gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="cf4e8-106">Doorgaans wordt deze procedure uitgevoerd door een kwaliteitsbewakingsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="cf4e8-107">Voer als vereiste vooraf de taakregistratie 'De kwaliteit van goederen inspecteren' uit.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="cf4e8-108">Om de goedkeuring van een niet-conformering te verwerken moet aan de gebruiker die de taakregistratie uitvoert, een 'Naam'-waarde zijn toegewezen op de pagina Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="cf4e8-109">Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="cf4e8-110">Een kwaliteitsorder selecteren</span><span class="sxs-lookup"><span data-stu-id="cf4e8-110">Select a quality order</span></span>
1. <span data-ttu-id="cf4e8-111">Ga naar Kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="cf4e8-112">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cf4e8-113">Selecteer de kwaliteitsorder die is gemaakt van de taakregistratie 'De kwaliteit van goederen inspecteren'.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="cf4e8-114">Een non-conformiteit maken</span><span class="sxs-lookup"><span data-stu-id="cf4e8-114">Create a nonconformance</span></span>
1. <span data-ttu-id="cf4e8-115">Klik op Query's.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-115">Click Inquiries.</span></span>
2. <span data-ttu-id="cf4e8-116">Klik op Non-conformiteiten.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-116">Click Non conformances.</span></span>
3. <span data-ttu-id="cf4e8-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-117">Click New.</span></span>
4. <span data-ttu-id="cf4e8-118">Klik in het veld Probleemtype op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cf4e8-119">Selecteer het probleem dat tijdens het inspectieproces is gevonden.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="cf4e8-120">Klik in het veld Probleemtype op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="cf4e8-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cf4e8-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cf4e8-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="cf4e8-124">Een non-conformiteit goedkeuren/afwijzen</span><span class="sxs-lookup"><span data-stu-id="cf4e8-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="cf4e8-125">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-125">Click Functions.</span></span>
2. <span data-ttu-id="cf4e8-126">Klik op Non-conformiteit goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="cf4e8-127">Keur voor dit voorbeeld de niet-conformering goed.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="cf4e8-128">Goedgekeurde non-conformiteiten kunnen aan gerelateerde bewerkingen worden gekoppeld om werk vast te leggen dat is uitgevoerd als onderdeel van de verwerking van de non-conformiteit en, zoals in deze taakregistratie, de verwerking van correctiebehandeling.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="cf4e8-129">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="cf4e8-130">Een correctieactie maken</span><span class="sxs-lookup"><span data-stu-id="cf4e8-130">Create a correction action</span></span>
1. <span data-ttu-id="cf4e8-131">Klik op Correcties.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-131">Click Corrections.</span></span>
2. <span data-ttu-id="cf4e8-132">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-132">Click New.</span></span>
3. <span data-ttu-id="cf4e8-133">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cf4e8-134">Klik in het veld Personeelsnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cf4e8-135">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cf4e8-136">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-136">Click Select.</span></span>
7. <span data-ttu-id="cf4e8-137">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-137">Click Attach.</span></span>
    * <span data-ttu-id="cf4e8-138">Maak een notitie over de correctie.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-138">Create a note about the correction.</span></span> <span data-ttu-id="cf4e8-139">In dit voorbeeld is de actie contact met de leverancier op te nemen om de non-conformiteit te bespreken.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="cf4e8-140">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-140">Click New.</span></span>
9. <span data-ttu-id="cf4e8-141">Klik op Notitie.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-141">Click Note.</span></span>
    * <span data-ttu-id="cf4e8-142">Afhankelijk van de rapportinstelling kunnen verschillende documenttypen worden afgedrukt in de rapporten die gerelateerd zijn aan beheer van non-conformiteiten.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="cf4e8-143">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="cf4e8-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="cf4e8-145">Een correctie onderhouden</span><span class="sxs-lookup"><span data-stu-id="cf4e8-145">Maintain a correction</span></span>
1. <span data-ttu-id="cf4e8-146">Klik op Als voltooid markeren.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-146">Click Mark complete.</span></span>
2. <span data-ttu-id="cf4e8-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-147">Click OK.</span></span>
3. <span data-ttu-id="cf4e8-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="cf4e8-149">Een niet-conformering sluiten</span><span class="sxs-lookup"><span data-stu-id="cf4e8-149">Close a nonconformance</span></span>
1. <span data-ttu-id="cf4e8-150">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-150">Click Functions.</span></span>
2. <span data-ttu-id="cf4e8-151">Klik op Non-conformiteit afsluiten.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="cf4e8-152">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-152">Click Yes.</span></span>
4. <span data-ttu-id="cf4e8-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-153">Close the page.</span></span>
5. <span data-ttu-id="cf4e8-154">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-154">Close the page.</span></span>
