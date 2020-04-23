---
title: Een conformiteit maken en verwerken
description: In dit onderwerp wordt het beheer van non-conformiteiten, op basis van een bestaande kwaliteitsorder, beschreven.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0c0c4415f490219485b3d96fa678a317c1f12f2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204120"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="80002-103">Een conformiteit maken en verwerken</span><span class="sxs-lookup"><span data-stu-id="80002-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80002-104">In dit onderwerp wordt het beheer van non-conformiteiten, op basis van een bestaande kwaliteitsorder, beschreven.</span><span class="sxs-lookup"><span data-stu-id="80002-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="80002-105">U kunt deze registratie in het demobedrijf USMF uitvoeren en u kunt de voorgestelde waarden gebruiken.</span><span class="sxs-lookup"><span data-stu-id="80002-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="80002-106">Doorgaans wordt deze procedure uitgevoerd door een kwaliteitsbewakingsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="80002-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="80002-107">Voer als vereiste de instructies in [De kwaliteit van goederen inspecteren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) uit.</span><span class="sxs-lookup"><span data-stu-id="80002-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="80002-108">Om de goedkeuring van een niet-conformering te verwerken moet aan de gebruiker die de taakregistratie uitvoert, een "Naam"-waarde zijn toegewezen op de pagina Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="80002-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="80002-109">Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="80002-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="80002-110">Een kwaliteitsorder selecteren</span><span class="sxs-lookup"><span data-stu-id="80002-110">Select a quality order</span></span>
1. <span data-ttu-id="80002-111">Ga in het navigatievenster naar **Modules > Voorraadbeheer > Periodieke taken > Kwaliteitsbeheer > Kwaliteitsorders**.</span><span class="sxs-lookup"><span data-stu-id="80002-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="80002-112">Selecteer in de lijst de kwaliteitsorder die is gemaakt in [De kwaliteit van goederen inspecteren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="80002-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="80002-113">Een non-conformiteit maken</span><span class="sxs-lookup"><span data-stu-id="80002-113">Create a nonconformance</span></span>
1. <span data-ttu-id="80002-114">Selecteer **Query's** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="80002-114">In the action pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="80002-115">Selecteer **Non-conformiteiten**.</span><span class="sxs-lookup"><span data-stu-id="80002-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="80002-116">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="80002-116">Select **New**.</span></span>
4. <span data-ttu-id="80002-117">Selecteer in de vervolgkeuzelijst van het veld **Probleemtype** het probleem dat tijdens het inspectieproces is aangetroffen.</span><span class="sxs-lookup"><span data-stu-id="80002-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="80002-118">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="80002-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="80002-119">Een non-conformiteit goedkeuren/afwijzen</span><span class="sxs-lookup"><span data-stu-id="80002-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="80002-120">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="80002-120">Select **Functions**.</span></span>
2. <span data-ttu-id="80002-121">Selecteer **Non-conformiteit goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="80002-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="80002-122">Keur voor dit voorbeeld de niet-conformering goed.</span><span class="sxs-lookup"><span data-stu-id="80002-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="80002-123">Goedgekeurde non-conformiteiten kunnen aan gerelateerde bewerkingen worden gekoppeld om werk vast te leggen dat is uitgevoerd als onderdeel van de verwerking van de non-conformiteit en, zoals in dit onderwerp, de verwerking van correctiebehandeling.</span><span class="sxs-lookup"><span data-stu-id="80002-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="80002-124">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80002-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="80002-125">Een correctieactie maken</span><span class="sxs-lookup"><span data-stu-id="80002-125">Create a correction action</span></span>
1. <span data-ttu-id="80002-126">Selecteer **Correcties**.</span><span class="sxs-lookup"><span data-stu-id="80002-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="80002-127">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="80002-127">Select **New**.</span></span>
3. <span data-ttu-id="80002-128">Selecteer in het veld **Personeelsnummer** van de nieuwe rij de gewenste record in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="80002-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="80002-129">Klik op **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="80002-129">Click **Select**.</span></span>
5. <span data-ttu-id="80002-130">Selecteer **Bijvoegen**.</span><span class="sxs-lookup"><span data-stu-id="80002-130">Select **Attach**.</span></span> <span data-ttu-id="80002-131">Maak een notitie over de correctie.</span><span class="sxs-lookup"><span data-stu-id="80002-131">Create a note about the correction.</span></span> <span data-ttu-id="80002-132">In dit voorbeeld is de actie contact met de leverancier op te nemen om de non-conformiteit te bespreken.</span><span class="sxs-lookup"><span data-stu-id="80002-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="80002-133">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="80002-133">Select **New**.</span></span>
7. <span data-ttu-id="80002-134">Selecteer **Opmerking**.</span><span class="sxs-lookup"><span data-stu-id="80002-134">Select **Note**.</span></span> <span data-ttu-id="80002-135">Afhankelijk van de rapportinstelling kunnen verschillende documenttypen worden afgedrukt in de rapporten die gerelateerd zijn aan beheer van non-conformiteiten.</span><span class="sxs-lookup"><span data-stu-id="80002-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="80002-136">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="80002-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="80002-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="80002-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="80002-138">Een correctie onderhouden</span><span class="sxs-lookup"><span data-stu-id="80002-138">Maintain a correction</span></span>
1. <span data-ttu-id="80002-139">Selecteer **Als voltooid markeren**.</span><span class="sxs-lookup"><span data-stu-id="80002-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="80002-140">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="80002-140">Select **OK**.</span></span>
3. <span data-ttu-id="80002-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="80002-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="80002-142">Een niet-conformering sluiten</span><span class="sxs-lookup"><span data-stu-id="80002-142">Close a nonconformance</span></span>
1. <span data-ttu-id="80002-143">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="80002-143">Select **Functions**.</span></span>
2. <span data-ttu-id="80002-144">Selecteer **Non-conformiteit afsluiten**.</span><span class="sxs-lookup"><span data-stu-id="80002-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="80002-145">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80002-145">Select **Yes**.</span></span>
4. <span data-ttu-id="80002-146">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="80002-146">Close the pages.</span></span>
